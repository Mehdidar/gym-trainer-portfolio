# Shivaraju K — Strength & Conditioning Coach

Portfolio website for a certified strength and conditioning coach in Bengaluru: services, physique gallery, certifications, and a lead form for new clients.

## Built with
- HTML, CSS and vanilla JavaScript
- [AOS](https://michalsnik.github.io/aos/) scroll animations and [Phosphor](https://phosphoricons.com/) icons
- Deployed on [Vercel](https://vercel.com) (`vercel.json` gives clean URLs and the `/admin` route)

## Project structure
```
index.html            # Main portfolio page
shiva_portfolio.html  # Alternate version of the portfolio page
admin.html            # Lead dashboard (reads /api/leads)
style.css             # Styles
*.png / *.jpeg        # Gallery photos and certificates (lowercase, hyphenated names)
vercel.json           # Vercel routing
package.json          # Backend dependencies (Resend for email, ioredis for storage)
```

## Run locally
Open `index.html` in a browser, or serve the folder:
```bash
npx serve .
```

## Lead dashboard
`admin.html` calls `/api/leads` and `/api/manage-lead`. These serverless functions are not in this repository yet, so the dashboard only works once an `api/` folder with those endpoints (using Resend and Redis, per `package.json`) is added and deployed. The dashboard should also require a login before showing any client data.

## Configuration
Keep API keys (Resend, Redis) in Vercel's Environment Variables or a local `.env` file — never commit them. `.env` is listed in `.gitignore`.

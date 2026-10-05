# Nexus AI Frontend

Next.js 15 (App Router) + TypeScript frontend for the Nexus AI Spring Boot API.

## Requirements
- Node.js 18.18 or newer (`node -v`)
- The backend running on `http://localhost:8080`

## Run (VS Code)
```bash
npm install
npm run dev
```
Open http://localhost:3000.

`.env.local` points the app to the backend:
```
NEXT_PUBLIC_API_URL=http://localhost:8080
NEXT_PUBLIC_APP_URL=http://localhost:3000
```
If the backend runs on another machine, change `NEXT_PUBLIC_API_URL` and restart `npm run dev`.

## Scripts
| Command | What it does |
|---|---|
| `npm run dev` | development server |
| `npm run build` | production build (also type-checks) |
| `npm start` | serve the production build |

## Pages
Auth: `/login`, `/register`, `/verify-otp`, `/forgot-password`, `/reset-password`.
App: `/dashboard`, `/resume`, `/jobs`, `/jobs/recommended`, `/applications`,
`/companies`, `/company-recommendations`, `/career-intelligence`,
`/tools/cover-letter`, `/tools/roadmap`, `/interview/questions`,
`/interview/practice`, `/interview/session`, `/premium`, `/payments`,
`/profile`, `/settings`, `/help`, `/admin`.

## Troubleshooting
- **Old screens after replacing files:** delete the `.next` folder and run `npm run dev` again.
- **"Hydration failed" in the console:** browser extensions such as Grammarly modify `<body>`; the app ignores that. Use a clean browser profile when recording demos.
- **401 or "Something went wrong" on AI pages:** set `OPENROUTER_API_KEY` in the backend and restart it.
- **Empty Company Match or Question Bank:** restart the backend once (companies are seeded on startup) and use *Generate with AI* on the Question Bank page.
- **Career Intelligence:** the backend has the service but no REST controller yet, so that page does not call an API.

# Nexus AI Frontend — Design Notes

The UI is intentionally close to the supplied final dashboard reference while using a new Nexus AI mark and a slightly different visual treatment: purple/blue gradients, softer cards, a wider information hierarchy and responsive navigation.

## Implemented frontend areas
- Auth: login, register, OTP verification, forgot/reset password
- Dashboard
- Resume Hub + upload + analyze
- Jobs + search + latest + recommendations
- Applications
- Company list + company recommendations
- Cover letter + career roadmap
- Question bank + mock interview + interview session
- Premium Razorpay flow + payment history
- Profile + settings + help
- Admin users + companies + question bank
- Career Intelligence premium landing/contract note

## Backend contract rule
The supplied `api-docs.json` is treated as the source of truth. The frontend does not invent a Career Intelligence HTTP endpoint because the backend currently has a service without a REST controller.

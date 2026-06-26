# Showtime — Equestrian Event Management Platform

A cross-platform event management application for the equestrian industry, built for organisers, riders, and venues. Designed as a direct competitor to US-based platforms, with a focus on the South African market and features tailored to local disciplines and workflows.

---

## Features

- **Event creation and management** — full lifecycle from setup to results
- **Online entries** — riders enter classes directly through the mobile app
- **Auto-generated ride orders** — algorithmic scheduling eliminates manual timetabling
- **Live arena status** — real-time per-arena updates during competition day
- **Push notifications** — instant alerts to riders for schedule changes
- **PDF generation** — printable programmes and entry sheets
- **Payments** — Stripe integration for entry fees
- **Multi-discipline support** — showjumping, dressage, showing, and more

---

## Tech Stack

| Layer | Technology |
|---|---|
| Mobile | React Native + Expo (iOS & Android) |
| Language | TypeScript (mobile), Python (backend) |
| Backend | FastAPI |
| Database | PostgreSQL + SQLAlchemy + Alembic |
| Task Queue | Redis + Celery |
| Auth | JWT / OAuth2 (Google & Apple sign-in) |
| Storage | AWS S3 / Cloudflare R2 |
| Notifications | Expo Push Notifications |
| PDF Generation | WeasyPrint |
| Monitoring | Sentry |
| Deployment | Railway (backend), Expo EAS (mobile) |

---

## Architecture Overview

```
┌──────────────────────┐      ┌──────────────────────┐
│   React Native App   │      │     Web Portal       │
│   (iOS & Android)    │      │   (Vercel / Next.js) │
└──────────┬───────────┘      └──────────┬───────────┘
           │                             │
           └──────────────┬──────────────┘
                          │ REST API
              ┌───────────▼───────────┐
              │      FastAPI          │
              │   (Railway/Render)    │
              └─────┬──────────┬──────┘
                    │          │
         ┌──────────▼──┐  ┌───▼──────────┐
         │ PostgreSQL   │  │ Redis/Celery  │
         │ (SQLAlchemy) │  │ (async tasks) │
         └─────────────┘  └──────────────┘
```

---

## Screenshots

*Contact me for a live demo or walkthrough.*

---

## Source Code

This is a portfolio showcase. The full source code is private as this project has commercial potential.

**Interested in the codebase or a walkthrough?** Reach out via [GitHub](https://github.com/James-Gooch-Git) or [email](mailto:gewainwright@gmail.com).

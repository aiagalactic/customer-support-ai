# Customer Support AI

AI agent that institutions (schools, hospitals, clinics) can use to answer client questions via Website, WhatsApp, and Messenger.

## Features

- Smart Q&A from PDF/FAQ uploads (LangChain + GPT)
- WhatsApp, Messenger, and web support
- Admin dashboard compatibility
- Stripe billing with webhook for credits
- Multi-language support

## Deployment on Render

1. Push this repo to GitHub
2. Go to [https://render.com](https://render.com)
3. Click **New → Web Service**
4. Connect the GitHub repo and select this project
5. Set these environment variables:

- `OPENAI_API_KEY`
- `STRIPE_SECRET_KEY`
- `STRIPE_WEBHOOK_SECRET`
- `SECRET_KEY`

Your service will go live and be ready to answer messages.

## Endpoints

- `POST /register` — Register org
- `POST /upload` — Upload PDFs
- `POST /message` — Send question
- `POST /create-checkout-session` — Payment link
- `POST /webhook` — Stripe payment listener

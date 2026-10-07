# 💗 Romantic Comment Website

A small responsive Next.js romantic page with two photo cards and a private message form that sends messages through Resend.

## 1. Install

```bash
npm install
```

## 2. Add your photos

Put your photos here:

```text
public/photos/photo1.jpg
public/photos/photo2.jpg
```

## 3. Configure Resend

Copy `.env.example` to `.env.local` and fill in:

```env
RESEND_API_KEY=re_xxxxxxxxxxxxxxxxx
TO_EMAIL=yourgmail@gmail.com
RESEND_FROM_EMAIL=Date Website <onboarding@resend.dev>
```

Keep `.env.local` private. Never commit your API key.

### Important about onboarding@resend.dev

Resend's onboarding sender is intended for testing. Depending on your Resend account/testing restrictions, you may only be able to send to your own/verified recipient. For a public website where anyone can submit messages, set up and verify a domain in Resend and use a sender address from that domain.

## 4. Run

```bash
npm run dev
```

Open `http://localhost:3000`.

## Email endpoint

The form sends a POST request to:

```text
/api/send-comment
```

The server route keeps your Resend API key out of the browser.

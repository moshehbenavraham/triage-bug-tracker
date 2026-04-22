# Triage

Triage is a React and TypeScript bug tracking dashboard for fast-moving engineering teams. It provides email and Google sign-in, issue creation, status tracking, severity filters, and analytics backed by Supabase.

## Stack

- React 18
- TypeScript
- Vite
- Tailwind CSS
- shadcn/ui
- Supabase

## Requirements

- Node.js 20+
- npm 10+
- A Supabase project with auth enabled

## Environment

Create a local `.env` file with:

```bash
VITE_SUPABASE_URL=https://your-project.supabase.co
VITE_SUPABASE_PUBLISHABLE_KEY=your-supabase-anon-key
```

If you want Google sign-in, enable the Google provider in Supabase Auth and set the callback URL to your app origin.

## Local Development

```bash
npm install
npm run dev
```

## Production Build

```bash
npm run build
npm run preview
```

The compiled app is emitted to `dist/` and can be served with standard tooling such as Nginx, Caddy, Apache, or any static hosting provider.

## Testing

```bash
npm test
```

## Deployment Notes

- Configure the two `VITE_SUPABASE_*` variables in your deployment environment.
- Make sure your Supabase auth redirect URLs include each deployed domain.
- This project no longer depends on vendor-specific build plugins or managed auth wrappers.

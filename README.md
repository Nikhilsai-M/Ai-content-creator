# ContentForge

ContentForge is a full-stack publishing platform for creators who want to draft, edit, publish, and grow content from one dashboard. It combines AI-assisted writing, rich post editing, public creator profiles, engagement tools, and analytics in a modern Next.js application.

## Features

- AI-powered content generation with Gemini
- Rich post editor with draft and publish workflows
- Image upload support through ImageKit
- Public creator profiles and individual post pages
- Community feed for discovering published content
- Likes, comments, and follower relationships
- Creator dashboard with post analytics and daily view charts
- Profile settings for custom usernames
- Clerk authentication with Convex-backed user storage

## Tech Stack

- Next.js 15 and React 19
- Tailwind CSS 4
- Convex for database, queries, and mutations
- Clerk for authentication
- Gemini API for AI writing support
- ImageKit for image uploads and delivery
- shadcn-style UI components

## Getting Started

Install dependencies:

```bash
npm install
```

Create a `.env.local` file in the project root and add the required environment variables:

```env
# Convex
CONVEX_DEPLOYMENT=
NEXT_PUBLIC_CONVEX_URL=

# Clerk
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
CLERK_JWT_ISSUER_DOMAIN=

# ImageKit
NEXT_PUBLIC_IMAGEKIT_PUBLIC_KEY=
NEXT_PUBLIC_IMAGEKIT_URL_ENDPOINT=
IMAGEKIT_PRIVATE_KEY=

# Unsplash
NEXT_PUBLIC_UNSPLASH_ACCESS_KEY=

# Gemini
GEMINI_API_KEY=
GEMINI_MODEL=gemini-2.5-flash
```

Run the development server:

```bash
npm run dev
```

In another terminal, start Convex:

```bash
npx convex dev
```

Open `http://localhost:3000` to use the app.

## Project Structure

- `app/` - Next.js routes, layouts, API routes, and server actions
- `components/` - Reusable UI and feature components
- `convex/` - Convex schema, queries, and mutations
- `hooks/` - Client hooks for auth and Convex data loading
- `lib/` - Shared utilities, static content, and service clients
- `public/` - Static assets

## Scripts

```bash
npm run dev
npm run build
npm run start
npm run lint
```

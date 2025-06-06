# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Commands

### Local Development

- `npm run dev` - Start development server with Turbopack
- `npm run build` - Build the Next.js application
- `npm run start` - Start production server
- `npm run lint` - Run ESLint

### Cloudflare Deployment

- `npm run deploy:build` - Build for Cloudflare using OpenNext
- `npm run deploy:only` - Deploy to Cloudflare
- `npm run deploy` - Build and deploy to Cloudflare
- `npm run preview` - Build and preview locally before deployment
- `npm run cf-typegen` - Generate Cloudflare types

## Architecture

This is a Next.js 15 tech blog deployed to Cloudflare Workers using OpenNext.js for Cloudflare. The project uses the App Router architecture.

### Key Technologies

- **Next.js 15** with App Router
- **React 19** for the frontend
- **Tailwind CSS v4** for styling
- **TypeScript** for type safety
- **OpenNext.js Cloudflare** for deployment to Cloudflare Workers
- **Wrangler** for Cloudflare tooling

### Project Structure

- Uses App Router (`src/app/`) with layout.tsx and page.tsx
- Path aliases configured with `@/*` pointing to `./src/*`
- Cloudflare-specific configuration in `open-next.config.ts` and `wrangler.jsonc`
- TypeScript types for Cloudflare environment in `cloudflare-env.d.ts`

### Deployment Architecture

The application is built using OpenNext.js which adapts Next.js for Cloudflare Workers. The build process creates a worker.js file and static assets that are deployed to Cloudflare's edge network.

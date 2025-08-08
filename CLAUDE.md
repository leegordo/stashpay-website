# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

StashPay is a Bitcoin wallet website built with Astro.js. This is a static site generator project based on the Astroship template from Web3Templates. The site appears to be a marketing/landing page for a minimalist Bitcoin wallet called StashPay.

## Development Commands

### Start Development Server
```bash
npm run dev
# or
pnpm dev  # recommended
```

### Build for Production
```bash
npm run build
# or
pnpm build  # recommended
```

### Preview Production Build
```bash
npm run preview
# or
pnpm preview  # recommended
```

### Package Manager
This project uses pnpm as the recommended package manager (as noted in README.md). Both `package-lock.json` and `pnpm-lock.yaml` are present, but pnpm should be preferred for new installations.

## Architecture

### Framework: Astro.js
- **Type**: Static Site Generator with component-based architecture
- **Config**: `astro.config.mjs` - configured for site domain `https://stashpay.me`
- **Integrations**: TailwindCSS, MDX, Sitemap, Astro Icon

### Styling: TailwindCSS
- **Config**: `tailwind.config.cjs`
- **Typography Plugin**: Included for rich text content
- **Font**: Inter Variable (loaded via @fontsource-variable/inter)

### Project Structure
```
src/
├── components/           # Reusable Astro components
│   ├── navbar/          # Navigation components
│   ├── ui/              # UI primitives (buttons, links, icons)
│   └── *.astro          # Feature components (hero, features, etc.)
├── layouts/             # Page layouts
│   └── Layout.astro     # Main layout with SEO, navbar, footer
├── pages/               # File-based routing
│   ├── index.astro      # Homepage (simplified - only shows Hero)
│   ├── contact.astro    # Contact page
│   ├── privacy.astro    # Privacy policy
│   └── terms.astro      # Terms of service
├── content/             # Content collections
├── assets/              # Images and static assets
└── utils/               # Utility functions
```

### Key Components
- **Layout.astro**: Main layout with SEO configuration, includes navbar and footer
- **Hero.astro**: Main hero section component
- **Container.astro**: Layout wrapper component
- Various feature components: CTA, Features, Logos, Pricing, etc.

## Content Strategy

The site is focused on Bitcoin/cryptocurrency with branding for "StashPay - A minimalist Bitcoin wallet for everyone" built on Lightning & Liquid networks.

## Deployment

The project appears configured for deployment to `stashpay.me` domain with:
- Static file generation
- SEO optimization with astro-seo
- Sitemap generation
- OpenGraph image (`/opengraph.jpg`)

## Important Notes

- This is based on the Astroship template but customized for StashPay branding
- The homepage is simplified compared to typical Astroship setup (only shows Hero component)
- Social media handles in Layout.astro still reference template defaults (@surjithctly, @web3templates)
- Claude Code package is included as dev dependency for development assistance
- reboot-astro-server: the astro server is throwing this error "ERR_CONNECTION_REFUSED" ensure the local server is running correctly
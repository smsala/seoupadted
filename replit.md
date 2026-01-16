# SMSala CPaaS Platform

## Overview

SMSala is an enterprise-grade Communications Platform as a Service (CPaaS) website designed for global B2B communications. The platform provides SMS, WhatsApp, and Voice services across 180+ countries. Built as a marketing/informational website with contact form functionality, it focuses on international SEO, programmatic content generation for country-specific pages, and conversion optimization.

The architecture follows a monorepo structure with a React frontend (Vite), Express backend, and PostgreSQL database using Drizzle ORM. The design system follows clean B2B SaaS principles inspired by Stripe, Twilio, and Linear.

## Recent Changes (January 15, 2026)

- **Complete website build**: All pages (home, service categories, service details, country pages, about, pricing, contact) fully implemented with modern Sinch/Plivo-style design
- **Advanced SEO**: Schema.org markup for Organization, Service, FAQ, Review, and Breadcrumb; hreflang tags with x-default for international SEO; canonical URLs and meta tags across all pages
- **Reviews system**: Created reviews.ts with global reviews and 15+ country-specific review sets; integrated ReviewsSection and CompactReviews components across all pages
- **Content expansion**: All pages expanded to 1200+ words with detailed sections including "What is it?", "How It Works", "Benefits", "Use Cases", and FAQs
- **Enhanced navigation**: Header with mega-menus for Products/Solutions/Countries; Footer with multi-column layout including Products, Use Cases, Countries, Company, Legal sections
- **Backend API**: Contact form submission endpoint at `/api/contact` with in-memory storage

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript, bundled by Vite
- **Routing**: Wouter (lightweight client-side router)
- **State Management**: TanStack Query for server state, React Context for theme
- **Styling**: Tailwind CSS with shadcn/ui component library (New York style)
- **Animations**: Framer Motion (minimal usage for performance)
- **Path Aliases**: `@/` maps to `client/src/`, `@shared/` maps to `shared/`

### Page Structure
The site implements a programmatic SEO strategy:
- Global pages: `/`, `/sms`, `/whatsapp`, `/voice`, `/contact`, `/about`, `/pricing`
- Service detail pages: `/{category}/{service-slug}` (e.g., `/sms/bulk-sms`)
- Country-specific pages: `/{country-code}` and `/{country-code}/{category}/{service}`
- Legal pages: `/privacy`, `/terms`, `/cookies`, `/gdpr`

### Backend Architecture
- **Framework**: Express.js with TypeScript
- **Server**: HTTP server with development (Vite middleware) and production (static serving) modes
- **API Pattern**: RESTful endpoints under `/api/` prefix
- **Build Process**: Custom build script using esbuild for server, Vite for client

### Data Layer
- **ORM**: Drizzle ORM with PostgreSQL dialect
- **Schema Location**: `shared/schema.ts` (shared between frontend and backend)
- **Validation**: Zod schemas generated from Drizzle schemas via `drizzle-zod`
- **Storage**: Abstracted storage interface with in-memory implementation (database-ready)

### Content Strategy
- Service definitions stored in `client/src/data/services.ts` as TypeScript objects
- Country data with telecom regulations in `client/src/data/countries.ts`
- Content is JSON-based and CMS-ready for future migration

### Design System
- Typography: Inter font family for UI, JetBrains Mono for code
- Color scheme: CSS variables with light/dark mode support
- Component library: Full shadcn/ui implementation with Radix UI primitives
- Spacing: Follows Tailwind default scale with documented design guidelines

## External Dependencies

### Database
- **PostgreSQL**: Primary database (requires `DATABASE_URL` environment variable)
- **Drizzle Kit**: Database migrations via `drizzle-kit push`

### UI Component Libraries
- **Radix UI**: Headless primitives for accessibility (accordion, dialog, dropdown, etc.)
- **shadcn/ui**: Pre-styled components built on Radix
- **Lucide React**: Icon library

### Development Tools
- **Vite**: Frontend build tool with HMR
- **tsx**: TypeScript execution for development server
- **esbuild**: Production bundling for server code

### Replit-Specific
- `@replit/vite-plugin-runtime-error-modal`: Error overlay in development
- `@replit/vite-plugin-cartographer`: Development tooling
- `@replit/vite-plugin-dev-banner`: Development environment indicator

### Form & Validation
- **react-hook-form**: Form state management
- **@hookform/resolvers**: Zod integration for form validation
- **zod**: Schema validation library

### Session Management (Available)
- `connect-pg-simple`: PostgreSQL session store (configured but not currently used)
- `express-session`: Session middleware (available for future auth features)
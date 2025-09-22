# ALF ID - Digital Certificates Landing Page

## Overview

This is a modern, responsive landing page for ALF ID, a company specializing in digital certificates. The application is built as a full-stack web application with a React frontend and Express backend, designed to showcase ALF ID's services and provide an engaging user experience for potential customers seeking digital certificate solutions.

The landing page features a hero section with an image carousel, service offerings, and comprehensive information about digital certificates for both individuals and businesses. The design emphasizes mobile-first responsiveness and modern UI patterns using shadcn/ui components.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety and modern development practices
- **Routing**: Wouter for lightweight client-side routing
- **UI Framework**: shadcn/ui component library built on Radix UI primitives for accessible, customizable components
- **Styling**: Tailwind CSS with custom design system variables and Montserrat font family
- **State Management**: TanStack Query (React Query) for server state management and data fetching
- **Build Tool**: Vite for fast development and optimized production builds

### Backend Architecture
- **Runtime**: Node.js with Express.js framework for RESTful API development
- **Language**: TypeScript for type safety across the entire stack
- **Architecture Pattern**: Monorepo structure with shared schema definitions between client and server
- **Storage Interface**: Abstracted storage layer with in-memory implementation (MemStorage) allowing for easy database integration later

### Data Storage Solutions
- **ORM**: Drizzle ORM configured for PostgreSQL with type-safe database operations
- **Database**: PostgreSQL (configured but not yet implemented, using Neon serverless provider)
- **Schema Management**: Centralized schema definitions in shared directory using Drizzle and Zod for validation
- **Migrations**: Drizzle Kit for database schema migrations and management

### Authentication and Authorization
- **Session Management**: Express sessions configured with PostgreSQL session store (connect-pg-simple)
- **User Schema**: Basic user model with username/password authentication structure
- **Security**: Prepared for secure authentication implementation with password hashing and session management

### External Dependencies
- **Database Provider**: Neon Database for serverless PostgreSQL hosting
- **UI Components**: Extensive Radix UI component library for accessibility and consistent design
- **Image Hosting**: Backblaze B2 cloud storage for static assets and images
- **WhatsApp Integration**: Direct WhatsApp messaging integration for customer communication
- **Development Tools**: Replit-specific plugins for development environment optimization

### Design System
- **Color Palette**: Custom CSS variables with primary color #001f32 (dark blue) and white secondary
- **Typography**: Montserrat font family for modern, clean text rendering
- **Responsive Design**: Mobile-first approach with Tailwind's responsive utilities
- **Component Architecture**: Modular component structure with reusable UI elements
- **Animation**: CSS transitions and transforms for smooth user interactions

### Development Workflow
- **Hot Reload**: Vite HMR for fast development iteration
- **Type Checking**: Comprehensive TypeScript configuration across client, server, and shared code
- **Code Organization**: Clear separation of concerns with dedicated directories for components, pages, hooks, and utilities
- **Build Process**: Optimized production builds with code splitting and asset optimization

## Complete Project Structure

The project now includes a complete build structure as requested, matching standard web development patterns:

### Directory Structure
```
├── client/                 # Frontend React application
│   ├── src/               # React source code
│   ├── index.html         # Main HTML template with SEO optimization
│   └── ...                # Component files, hooks, pages
├── server/                # Backend Express application
│   ├── index.ts           # Main server entry point
│   ├── routes.ts          # API route definitions
│   ├── storage.ts         # Data storage interface
│   └── vite.ts           # Vite integration
├── shared/                # Shared TypeScript definitions
│   └── schema.ts          # Database schema and types
├── public/                # Static public assets
│   ├── favicon.ico        # Website icon
│   ├── logo.svg          # ALF ID logo
│   ├── manifest.json     # PWA manifest
│   ├── robots.txt        # Search engine rules
│   └── sitemap.xml       # Site structure for SEO
├── assets/                # Project assets
│   ├── images/           # Image assets
│   └── icons/            # Icon assets
├── dist/                  # Production build output
│   ├── index.js          # Compiled server code
│   └── public/           # Compiled frontend assets
├── project/               # Project documentation
│   ├── README.md         # Project documentation
│   ├── CHANGELOG.md      # Version history
│   └── package-info.json # Extended package information
├── node_modules/          # Dependencies
├── package.json          # Project configuration
├── vite.config.ts        # Vite build configuration
├── tailwind.config.ts    # Tailwind CSS configuration
├── tsconfig.json         # TypeScript configuration
├── drizzle.config.ts     # Database configuration
├── .gitignore           # Git ignore rules
└── replit.md            # This documentation
```

### Build System Configuration
- **Production Build**: `npm run build` creates optimized client and server bundles
- **Development**: `npm run dev` runs both frontend and backend with hot reload
- **Production Start**: `npm run start` runs the compiled production server
- **Type Checking**: `npm run check` validates TypeScript across the project
- **Database**: `npm run db:push` manages database schema updates

### Build Outputs
- **Frontend**: Compiled to `dist/public/` with optimized assets and chunking
- **Backend**: Compiled to `dist/index.js` with all dependencies bundled
- **Assets**: Favicon, manifest, robots.txt, and sitemap included in build

### SEO and Performance
- **Meta Tags**: Complete Open Graph and Twitter Card implementation
- **PWA Support**: Web app manifest for mobile installation
- **Search Engine Optimization**: Robots.txt and sitemap.xml configured
- **Performance**: Code splitting, asset optimization, and modern bundling

This structure follows web development best practices and provides a complete, production-ready build system.
- **Type Checking**: Comprehensive TypeScript configuration across client, server, and shared code
- **Code Organization**: Clear separation of concerns with dedicated directories for components, pages, hooks, and utilities
- **Build Process**: Optimized production builds with code splitting and asset optimization
- **Animation System**: Framer Motion with React Intersection Observer for scroll-triggered animations
- **Responsive Design**: Mobile-first approach with sticky navigation and optimized touch interactions

### Recent Updates (August 2025)
- **Scroll Animations**: Implemented smooth, modern animations for all page elements using ScrollReveal component
- **Fixed Header**: Enhanced navigation header that follows the page during scroll with backdrop blur effect and 40% opacity
- **Carousel Update**: Updated main carousel to display 3 custom mockup images from Backblaze B2 storage with Brazilian Portuguese titles in portrait format (700x1300)
- **Logo Enhancement**: Added ALF ID logo to header with transparent background and drop shadow effect, removing white background
- **Button Optimization**: Centralized and resized all call-to-action buttons for better user experience and visual consistency
- **Contact Sections**: Improved "Atendemos pessoas físicas" and "Entre em Contato" sections with better layout and button sizing
- **Icon Button**: Simplified certificate discovery button to a clean circular phone icon for minimalist design
- **Dark Sections**: Added alternating dark blue (#001f32) sections with white text and highlighted content boxes
- **Enhanced UX**: All sections now feature entrance animations with staggered delays for visual appeal
- **Mobile Optimization**: Responsive design improvements ensuring perfect functionality on all devices
- **Visual Hierarchy**: Improved content highlighting with glass-morphism effect boxes and emphasized text elements
- **Mobile Menu**: Implemented functional hamburger menu for mobile navigation with smooth animations and auto-close functionality
- **Partners Section**: Added new "Parceiros" section with partner logos and navigation integration
- **Final Build**: Created production-ready build with all features optimized for deployment (site_final_alf_id.zip)
# Portfolio Website - replit.md

## Overview

This is a modern full-stack portfolio website built with React, TypeScript, and Express.js. The application features a personal portfolio showcasing projects, skills, and providing a contact form. It uses a clean, dark-themed design with smooth animations and responsive layouts.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Styling**: Tailwind CSS with custom dark theme
- **UI Components**: Radix UI primitives with shadcn/ui styling
- **Animations**: Framer Motion for smooth transitions and effects
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack Query for server state management
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js server
- **Language**: TypeScript with ES modules
- **Database**: PostgreSQL with Drizzle ORM
- **Cloud Provider**: Neon Database for serverless PostgreSQL
- **API Design**: RESTful endpoints for contacts, projects, and skills
- **Data Validation**: Zod schemas shared between client and server

### Build System
- **Frontend Bundler**: Vite with React plugin
- **Backend Bundler**: esbuild for production builds
- **Development**: Hot module replacement and error overlay
- **TypeScript**: Strict mode with path mapping for clean imports

## Key Components

### Data Models
- **Contacts**: Stores contact form submissions with newsletter preferences
- **Projects**: Portfolio projects with categories, technologies, and links
- **Skills**: Technical skills organized by category with proficiency levels
- **Users**: Basic user system (structure in place for future expansion)

### UI Sections
- **Navigation**: Fixed header with smooth scroll navigation
- **Hero**: Animated landing section with personal introduction
- **About**: Personal story and experience highlights
- **Skills**: Technical skills organized by category with visual indicators
- **Projects**: Filterable project showcase with live/GitHub links
- **Contact**: Contact form with validation and newsletter signup
- **Footer**: Additional navigation and social links

### Shared Components
- Reusable UI components from shadcn/ui library
- Custom animation variants for consistent motion design
- Form components with integrated validation
- Responsive design patterns for mobile and desktop

## Data Flow

1. **Client Requests**: React components use TanStack Query to fetch data
2. **API Layer**: Express.js routes handle CRUD operations
3. **Database Layer**: Drizzle ORM manages PostgreSQL interactions
4. **Response Flow**: JSON responses with proper error handling
5. **State Updates**: TanStack Query handles caching and invalidation

### Storage Implementation
- In-memory storage for development (MemStorage class)
- Database abstraction layer (IStorage interface) for easy switching
- Sample data initialization for demo purposes

## External Dependencies

### Frontend Libraries
- **UI Framework**: React with TypeScript support
- **Styling**: Tailwind CSS with PostCSS processing
- **Components**: Extensive Radix UI component library
- **Animations**: Framer Motion for complex animations
- **Forms**: React Hook Form with Hookform resolvers
- **HTTP Client**: Native fetch with TanStack Query wrapper
- **Date Handling**: date-fns for date formatting

### Backend Libraries
- **Server**: Express.js with TypeScript
- **Database**: Drizzle ORM with PostgreSQL dialect
- **Validation**: Zod for runtime type checking
- **Database Driver**: Neon serverless PostgreSQL driver
- **Session Management**: connect-pg-simple for PostgreSQL sessions

### Development Tools
- **Build Tools**: Vite for frontend, esbuild for backend
- **TypeScript**: Strict configuration with path mapping
- **Linting**: Built-in TypeScript checking
- **Development**: tsx for TypeScript execution
- **Replit Integration**: Cartographer plugin and error modal

## Deployment Strategy

### Production Build
- Frontend builds to `dist/public` directory
- Backend bundles to `dist/index.js` with external packages
- Static file serving through Express in production
- Environment-based configuration for database connections

### Development Environment
- Vite dev server with HMR for frontend development
- Express server with automatic TypeScript compilation
- Database migrations through Drizzle Kit
- Replit-specific development enhancements

### Database Management
- Schema defined in shared TypeScript files
- Migrations generated and applied through Drizzle Kit
- Environment variable configuration for database URL
- PostgreSQL dialect with Neon serverless driver

### Environment Configuration
- Development: Local development with Vite middleware
- Production: Static file serving with optimized builds
- Database: Environment-based connection string
- Build optimization: Tree shaking and code splitting
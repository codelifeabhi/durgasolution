# Durga Solutions - Computer Repair Landing Page

## Overview

This project is a professional landing page for Durga Solutions, a computer and laptop repair service business. It's built as a full-stack web application using modern technologies to create an engaging, responsive website that attracts customers and converts visitors into service requests.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety and modern development patterns
- **Styling**: Tailwind CSS with shadcn/ui components for consistent, professional design
- **Build Tool**: Vite for fast development and optimized production builds
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack Query (React Query) for server state management
- **Forms**: React Hook Form with Zod validation for robust form handling

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript throughout the entire stack
- **API Design**: RESTful endpoints with structured error handling
- **Request Processing**: Express middleware for JSON parsing, logging, and error handling

### Data Storage Solutions
- **Database**: PostgreSQL configured with Drizzle ORM
- **Schema Management**: Drizzle Kit for migrations and schema evolution
- **Connection**: Neon Database serverless PostgreSQL for cloud deployment
- **Development Storage**: In-memory storage fallback for development/testing

## Key Components

### Frontend Components
1. **Landing Page Sections**:
   - Header with navigation and branding
   - Hero section with compelling CTAs
   - About section highlighting company experience
   - Services showcase (laptop repair, desktop repair, parts sales)
   - Why Choose Us section with key differentiators
   - Customer testimonials
   - Contact form with quote request functionality
   - Footer with contact information and social links

2. **UI Component Library**:
   - shadcn/ui components for consistent design system
   - Custom form components with validation
   - Responsive design patterns for mobile-first approach
   - Toast notifications for user feedback

### Backend Components
1. **API Endpoints**:
   - `POST /api/quotes` - Quote request submission
   - `GET /api/quotes` - Admin quote retrieval
   
2. **Data Models**:
   - Users table for potential admin functionality
   - Quotes table for customer service requests
   - Zod schemas for runtime validation

3. **Storage Layer**:
   - Abstract storage interface for flexibility
   - Memory storage implementation for development
   - Drizzle ORM integration for PostgreSQL

## Data Flow

1. **Quote Submission Flow**:
   - User fills out contact form on landing page
   - Form data validated client-side with Zod schema
   - API request sent to backend with validated data
   - Server validates data again and stores in database
   - Success/error response returned to client
   - Toast notification displayed to user

2. **Page Rendering Flow**:
   - Vite serves React application in development
   - Express serves static files in production
   - React components render landing page sections
   - Smooth scrolling navigation between sections

## External Dependencies

### Core Technologies
- **@neondatabase/serverless**: Serverless PostgreSQL connection
- **drizzle-orm**: Type-safe database operations
- **@tanstack/react-query**: Server state management
- **@radix-ui/***: Accessible UI primitives
- **tailwindcss**: Utility-first CSS framework

### Development Tools
- **vite**: Build tool and development server
- **typescript**: Static type checking
- **@replit/vite-plugin-runtime-error-modal**: Development error handling
- **@replit/vite-plugin-cartographer**: Replit-specific development features

### Form Handling
- **react-hook-form**: Performant form library
- **@hookform/resolvers**: Form validation resolvers
- **zod**: Schema validation library

## Deployment Strategy

### Development Environment
- Vite development server with hot module replacement
- Express server running concurrently for API endpoints
- Environment variable configuration for database connection
- TypeScript compilation and type checking

### Production Build
- Frontend: Vite builds optimized static assets
- Backend: esbuild bundles server code for Node.js
- Database: Drizzle migrations applied via `db:push` command
- Environment: Production environment variables required

### Key Build Commands
- `npm run dev`: Start development servers
- `npm run build`: Build for production
- `npm run start`: Start production server
- `npm run db:push`: Apply database schema changes

## Changelog
```
Changelog:
- June 30, 2025. Initial setup
```

## User Preferences
```
Preferred communication style: Simple, everyday language.
```
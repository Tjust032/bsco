# BSCO Monorepo

This is a Turborepo monorepo containing both frontend and backend applications.

## Project Structure

```
bsco/
├── apps/
│   ├── frontend/    # React Router v7 + Tailwind CSS
│   └── backend/     # Node.js + Express.js + TypeScript
├── packages/        # Shared packages (future use)
├── turbo.json      # Turborepo configuration
└── package.json    # Root workspace configuration
```

## Getting Started

### Install Dependencies

```bash
npm install
```

### Development

```bash
# Run both frontend and backend in development mode
npm run dev

# Or run individually:
npm run dev --filter=frontend
npm run dev --filter=backend
```

### Build

```bash
# Build all apps
npm run build

# Or build individually:
npm run build --filter=frontend
npm run build --filter=backend
```

### Start Production

```bash
# Start all apps in production mode
npm run start
```

## Apps

### Frontend (React Router v7)

- **Port:** 5173 (development)
- **Location:** `apps/frontend/`
- **Tech Stack:** React Router v7, TypeScript, Tailwind CSS, Vite

### Backend (Express.js)

- **Port:** 3001
- **Location:** `apps/backend/`
- **Tech Stack:** Node.js, Express.js, TypeScript, CORS, Helmet

## Available Scripts

- `npm run dev` - Start all apps in development mode
- `npm run build` - Build all apps for production
- `npm run start` - Start all apps in production mode
- `npm run typecheck` - Run TypeScript type checking for all apps

## Environment Variables

Backend environment variables (copy `apps/backend/env.example` to `apps/backend/.env`):

- `PORT` - Backend server port (default: 3001)
- `FRONTEND_URL` - Frontend URL for CORS (default: http://localhost:5173)
- `NODE_ENV` - Environment (development/production)

A modern, production-ready template for building full-stack React applications using React Router.

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/remix-run/react-router-templates/tree/main/default)

## Features

- 🚀 Server-side rendering
- ⚡️ Hot Module Replacement (HMR)
- 📦 Asset bundling and optimization
- 🔄 Data loading and mutations
- 🔒 TypeScript by default
- 🎉 TailwindCSS for styling
- 📖 [React Router docs](https://reactrouter.com/)

## Getting Started

### Installation

Install the dependencies:

```bash
npm install
```

### Development

Start the development server with HMR:

```bash
npm run dev
```

Your application will be available at `http://localhost:5173`.

## Building for Production

Create a production build:

```bash
npm run build
```

## Deployment

### Docker Deployment

To build and run using Docker:

```bash
docker build -t my-app .

# Run the container
docker run -p 3000:3000 my-app
```

The containerized application can be deployed to any platform that supports Docker, including:

- AWS ECS
- Google Cloud Run
- Azure Container Apps
- Digital Ocean App Platform
- Fly.io
- Railway

### DIY Deployment

If you're familiar with deploying Node applications, the built-in app server is production-ready.

Make sure to deploy the output of `npm run build`

```
├── package.json
├── package-lock.json (or pnpm-lock.yaml, or bun.lockb)
├── build/
│   ├── client/    # Static assets
│   └── server/    # Server-side code
```

## Styling

This template comes with [Tailwind CSS](https://tailwindcss.com/) already configured for a simple default starting experience. You can use whatever CSS framework you prefer.

---

Built with ❤️ using React Router.

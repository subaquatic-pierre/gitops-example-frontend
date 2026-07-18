# GitOps Example Frontend

This is a [Next.js](https://nextjs.org/) project bootstrapped with `create-next-app` and configured for GitOps deployments using Docker.

## Getting Started

First, install the dependencies:

```bash
npm install
```

Then, run the development server:

```bash
npm run dev
```

Open [http://localhost:4000](http://localhost:4000) with your browser to see the result.

## Docker Environments

This project includes Dockerfiles for different environments:

- `Dockerfile.dev` - Development environment
- `Dockerfile.staging` - Staging environment 
- `Dockerfile.prod` - Production environment

To build and run with Docker locally (example using prod):

```bash
docker build -t frontend-prod -f Dockerfile.prod .
docker run -p 4000:4000 frontend-prod
```

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build the application for production
- `npm run build:static` - Export a static build
- `npm run build:docker` - Build standalone application for Docker
- `npm run start` - Start production server
- `npm run lint` - Run ESLint

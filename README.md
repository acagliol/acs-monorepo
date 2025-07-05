# ACS (Automated Consultancy Services) Monorepo

A comprehensive monorepo containing the frontend and backend services for ACS, an automated consultancy platform built with modern web technologies.

## Project Structure

```
acs-monorepo/
├── acs-frontend/          # Next.js frontend application
├── acs-backend/           # Backend services and infrastructure
├── package.json           # Root package.json with workspace scripts
└── .gitmodules           # Git submodules configuration
```

## Quick Start

### Prerequisites

- **Node.js** >= 18.0.0
- **npm** >= 8.0.0
- **Git** with submodule support

### Installation

1. **Clone the monorepo with submodules:**
   ```bash
   git clone --recursive https://github.com/acagliol/acs-monorepo.git
   cd acs-monorepo
   ```

2. **If you already cloned without submodules:**
   ```bash
   git submodule update --init --recursive
   ```

3. **Install dependencies for all workspaces:**
   ```bash
   npm run install:all
   ```

### Development

#### Start all services:
```bash
npm run dev
```

#### Start individual services:
```bash
# Frontend only
npm run dev:frontend

# Backend only
npm run dev:backend
```

#### Build all services:
```bash
npm run build
```

#### Build individual services:
```bash
# Frontend only
npm run build:frontend

# Backend only
npm run build:backend
```

## Available Scripts

| Script | Description |
|--------|-------------|
| `dev` | Start both frontend and backend in development mode |
| `dev:frontend` | Start frontend development server |
| `dev:backend` | Start backend development server |
| `build` | Build all workspaces |
| `build:frontend` | Build frontend application |
| `build:backend` | Build backend services |
| `test` | Run tests across all workspaces |
| `lint` | Run linting across all workspaces |
| `clean` | Clean build artifacts from all workspaces |
| `install:all` | Install dependencies for all workspaces |

## Repository Links

### Frontend Repository
- **GitHub**: https://github.com/acagliol/acs-frontend.git
- **Technology Stack**: Next.js 15, React 18, TypeScript, Tailwind CSS
- **Features**: Modern UI/UX, authentication, dashboard, analytics

### Backend Repository
- **GitHub**: https://github.com/acagliol/acs-backend.git
- **Technology Stack**: AWS services, Terraform, serverless architecture
- **Features**: API services, infrastructure as code, cloud deployment

## Development Workflow

### Working with Submodules

1. **Update submodules to latest:**
   ```bash
   git submodule update --remote
   ```

2. **Make changes in submodules:**
   ```bash
   cd acs-frontend
   # Make your changes
   git add .
   git commit -m "Your changes"
   git push origin main
   ```

3. **Update main repo to use new submodule versions:**
   ```bash
   cd ..
   git add acs-frontend acs-backend
   git commit -m "Update submodules"
   git push origin main
   ```

### Environment Setup

1. **Frontend Environment:**
   - Copy `.env.example` to `.env.local` in `acs-frontend/`
   - Configure authentication, API endpoints, and other environment variables

2. **Backend Environment:**
   - Configure AWS credentials and Terraform variables
   - Set up environment-specific configurations

## Architecture Overview

### Frontend (acs-frontend/)
- **Framework**: Next.js 15 with App Router
- **UI Library**: Custom components with Tailwind CSS
- **Authentication**: NextAuth.js with multiple providers
- **State Management**: React hooks and context
- **Styling**: Tailwind CSS with custom theme system

### Backend (acs-backend/)
- **Infrastructure**: AWS services managed with Terraform
- **API**: Serverless functions and API Gateway
- **Database**: AWS DynamoDB and other managed services
- **Authentication**: AWS Cognito integration
- **Deployment**: CI/CD with GitHub Actions

## Contributing

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/amazing-feature`
3. **Make your changes** in the appropriate submodule
4. **Commit your changes**: `git commit -m 'Add amazing feature'`
5. **Push to the branch**: `git push origin feature/amazing-feature`
6. **Open a Pull Request**

## Requirements

### System Requirements
- **Node.js**: >= 18.0.0
- **npm**: >= 8.0.0
- **Git**: Latest version with submodule support
- **Memory**: 8GB RAM recommended
- **Storage**: 2GB free space

### Development Tools
- **VS Code** (recommended)
- **Git** for version control
- **Docker** (optional, for containerized development)

## Troubleshooting

### Common Issues

1. **Submodules not initialized:**
   ```bash
   git submodule update --init --recursive
   ```

2. **Dependencies not installed:**
   ```bash
   npm run install:all
   ```

3. **Port conflicts:**
   - Frontend runs on port 3000
   - Backend runs on port 8000
   - Ensure these ports are available

4. **Build errors:**
   ```bash
   npm run clean
   npm run install:all
   npm run build
   ```

## License

This project is proprietary software. All rights reserved.

## Support

For support and questions:
- **Issues**: Create an issue in the respective repository
- **Documentation**: Check individual README files in each submodule
- **Team**: Contact the development team

---

**Note**: This is a monorepo using Git submodules. Always ensure you're working with the latest submodule versions and follow the proper workflow for making changes. 
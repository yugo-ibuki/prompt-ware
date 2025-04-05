# Directory Structure

## Frontend (Next.js)
```
frontend/
├── .next/               # Next.js build output
├── public/             # Static files
│   ├── images/
│   └── fonts/
├── src/
│   ├── app/           # App Router pages
│   ├── components/    # React components
│   │   ├── atoms/
│   │   ├── molecules/
│   │   ├── organisms/
│   │   ├── templates/
│   │   └── pages/
│   ├── hooks/         # Custom React hooks
│   ├── stores/        # Zustand stores
│   ├── types/         # TypeScript type definitions
│   ├── utils/         # Utility functions
│   ├── styles/        # Global styles
│   ├── api/           # API client and types
│   └── constants/     # Constants and configurations
├── tests/
│   ├── unit/
│   ├── integration/
│   └── e2e/
└── .storybook/        # Storybook configuration
```

## Backend (Go)
```
backend/
├── cmd/
│   └── api/          # Application entry points
├── internal/
│   ├── api/         # API handlers
│   ├── middleware/  # HTTP middleware
│   ├── models/      # Database models
│   ├── repository/  # Data access layer
│   ├── service/     # Business logic
│   └── utils/       # Utility functions
├── pkg/             # Public packages
│   ├── logger/
│   ├── config/
│   └── errors/
├── migrations/      # Database migrations
├── scripts/        # Build and deployment scripts
└── tests/
    ├── unit/
    └── integration/
```

## Project Root
```
.
├── .github/         # GitHub Actions and templates
├── .vscode/        # VS Code settings
├── docs/           # Project documentation
├── frontend/       # Frontend application
├── backend/        # Backend application
├── docker/         # Docker configurations
├── tools/          # Development tools
└── scripts/        # Project-wide scripts
```

## Important Notes

1. All new components should follow the Atomic Design pattern in the frontend structure
2. Keep business logic separate from API handlers in the backend
3. Shared types should be in the `types` directory
4. Environment-specific configurations should be in the `config` directory
5. All tests should be co-located with their respective code
6. Documentation should be maintained alongside code changes

Note: This structure serves as a template and may be adjusted based on project requirements with approval. 
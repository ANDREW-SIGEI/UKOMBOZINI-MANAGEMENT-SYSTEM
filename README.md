# UKOMBOZINI Table Banking Management System (TBMS)

A comprehensive digital solution for managing table banking operations, built with Django REST Framework (backend) and React TypeScript (frontend).

## Repository
**GitHub:** git@github.com:ANDREW-SIGEI/UKOMBOZINI-MANAGEMENT-SYSTEM.git

## Overview
This system streamlines table banking activities by providing role-based access for Administrators, Field Officers, and Members. Key features include loan management with mandatory ID verification, financial tracking via Cash In/Out/TRF tables, meeting scheduling, and annual dividend calculations.

## Key Features

### User Roles
- **Administrator:** System oversight, officer management, global financial monitoring
- **Field Officer:** Group assignments, data entry, meeting management, calendar updates
- **Member:** Personal dashboard, loan applications, attendance tracking

### Core Functionality
- Group and member registration with location hierarchy
- Loan processing (short-term, long-term, project) with ID verification
- Financial tables: Cash In (10+ categories), Cash Out (7+ categories), TRF Balance
- Interactive calendar for meetings and scheduling
- Annual dividend calculations
- Officer activity tracking and GPS monitoring
- Offline capabilities (PWA)

### Security & Compliance
- Mandatory ID verification for loan approvals
- Digital signatures for agreements
- Role-based permissions
- Encrypted data storage
- Audit logging

## Technology Stack

### Backend
- **Framework:** Django 4.x + Django REST Framework
- **Database:** PostgreSQL
- **Authentication:** JWT with refresh tokens
- **Deployment:** Docker, Gunicorn, Nginx

### Frontend
- **Framework:** React 18 + TypeScript
- **State Management:** Redux Toolkit
- **UI Library:** Material-UI (MUI)
- **Build Tool:** Vite
- **Deployment:** Docker, Nginx

### DevOps
- **Containerization:** Docker & Docker Compose
- **Version Control:** Git
- **CI/CD:** GitHub Actions
- **Monitoring:** Sentry, Prometheus

## Project Structure
```
UKOMBOZINI-MANAGEMENT-SYSTEM/
├── backend/                          # Django Backend
│   ├── core/                         # Main Django project
│   ├── ukombozini/                   # Main app
│   │   └── apps/                     # Feature-specific apps
│   │       ├── authentication/       # User auth & roles
│   │       ├── groups/               # Group & member management
│   │       ├── loans/                # Loan models & logic
│   │       ├── transactions/         # Cash in/out, TRF
│   │       ├── meetings/             # Calendar & attendance
│   │       ├── reports/              # Financial reports & dividends
│   │       └── officers/             # Officer tracking
│   ├── requirements.txt
│   ├── manage.py
│   └── Dockerfile
├── frontend/                         # React Frontend
│   ├── public/
│   ├── src/
│   │   ├── components/               # Reusable UI components
│   │   │   ├── auth/                 # Login/Register
│   │   │   ├── dashboard/            # Dashboards per role
│   │   │   ├── forms/                # Loan, Member, Group forms
│   │   │   ├── tables/               # Cash In/Out, TRF tables
│   │   │   └── verification/         # ID upload, Camera, Signature
│   │   ├── pages/                    # Route pages
│   │   ├── hooks/                    # Custom React hooks
│   │   ├── utils/                    # API, validation
│   │   └── types/                    # TypeScript types
│   ├── package.json
│   ├── tsconfig.json
│   └── Dockerfile
├── docs/                             # Documentation
├── tests/                            # Test suites
├── docker-compose.yml                # Full stack orchestration
├── .gitignore
└── README.md
```

## Quick Start

### Prerequisites
- Docker & Docker Compose
- Git

### Installation
1. Clone the repository:
   ```bash
   git clone git@github.com:ANDREW-SIGEI/UKOMBOZINI-MANAGEMENT-SYSTEM.git
   cd UKOMBOZINI-MANAGEMENT-SYSTEM
   ```

2. Start the development environment:
   ```bash
   docker-compose up -d
   ```

3. Access the application:
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:8000
   - Admin Panel: http://localhost:8000/admin

### Development Setup
1. Backend setup:
   ```bash
   cd backend
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   python manage.py migrate
   python manage.py createsuperuser
   python manage.py runserver
   ```

2. Frontend setup:
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

## API Documentation
- Swagger UI: http://localhost:8000/swagger/
- ReDoc: http://localhost:8000/redoc/

## Testing
```bash
# Backend tests
cd backend
python manage.py test

# Frontend tests
cd frontend
npm test
```

## Deployment
See [Deployment Guide](docs/Deployment-Guide.md) for production setup instructions.

## Contributing
1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit changes: `git commit -am 'Add your feature'`
4. Push to branch: `git push origin feature/your-feature`
5. Submit a pull request

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support
For support and questions:
- Email: support@ukombozini.com
- Documentation: [User Manual](docs/User-Manual.md)

## Roadmap
- Phase 1: Foundation & Authentication (Complete)
- Phase 2: Core Models & APIs (In Progress)
- Phase 3-12: See [TODO.md](TODO.md) for detailed implementation phases

---
**Built with ❤️ for table banking communities**

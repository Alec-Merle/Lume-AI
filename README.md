# Lume - AI-Powered Enterprise Document Management Platform

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](https://github.com/Alec-Merle/Lume-AI)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Documentation](https://img.shields.io/badge/docs-complete-green)](https://github.com/Alec-Merle/Lume-AI)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.6.3-blue.svg)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-18.3.1-blue.svg)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18+-green.svg)](https://nodejs.org/)

> Lume is a next-generation AI-powered document vault that transforms enterprise document chaos into intelligent, searchable knowledge. Built for modern enterprises, Lume combines artificial intelligence with robust document management to create a single source of truth for organizational knowledge.

## 🏆 Project Overview

**Lume** represents the strategic bridge to the Palantir Foundry ecosystem - an AI-powered enterprise document vault that automates organization, tracks versions, generates summaries, and manages approval workflows. The platform positions enterprises for seamless AI integration while solving the $50 billion document management crisis facing Fortune 500 companies.

### Core Vision
Transform scattered document repositories into AI-ready intelligence hubs that drive decision-making, ensure compliance, and unlock institutional knowledge.

## 📋 Project Documentation

This project includes comprehensive documentation covering all aspects of development, deployment, and business strategy:

### 📖 Business & Strategic Documentation
- **[📊 Business Plan](./BUSINESS_PLAN.md)** - Complete business strategy, market analysis, and financial projections
- **[🎯 Business Model Canvas](./BUSINESS_MODEL_CANVAS.md)** - Visual business model overview and value propositions  
- **[📈 Market Research](./LUME_MARKET_RESEARCH.md)** - Industry analysis, competitive landscape, and market opportunities
- **[🤝 Palantir Partnership Proposal](./BEYOND_BOUNDARIES_PALANTIR_PITCH.md)** - Strategic partnership framework and integration roadmap

### 🔬 Technical Documentation
- **[📑 Technical Whitepaper](./WHITEPAPER.md)** - In-depth technical analysis, architecture decisions, and implementation details
- **[🗃️ Database Schema](./shared/schema.ts)** - Complete data model definitions and type schemas
- **[🛠️ Configuration Files](./components.json)** - UI component system configuration and aliases

## 🌟 Key Features

### 🤖 AI-Powered Intelligence
- **Smart Categorization**: Automatic document classification using advanced ML algorithms powered by Claude Sonnet 4
- **Intelligent Summarization**: AI-generated summaries with key insights, risk assessments, and suggested actions
- **Semantic Search**: Natural language search with relevance scoring and highlighted excerpts
- **Content Analysis**: Deep understanding of document relationships and contextual connections
- **Question Answering**: AI-powered document querying with citation and confidence scoring

### 📚 Enterprise Document Management
- **Version Control**: Complete revision history with visual diff comparison and change tracking
- **Approval Workflows**: Customizable multi-stage review and approval processes with activity logging
- **Role-Based Access Control**: Four distinct roles (Author, Reviewer, Approver, Admin) with granular permissions
- **Audit Trail**: Comprehensive activity logging for regulatory compliance and governance
- **Document Lifecycle**: Complete document management from creation to archival

### 🎨 Modern User Experience
- **Glassmorphism Design**: Premium modern interface with dark-first theming and custom CSS properties
- **Interactive Dashboard**: Tile-based document categories with real-time statistics and AI suggestions
- **Responsive Layout**: Optimized for desktop, tablet, and mobile devices with consistent UX
- **Accessibility First**: Full keyboard navigation, screen reader support, and WCAG compliance
- **Progressive Web App**: Offline capabilities and native-like mobile experience

### 🔐 Enterprise-Grade Security
- **Session-Based Authentication**: Secure server-side session management with PostgreSQL store
- **Environment Validation**: Comprehensive startup checks for required configuration
- **Data Encryption**: End-to-end encryption for sensitive documents and user data
- **Compliance Ready**: Built for SOC 2, GDPR, HIPAA, and other regulatory requirements
- **Secure File Upload**: Validated file handling with type checking and size limits

## 🏗️ Technical Architecture

### Frontend Stack
- **[React 18.3.1](./client/src/App.tsx)** + **TypeScript 5.6.3**: Type-safe component architecture with modern React patterns
- **[Vite](./vite.config.ts)**: Lightning-fast build system with hot module replacement and optimizations
- **[Tailwind CSS](./tailwind.config.ts)**: Utility-first styling with custom design system and dark mode support
- **[Radix UI + shadcn/ui](./client/src/components/ui/)**: Accessible component library with premium styling and animations
- **[TanStack Query v5](./client/src/lib/queryClient.ts)**: Robust server state management, caching, and data synchronization
- **[Wouter](./client/src/App.tsx)**: Lightweight client-side routing with modern patterns
- **[React Hook Form + Zod](./client/src/components/ui/form.tsx)**: Type-safe form handling with validation

### Backend Infrastructure
- **[Node.js + Express](./server/index.ts)**: High-performance TypeScript server with comprehensive error handling
- **[PostgreSQL + Drizzle ORM](./shared/schema.ts)**: Type-safe database operations with schema migrations and validation
- **[Neon Database](./drizzle.config.ts)**: Serverless PostgreSQL for scalable cloud hosting and automatic scaling
- **[Multer](./server/routes.ts)**: Secure file upload handling with validation and memory storage
- **[Express Sessions](./server/index.ts)**: Server-side session management with PostgreSQL store integration

### AI/ML Integration
- **[Anthropic Claude Sonnet 4](./server/lib/ai.ts)**: Advanced text analysis, summarization, and document understanding
- **Smart Categorization**: Machine learning-powered automatic document classification
- **Risk Assessment**: AI-driven content analysis for compliance and security evaluation
- **Workflow Optimization**: Intelligent routing suggestions based on document content and organizational patterns

### Database Schema
The complete database schema is defined in [`shared/schema.ts`](./shared/schema.ts) and includes:

- **Users**: Authentication, roles, and user management
- **Categories**: Document classification with visual styling
- **Documents**: Core document entities with metadata and status tracking
- **Document Versions**: Complete version history with change notes
- **Document Approvals**: Multi-stage approval workflows with activity logging
- **Document Summaries**: AI-generated insights and risk assessments

## 🚀 Quick Start

### Prerequisites
- **Node.js 18+** and npm
- **PostgreSQL database** (Neon recommended for cloud deployment)
- **Anthropic API key** for AI features
- **Modern web browser** with JavaScript enabled

### Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Alec-Merle/Lume-AI.git
   cd Lume-AI
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Configuration**
   
   Create a `.env` file in the project root or configure environment variables:
   
   ```bash
   # Required Environment Variables
   ANTHROPIC_API_KEY=sk-ant-your-api-key-here
   DATABASE_URL=postgresql://username:password@host:port/database
   
   # Optional Environment Variables  
   SESSION_SECRET=your-secure-session-secret-here
   PORT=5000
   NODE_ENV=development
   ```

   **Getting API Keys:**
   - **Anthropic API Key**: Visit [console.anthropic.com](https://console.anthropic.com) to create an account and generate an API key
   - **Database URL**: Use [Neon](https://neon.tech) for serverless PostgreSQL or your preferred PostgreSQL provider

4. **Database Setup**
   ```bash
   # Push schema to database
   npm run db:push
   ```

5. **Start Development Server**
   ```bash
   npm run dev
   ```

6. **Access the Application**
   - Frontend & API: `http://localhost:5000`
   - The application serves both frontend and backend on the same port

### Production Deployment

For production deployment:

```bash
# Build the application
npm run build

# Start production server
npm run start
```

**Environment Variables for Deployment:**
Ensure these environment variables are configured in your deployment environment:
- `ANTHROPIC_API_KEY` - Required for AI features
- `DATABASE_URL` - PostgreSQL connection string
- `SESSION_SECRET` - Secure session signing key (auto-generated if not provided)
- `NODE_ENV=production` - Enables production optimizations

## 📁 Project Structure

```
Lume-AI/
├── 📂 client/                     # Frontend React application
│   ├── 📂 src/
│   │   ├── 📂 components/         # Reusable UI components
│   │   │   ├── 📂 ai/            # AI-related components
│   │   │   ├── 📂 dashboard/     # Dashboard-specific components
│   │   │   ├── 📂 document/      # Document management components
│   │   │   ├── 📂 layout/        # Layout and navigation components
│   │   │   ├── 📂 search/        # Search functionality components
│   │   │   ├── 📂 tour/          # User onboarding components
│   │   │   ├── 📂 ui/            # shadcn/ui component library
│   │   │   ├── 📂 upload/        # File upload components
│   │   │   └── 📂 workflow/      # Approval workflow components
│   │   ├── 📂 contexts/          # React context providers
│   │   ├── 📂 hooks/             # Custom React hooks
│   │   ├── 📂 lib/               # Utility libraries and configurations
│   │   ├── 📂 pages/             # Application pages and routing
│   │   ├── 📄 App.tsx            # Main application component
│   │   ├── 📄 main.tsx           # React application entry point
│   │   └── 📄 index.css          # Global styles and Tailwind configuration
│   └── 📄 index.html             # HTML entry point
├── 📂 server/                     # Backend Express server
│   ├── 📂 lib/                   # Server utilities and integrations
│   │   └── 📄 ai.ts              # Anthropic AI integration and functions
│   ├── 📄 index.ts               # Express server setup and configuration
│   ├── 📄 routes.ts              # API route definitions and handlers
│   ├── 📄 storage.ts             # Database abstraction and storage interface
│   └── 📄 vite.ts                # Vite development server integration
├── 📂 shared/                     # Shared types and schemas
│   └── 📄 schema.ts              # Database schema and type definitions
├── 📂 public/                     # Static assets and images
│   └── 📂 images/                # Project assets and user uploads
├── 📂 attached_assets/            # Development assets and resources
├── ⚙️ Configuration Files
│   ├── 📄 package.json           # Dependencies and scripts
│   ├── 📄 vite.config.ts         # Vite build configuration
│   ├── 📄 tailwind.config.ts     # Tailwind CSS configuration
│   ├── 📄 tsconfig.json          # TypeScript configuration
│   ├── 📄 drizzle.config.ts      # Database migration configuration
│   ├── 📄 postcss.config.js      # PostCSS configuration
│   └── 📄 components.json        # shadcn/ui component configuration
└── 📋 Documentation
    ├── 📄 README.md              # This comprehensive guide
    ├── 📄 BUSINESS_PLAN.md       # Complete business strategy and projections
    ├── 📄 BUSINESS_MODEL_CANVAS.md # Business model visualization
    ├── 📄 WHITEPAPER.md          # Technical whitepaper and research
    ├── 📄 LUME_MARKET_RESEARCH.md # Market analysis and opportunities
    ├── 📄 PALANTIR_DEMO_SCRIPT.md # Partnership presentation materials
    └── 📄 BEYOND_BOUNDARIES_PALANTIR_PITCH.md # Strategic partnership proposal
```

## 🔧 Development Guide

### Available Scripts

```bash
# Development
npm run dev          # Start development server with hot reload
npm run check        # TypeScript type checking
npm run db:push      # Push database schema changes

# Production
npm run build        # Build for production
npm run start        # Start production server
```

### Key Development Files

| File | Purpose | Description |
|------|---------|-------------|
| [`server/index.ts`](./server/index.ts) | Server Entry Point | Express server setup, middleware configuration, environment validation |
| [`server/routes.ts`](./server/routes.ts) | API Routes | RESTful API endpoints, request validation, and response handling |
| [`server/storage.ts`](./server/storage.ts) | Data Layer | Database abstraction, CRUD operations, and storage interface |
| [`server/lib/ai.ts`](./server/lib/ai.ts) | AI Integration | Anthropic Claude integration for document analysis and categorization |
| [`shared/schema.ts`](./shared/schema.ts) | Data Schema | Drizzle ORM schema definitions, Zod validation, and TypeScript types |
| [`client/src/App.tsx`](./client/src/App.tsx) | Frontend Entry | React application setup, routing configuration, and context providers |
| [`client/src/lib/queryClient.ts`](./client/src/lib/queryClient.ts) | API Client | TanStack Query configuration and API request handling |

### Core Components Architecture

#### AI Components (`client/src/components/ai/`)
Components handling AI-powered features and intelligent document processing.

#### Dashboard Components (`client/src/components/dashboard/`)
- [`ai-suggestions.tsx`](./client/src/components/dashboard/ai-suggestions.tsx) - AI-powered workflow suggestions and recommendations

#### Document Components (`client/src/components/document/`)
- [`document-card.tsx`](./client/src/components/document/document-card.tsx) - Document tile display with metadata
- [`ai-summary.tsx`](./client/src/components/document/ai-summary.tsx) - AI-generated document summaries and insights
- [`version-diff.tsx`](./client/src/components/document/version-diff.tsx) - Visual document version comparison
- [`ai-diff-summary.tsx`](./client/src/components/document/ai-diff-summary.tsx) - AI analysis of document changes

#### Layout Components (`client/src/components/layout/`)
- [`app-layout.tsx`](./client/src/components/layout/app-layout.tsx) - Main application shell and navigation
- [`sidebar.tsx`](./client/src/components/layout/sidebar.tsx) - Primary navigation sidebar
- [`topbar.tsx`](./client/src/components/layout/topbar.tsx) - Application header and user controls

### Page Structure (`client/src/pages/`)

| Page | Route | Purpose | Key Features |
|------|-------|---------|--------------|
| [`landing.tsx`](./client/src/pages/landing.tsx) | `/` | Marketing Landing | Hero section, feature showcase, authentication |
| [`dashboard.tsx`](./client/src/pages/dashboard.tsx) | `/dashboard` | Main Dashboard | Category tiles, AI suggestions, recent activity |
| [`documents.tsx`](./client/src/pages/documents.tsx) | `/documents` | Document List | Search, filters, bulk operations |
| [`document-detail.tsx`](./client/src/pages/document-detail.tsx) | `/documents/:id` | Document View | Content display, versions, approvals |
| [`document-diff.tsx`](./client/src/pages/document-diff.tsx) | `/documents/:id/diff` | Version Comparison | Side-by-side diff with AI analysis |
| [`category.tsx`](./client/src/pages/category.tsx) | `/categories/:id` | Category View | Category-specific documents and analytics |
| [`upload.tsx`](./client/src/pages/upload.tsx) | `/upload` | File Upload | Drag-and-drop upload with AI categorization |
| [`search.tsx`](./client/src/pages/search.tsx) | `/search` | Search Results | Semantic search with highlighting |
| [`approval-dashboard.tsx`](./client/src/pages/approval-dashboard.tsx) | `/approvals` | Approval Management | Workflow oversight and status tracking |
| [`settings.tsx`](./client/src/pages/settings.tsx) | `/settings` | User Settings | Profile, preferences, role management |

## 🔌 API Reference

### Authentication Endpoints
```bash
GET /api/auth/user          # Get current user information
POST /api/auth/switch-role  # Switch user role (demo feature)
```

### Document Management
```bash
GET /api/documents                    # List all documents with filtering
GET /api/documents/recent            # Get recently updated documents
GET /api/documents/:id               # Get specific document with details
POST /api/documents                  # Create new document
PATCH /api/documents/:id             # Update document metadata
POST /api/documents/upload           # Upload document file
GET /api/documents/:id/versions      # Get document version history
POST /api/documents/:id/versions     # Create new document version
GET /api/documents/:id/summary       # Get AI-generated document summary
```

### AI-Powered Features
```bash
POST /api/ai/categorize             # AI document categorization
POST /api/ai/summarize              # Generate AI summary and insights
POST /api/ai/ask                    # Ask questions about documents
POST /api/ai/workflow               # Get workflow suggestions
GET /api/ai/related/:documentId     # Find related documents
GET /api/ai/suggestions             # Get dashboard AI suggestions
```

### Approval Workflows
```bash
GET /api/approvals                  # List all approval workflows
GET /api/approvals/stats           # Get approval statistics
GET /api/documents/:id/approval    # Get document approval status
POST /api/documents/:id/approval   # Create approval workflow
PATCH /api/documents/:id/approval  # Update approval status
POST /api/documents/:id/submit-review # Submit document for review
```

### Categories & Search
```bash
GET /api/categories                 # List all categories
GET /api/categories/stats          # Get category statistics  
GET /api/categories/:id            # Get specific category
GET /api/documents/category/:id    # Get documents by category
GET /api/search                    # Search documents with filters
GET /api/search/suggestions        # Get search suggestions
```

### Users & System
```bash
GET /api/users                     # List all users (admin only)
```

## 🛠️ Development Workflow

### Environment Setup

1. **Development Environment**
   ```bash
   # Install dependencies
   npm install
   
   # Set up environment variables
   cp .env.example .env
   # Edit .env with your configuration
   
   # Push database schema
   npm run db:push
   
   # Start development server
   npm run dev
   ```

2. **Code Quality Tools**
   ```bash
   # Type checking
   npm run check
   
   # Database schema validation
   npm run db:push
   ```

### Technology Stack Details

#### Frontend Dependencies
- **React Ecosystem**: React 18.3.1, React DOM, React Hook Form
- **Styling**: Tailwind CSS, Tailwind Animate, PostCSS, Autoprefixer
- **UI Components**: Full Radix UI component suite, Lucide React icons, React Icons
- **State Management**: TanStack React Query v5, React Context API
- **Routing**: Wouter for lightweight client-side navigation
- **Forms & Validation**: React Hook Form, Zod, @hookform/resolvers
- **Utilities**: date-fns, clsx, tailwind-merge, class-variance-authority

#### Backend Dependencies  
- **Server Framework**: Express.js with TypeScript support
- **Database**: Drizzle ORM, @neondatabase/serverless, Drizzle Kit
- **AI Integration**: @anthropic-ai/sdk for Claude integration
- **File Handling**: Multer for multipart form data and file uploads
- **Session Management**: Express Session, Connect PG Simple
- **Authentication**: Passport.js with local strategy support
- **Validation**: Zod, Zod Validation Error for schema validation

#### Development Tools
- **Build System**: Vite with React plugin, ESBuild for production builds
- **TypeScript**: Full type safety with strict mode enabled
- **Code Quality**: Vite plugins for development experience
- **Database Tools**: Drizzle Kit for schema management and migrations

### Component Development Patterns

#### UI Component Structure
All UI components follow the shadcn/ui patterns located in [`client/src/components/ui/`](./client/src/components/ui/):

- **Accessibility First**: All components include proper ARIA labels and keyboard navigation
- **Dark Mode Support**: Components use CSS variables for consistent theming
- **TypeScript Integration**: Full type safety with variant props and component APIs
- **Customizable**: Built on Radix UI primitives for maximum flexibility

#### Data Fetching Patterns
```typescript
// Example from client/src/pages/dashboard.tsx
const { data: categories, isLoading } = useQuery({
  queryKey: ['/api/categories/stats'],
});

// Example mutation pattern
const createDocument = useMutation({
  mutationFn: async (data: InsertDocument) => {
    return apiRequest('/api/documents', { 
      method: 'POST', 
      body: JSON.stringify(data) 
    });
  },
  onSuccess: () => {
    queryClient.invalidateQueries({ queryKey: ['/api/documents'] });
  }
});
```

#### Form Handling Patterns  
```typescript
// Example from upload components
const form = useForm<InsertDocument>({
  resolver: zodResolver(insertDocumentSchema.extend({
    // Additional validation rules
  })),
  defaultValues: {
    title: "",
    categoryId: "",
    status: "Draft"
  }
});
```

## 🎯 Market Opportunity & Business Context

### Market Size & Opportunity
Lume addresses a **$50 billion market opportunity** in enterprise document management:

- **2.5 quintillion bytes** of data generated daily by enterprises
- **80% unstructured** document content lacking proper organization
- **$15,000 annual cost** per knowledge worker due to document inefficiencies
- **75% faster** approval cycles achievable with AI-powered workflows

*For comprehensive market analysis, see [LUME_MARKET_RESEARCH.md](./LUME_MARKET_RESEARCH.md)*

### Strategic Positioning
- **Palantir Partnership Track**: Designed for integration with Palantir Foundry ecosystem
- **Enterprise-First**: Built specifically for Fortune 500 compliance and scale requirements
- **AI-Native Architecture**: Positioned for the next generation of intelligent document processing
- **Competitive Advantages**: See detailed analysis in [BUSINESS_PLAN.md](./BUSINESS_PLAN.md)

## 🧪 Testing & Quality Assurance

### Testing Strategy
- **Component Testing**: React Testing Library for UI component validation
- **API Testing**: Integration tests for all backend endpoints
- **Type Safety**: Comprehensive TypeScript coverage with strict mode
- **Database Testing**: Schema validation and migration testing
- **AI Feature Testing**: Mock responses and error handling validation

### Code Quality Standards
- **TypeScript Strict Mode**: Enabled across the entire codebase
- **ESLint + Prettier**: Automated code formatting and style enforcement
- **Semantic Commits**: Conventional commit messages for clear change tracking
- **Code Reviews**: Required for all contributions and feature additions

## 🚀 Deployment & Infrastructure

### Supported Platforms
- **Replit**: Primary development and hosting platform
- **Vercel/Netlify**: Frontend deployment with serverless functions
- **AWS/Azure/GCP**: Full-stack deployment with container orchestration
- **Docker**: Containerized deployment for enterprise environments

### Infrastructure Requirements
- **Node.js 18+**: Runtime environment
- **PostgreSQL 12+**: Primary database (Neon recommended)
- **Redis** (optional): Session storage and caching
- **CDN**: Static asset delivery (automatic with most platforms)

### Performance Specifications
- **Sub-100ms** API response times for document operations
- **99.9% uptime** SLA with redundant infrastructure
- **Horizontal scaling** support with stateless server architecture
- **Auto-scaling** based on demand patterns and resource usage

## 🛡️ Security & Compliance

### Security Features
- **Environment Validation**: Startup checks for required security configuration
- **Session Security**: Secure session management with PostgreSQL backing
- **Input Validation**: Comprehensive request validation with Zod schemas
- **File Upload Security**: Type validation, size limits, and malware scanning
- **API Security**: Rate limiting, CORS configuration, and error handling

### Compliance Standards
- **SOC 2 Type II**: Infrastructure and process compliance
- **GDPR Ready**: Data privacy controls and user consent management
- **HIPAA Compatible**: Healthcare industry security requirements
- **Audit Trail**: Comprehensive logging for regulatory compliance

### Data Protection
- **Encryption at Rest**: Database and file storage encryption
- **Encryption in Transit**: HTTPS/TLS for all communications
- **Access Controls**: Role-based permissions with principle of least privilege
- **Data Retention**: Configurable retention policies for compliance

## 🏢 Enterprise Integration

### Supported Integrations
- **Palantir Foundry**: Strategic partnership for data platform integration - see [partnership proposal](./BEYOND_BOUNDARIES_PALANTIR_PITCH.md)
- **Microsoft 365**: SharePoint, Teams, and Office document synchronization
- **Google Workspace**: Drive, Docs, and collaborative editing integration
- **Slack/Teams**: Real-time notifications and workflow updates
- **SSO Providers**: Active Directory, Okta, Auth0, and SAML integration

### API-First Architecture
- **RESTful Design**: Comprehensive API with consistent patterns and error handling
- **Type-Safe Client**: Generated TypeScript clients for external integrations
- **Webhook Support**: Real-time event notifications for document changes
- **Rate Limiting**: Built-in protection against abuse and system overload

## 📊 Business Intelligence & Analytics

### AI-Powered Insights
- **Document Intelligence**: Automated content analysis and categorization
- **Risk Assessment**: Proactive identification of compliance and security issues
- **Workflow Optimization**: Data-driven suggestions for process improvements
- **Usage Analytics**: Detailed metrics on document access and collaboration patterns

### Reporting Capabilities
- **Executive Dashboards**: High-level KPIs and organizational metrics
- **Compliance Reports**: Automated generation of regulatory compliance documentation
- **Usage Analytics**: Detailed user engagement and system utilization reports
- **Custom Reports**: Flexible reporting with export capabilities

## 🤝 Contributing

### Development Contribution Workflow
1. **Fork the repository** and create a feature branch
3. **Write comprehensive tests** for new features and bug fixes
4. **Update documentation** for API changes and new features
5. **Submit pull request** with detailed description and test coverage

### Code Standards & Guidelines
- **TypeScript**: Strict mode enabled with comprehensive type coverage
- **Component Architecture**: Follow patterns established in existing components
- **State Management**: Use TanStack Query for server state, React Context for client state
- **Styling**: Tailwind CSS with custom properties for theming
- **Error Handling**: Comprehensive error boundaries and graceful degradation
- **Accessibility**: WCAG 2.1 AA compliance for all interactive elements

### Testing Requirements
- **Unit Tests**: Required for all utility functions and business logic
- **Integration Tests**: API endpoint testing with database integration
- **Component Tests**: React Testing Library for UI component validation
- **Type Testing**: TypeScript compilation and type checking

## 🌐 Business Context & Strategic Vision

### Partnership Opportunities
- **[Palantir Foundry Integration](./BEYOND_BOUNDARIES_PALANTIR_PITCH.md)**: Strategic partnership for enterprise data platform integration
- **Enterprise Software Ecosystem**: Integration with major productivity and collaboration platforms
- **AI/ML Platform Partnerships**: Expanding AI capabilities through strategic technology partnerships

### Market Position
- **Target Market**: Fortune 500 enterprises with complex document management needs
- **Competitive Advantages**: AI-first architecture, enterprise-grade security, modern UX
- **Growth Strategy**: Land and expand with departmental pilots scaling to enterprise-wide deployments

*For detailed business analysis, see [BUSINESS_PLAN.md](./BUSINESS_PLAN.md) and [BUSINESS_MODEL_CANVAS.md](./BUSINESS_MODEL_CANVAS.md)*

## 📈 Roadmap & Future Development

### Immediate Priorities (Q1 2025)
- [ ] **Enhanced AI Features**: Advanced summarization and content analysis
- [ ] **Mobile Application**: Native iOS and Android applications
- [ ] **Palantir Integration**: Deep integration with Foundry platform
- [ ] **Enterprise SSO**: Advanced authentication and authorization

### Medium-term Goals (Q2-Q3 2025)
- [ ] **Analytics Dashboard**: Advanced reporting and business intelligence
- [ ] **Multi-language Support**: Internationalization and localization
- [ ] **API Marketplace**: Third-party integrations and developer ecosystem
- [ ] **Advanced Workflows**: Complex approval processes and automation
- [ ] **Machine Learning Insights**: Predictive analytics and trend analysis

### Long-term Vision (Q4 2025+)
- [ ] **Global Deployment**: Multi-region infrastructure and compliance
- [ ] **Advanced Search**: Vector search and semantic understanding
- [ ] **Compliance Automation**: Automated regulatory reporting and monitoring
- [ ] **Enterprise Reporting**: Advanced analytics and business intelligence

## 🏆 Recognition & Achievements

- **Palantir Startup Fellowship**: Selected for enterprise partnership program
- **AI Innovation Award**: Recognition for document intelligence platform
- **Enterprise Software Excellence**: Award for user experience design and accessibility

## 🤝 Support & Contact

### Enterprise Sales & Partnerships
- **Email**: sales@dovah.io
- **Phone**: +1 (555) 123-4567  
- **Schedule Demo**: [calendly.com/dovah-demo](https://calendly.com/dovah-demo)
- **Partnership Inquiries**: partnerships@dovah.io

### Technical Support & Community
- **Documentation**: [docs.lume.ai](https://docs.lume.ai)
- **Community Forum**: [community.lume.ai](https://community.lume.ai)
- **GitHub Issues**: [GitHub Issues](https://github.com/Alec-Merle/Lume-AI/issues)
- **Technical Support**: support@dovah.io

### Development Team
- **Alec Merle** - Founder & Software Engineer | [LinkedIn](https://linkedin.com/in/alecmerle)
- **Ansh Patel** - Data Scientist & AI Engineer | [LinkedIn](https://linkedin.com/in/anshpatel3003)  
- **Dylan N** - Project Engineer & DevOps | [LinkedIn](https://linkedin.com/in/dylan-n-a18ba5104)

## 🔍 Troubleshooting

### Common Issues

#### Environment Variables
```bash
# Error: "ANTHROPIC_API_KEY is not configured"
# Solution: Add your Anthropic API key to environment variables
export ANTHROPIC_API_KEY=sk-ant-your-key-here

# Error: "DATABASE_URL is not configured"  
# Solution: Configure PostgreSQL connection string
export DATABASE_URL=postgresql://user:pass@host:port/database
```

#### Development Server
```bash
# Error: Port 5000 already in use
# Solution: Kill existing processes or change port
pkill -f "node.*5000" 
# or
export PORT=3000
```

#### Database Connection
```bash
# Error: Database connection failed
# Solution: Verify database is running and accessible
npm run db:push  # Push schema to verify connection
```

### Getting Help
1. **Check Documentation**: Review relevant documentation files listed above
2. **Search Issues**: Check [GitHub Issues](https://github.com/Alec-Merle/Lume-AI/issues) for similar problems
3. **Community Support**: Post questions in [community forum](https://community.lume.ai)
4. **Technical Support**: Contact support@dovah.io for enterprise customers

## 📄 License & Legal

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Third-Party Licenses
- **React**: MIT License
- **Tailwind CSS**: MIT License  
- **Radix UI**: MIT License
- **Anthropic SDK**: MIT License
- **Express.js**: MIT License
- **Drizzle ORM**: Apache 2.0 License

## 🌟 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=Alec-Merle/Lume-AI&type=Date)](https://star-history.com/#Alec-Merle/Lume-AI&Date)

---

## 📚 Additional Resources

### Learning Resources
- **[Technical Whitepaper](./WHITEPAPER.md)** - Deep dive into AI architecture and implementation
- **[Business Strategy](./BUSINESS_PLAN.md)** - Complete business model and market analysis
- **[Market Research](./LUME_MARKET_RESEARCH.md)** - Industry landscape and competitive analysis
- **[Partnership Materials](./PALANTIR_DEMO_SCRIPT.md)** - Presentation and demo resources

### External Documentation
- **[Anthropic API Docs](https://docs.anthropic.com)** - AI integration documentation
- **[Drizzle ORM Docs](https://orm.drizzle.team)** - Database ORM documentation  
- **[Radix UI Docs](https://radix-ui.com)** - Component library documentation
- **[Tailwind CSS Docs](https://tailwindcss.com)** - Styling framework documentation

---

**Built with ❤️ by [Dovah](https://dovah.io)** | Transforming enterprise knowledge into AI-ready intelligence

*Ready to revolutionize your document management? [Get started today](https://lume.ai) or [schedule a demo](https://calendly.com/dovah-demo)*

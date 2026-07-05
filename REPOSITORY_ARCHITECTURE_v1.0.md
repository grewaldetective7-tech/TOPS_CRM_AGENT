# TOPS ENTERPRISE PLATFORM - REPOSITORY ARCHITECTURE v1.0

## 🏛️ **APPROVED STRUCTURE**

```
TOPS_ENTERPRISE_PLATFORM/
│
├── 📁 Project-1-TOPS-Universal-CRM/
│   ├── 📁 docs/
│   │   ├── BLUEPRINT_v5.0.md                    [Pending Approval]
│   │   ├── DATABASE_SCHEMA.md                   [Pending Approval]
│   │   ├── API_SPECIFICATIONS.md                [Pending Approval]
│   │   ├── DASHBOARD_REQUIREMENTS.md            [Pending Approval]
│   │   ├── MOBILE_APP_SPECIFICATIONS.md         [Pending Approval]
│   │   ├── BUSINESS_WORKFLOWS.md                [Pending Approval]
│   │   ├── AGENT_DEFINITIONS.md                 [Pending Approval]
│   │   ├── DATA_MODELS.md                       [Pending Approval]
│   │   └── TESTING_STRATEGY.md                  [Pending Approval]
│   │
│   ├── 📁 src/
│   │   ├── 📁 business-logic/
│   │   │   ├── 📁 client-management/
│   │   │   │   ├── client.service.ts
│   │   │   │   ├── client.repository.ts
│   │   │   │   └── client.types.ts
│   │   │   ├── 📁 sales-module/
│   │   │   │   ├── sales.service.ts
│   │   │   │   ├── sales.repository.ts
│   │   │   │   └── sales.types.ts
│   │   │   ├── 📁 payment-collection/
│   │   │   │   ├── payment.service.ts
│   │   │   │   ├── payment.repository.ts
│   │   │   │   └── payment.types.ts
│   │   │   ├── 📁 marketing-module/
│   │   │   │   ├── marketing.service.ts
│   │   │   │   ├── marketing.repository.ts
│   │   │   │   └── marketing.types.ts
│   │   │   ├── 📁 service-module/
│   │   │   │   ├── service.service.ts
│   │   │   │   ├── service.repository.ts
│   │   │   │   └── service.types.ts
│   │   │   └── 📁 renewal-module/
│   │   │       ├── renewal.service.ts
│   │   │       ├── renewal.repository.ts
│   │   │       └── renewal.types.ts
│   │   │
│   │   ├── 📁 database/
│   │   │   ├── 📁 migrations/
│   │   │   │   └── 001_initial_schema.sql
│   │   │   ├── 📁 schema/
│   │   │   │   ├── clients.schema.sql
│   │   │   │   ├── sales.schema.sql
│   │   │   │   ├── payments.schema.sql
│   │   │   │   ├── marketing.schema.sql
│   │   │   │   ├── services.schema.sql
│   │   │   │   └── renewals.schema.sql
│   │   │   └── connection.config.ts
│   │   │
│   │   ├── 📁 apis/
│   │   │   ├── 📁 client-api/
│   │   │   │   ├── client.controller.ts
│   │   │   │   ├── client.routes.ts
│   │   │   │   └── client.validators.ts
│   │   │   ├── 📁 sales-api/
│   │   │   │   ├── sales.controller.ts
│   │   │   │   ├── sales.routes.ts
│   │   │   │   └── sales.validators.ts
│   │   │   ├── 📁 payment-api/
│   │   │   │   ├── payment.controller.ts
│   │   │   │   ├── payment.routes.ts
│   │   │   │   └── payment.validators.ts
│   │   │   ├── 📁 marketing-api/
│   │   │   │   ├── marketing.controller.ts
│   │   │   │   ├── marketing.routes.ts
│   │   │   │   └── marketing.validators.ts
│   │   │   ├── 📁 service-api/
│   │   │   │   ├── service.controller.ts
│   │   │   │   ├── service.routes.ts
│   │   │   │   └── service.validators.ts
│   │   │   └── 📁 renewal-api/
│   │   │       ├── renewal.controller.ts
│   │   │       ├── renewal.routes.ts
│   │   │       └── renewal.validators.ts
│   │   │
│   │   ├── 📁 dashboards/
│   │   │   ├── 📁 dashboard-1-sales-overview/
│   │   │   │   ├── dashboard1.controller.ts
│   │   │   │   ├── dashboard1.service.ts
│   │   │   │   └── dashboard1.types.ts
│   │   │   ├── 📁 dashboard-2-payment-status/
│   │   │   ├── 📁 dashboard-3-client-health/
│   │   │   ├── 📁 dashboard-4-marketing-campaigns/
│   │   │   ├── 📁 dashboard-5-service-tickets/
│   │   │   ├── 📁 dashboard-6-renewals-pipeline/
│   │   │   ├── 📁 dashboard-7-financial-summary/
│   │   │   └── dashboard-counter.service.ts
│   │   │       (Updates only after saved remark/transaction)
│   │   │
│   │   ├── 📁 agents/
│   │   │   ├── 📁 sales-agent/
│   │   │   │   ├── sales-agent.ts
│   │   │   │   └── sales-agent.workflows.ts
│   │   │   ├── 📁 marketing-agent/
│   │   │   │   ├── marketing-agent.ts
│   │   │   │   └── marketing-agent.workflows.ts
│   │   │   ├── 📁 payment-agent/
│   │   │   │   ├── payment-agent.ts
│   │   │   │   └── payment-agent.workflows.ts
│   │   │   └── 📁 service-agent/
│   │   │       ├── service-agent.ts
│   │   │       └── service-agent.workflows.ts
│   │   │
│   │   ├── 📁 workflows/
│   │   │   ├── client-onboarding.workflow.ts
│   │   │   ├── payment-collection.workflow.ts
│   │   │   ├── service-request.workflow.ts
│   │   │   └── renewal.workflow.ts
│   │   │
│   │   └── 📁 types/
│   │       ├── client.types.ts
│   │       ├── sales.types.ts
│   │       ├── payment.types.ts
│   │       └── index.ts
│   │
│   ├── 📁 web-app/
│   │   ├── 📁 src/
│   │   │   ├── 📁 components/
│   │   │   ├── 📁 pages/
│   │   │   ├── 📁 services/
│   │   │   └── App.tsx
│   │   ├── package.json
│   │   └── tsconfig.json
│   │
│   ├── 📁 mobile-app/
│   │   ├── 📁 ios/
│   │   ├── 📁 android/
│   │   ├── 📁 shared/
│   │   └── package.json
│   │
│   ├── 📁 tests/
│   │   ├── 📁 unit/
│   │   ├── 📁 integration/
│   │   └── 📁 e2e/
│   │
│   ├── 📁 config/
│   │   ├── database.config.ts
│   │   ├── environment.config.ts
│   │   └── constants.ts
│   │
│   ├── .env.example
│   ├── package.json
│   ├── tsconfig.json
│   ├── README.md
│   └── CHANGELOG.md
│
├── 📁 Project-2-TOPS-Night-Patrol/
│   ├── 📁 docs/
│   │   ├── BLUEPRINT_v5.0.md                    [Pending Approval]
│   │   ├── DATABASE_SCHEMA.md                   [Pending Approval]
│   │   ├── API_SPECIFICATIONS.md                [Pending Approval]
│   │   ├── DASHBOARD_REQUIREMENTS.md            [Pending Approval]
│   │   ├── MOBILE_APP_SPECIFICATIONS.md         [Pending Approval]
│   │   ├── BUSINESS_WORKFLOWS.md                [Pending Approval]
│   │   ├── AGENT_DEFINITIONS.md                 [Pending Approval]
│   │   ├── DATA_MODELS.md                       [Pending Approval]
│   │   └── TESTING_STRATEGY.md                  [Pending Approval]
│   │
│   ├── 📁 src/
│   │   ├── 📁 business-logic/
│   │   │   ├── 📁 officer-management/
│   │   │   │   ├── officer.service.ts
│   │   │   │   ├── officer.repository.ts
│   │   │   │   └── officer.types.ts
│   │   │   ├── 📁 duty-management/
│   │   │   │   ├── duty.service.ts
│   │   │   │   ├── duty.repository.ts
│   │   │   │   └── duty.types.ts
│   │   │   ├── 📁 beat-management/
│   │   │   │   ├── beat.service.ts
│   │   │   │   ├── beat.repository.ts
│   │   │   │   └── beat.types.ts
│   │   │   ├── 📁 patrol-visits/
│   │   │   │   ├── patrol.service.ts
│   │   │   │   ├── patrol.repository.ts
│   │   │   │   └── patrol.types.ts
│   │   │   ├── 📁 cctv-incidents/
│   │   │   │   ├── incident.service.ts
│   │   │   │   ├── incident.repository.ts
│   │   │   │   └── incident.types.ts
│   │   │   ├── 📁 complaint-response/
│   │   │   │   ├── complaint.service.ts
│   │   │   │   ├── complaint.repository.ts
│   │   │   │   └── complaint.types.ts
│   │   │   └── 📁 qrt-management/
│   │   │       ├── qrt.service.ts
│   │   │       ├── qrt.repository.ts
│   │   │       └── qrt.types.ts
│   │   │
│   │   ├── 📁 database/
│   │   │   ├── 📁 migrations/
│   │   │   │   └── 001_initial_schema.sql
│   │   │   ├── 📁 schema/
│   │   │   │   ├── officers.schema.sql
│   │   │   │   ├── duties.schema.sql
│   │   │   │   ├── beats.schema.sql
│   │   │   │   ├── patrols.schema.sql
│   │   │   │   ├── incidents.schema.sql
│   │   │   │   ├── complaints.schema.sql
│   │   │   │   └── qrt.schema.sql
│   │   │   └── connection.config.ts
│   │   │
│   │   ├── 📁 apis/
│   │   │   ├── 📁 officer-api/
│   │   │   │   ├── officer.controller.ts
│   │   │   │   ├── officer.routes.ts
│   │   │   │   └── officer.validators.ts
│   │   │   ├── 📁 duty-api/
│   │   │   ├── 📁 beat-api/
│   │   │   ├── 📁 patrol-api/
│   │   │   ├── 📁 incident-api/
│   │   │   ├── 📁 complaint-api/
│   │   │   └── 📁 qrt-api/
│   │   │
│   │   ├── 📁 dashboards/
│   │   │   ├── 📁 main-dashboard/
│   │   │   │   ├── main-dashboard.controller.ts
│   │   │   │   ├── main-dashboard.service.ts
│   │   │   │   └── main-dashboard.types.ts
│   │   │   ├── 📁 beat-dashboards/
│   │   │   │   ├── 📁 beat-1-dashboard/
│   │   │   │   ├── 📁 beat-2-dashboard/
│   │   │   │   ├── 📁 beat-3-dashboard/
│   │   │   │   ├── 📁 beat-4-dashboard/
│   │   │   │   ├── 📁 beat-5-dashboard/
│   │   │   │   ├── 📁 beat-6-dashboard/
│   │   │   │   ├── 📁 beat-7-dashboard/
│   │   │   │   └── beat-dashboard.service.ts
│   │   │   └── dashboard-counter.service.ts
│   │   │       (Updates only after saved patrol visit/remark)
│   │   │
│   │   ├── 📁 agents/
│   │   │   ├── 📁 patrol-agent/
│   │   │   │   ├── patrol-agent.ts
│   │   │   │   └── patrol-agent.workflows.ts
│   │   │   ├── 📁 incident-agent/
│   │   │   │   ├── incident-agent.ts
│   │   │   │   └── incident-agent.workflows.ts
│   │   │   ├── 📁 qrt-agent/
│   │   │   │   ├── qrt-agent.ts
│   │   │   │   └── qrt-agent.workflows.ts
│   │   │   └── 📁 complaint-agent/
│   │   │       ├── complaint-agent.ts
│   │   │       └── complaint-agent.workflows.ts
│   │   │
│   │   ├── 📁 workflows/
│   │   │   ├── duty-on-off.workflow.ts
│   │   │   ├── patrol-visit.workflow.ts
│   │   │   ├── incident-response.workflow.ts
│   │   │   ├── complaint-response.workflow.ts
│   │   │   └── qrt-dispatch.workflow.ts
│   │   │
│   │   └── 📁 types/
│   │       ├── officer.types.ts
│   │       ├── patrol.types.ts
│   │       ├── incident.types.ts
│   │       └── index.ts
│   │
│   ├── 📁 web-app/
│   │   ├── 📁 src/
│   │   │   ├── 📁 components/
│   │   │   ├── 📁 pages/
│   │   │   ├── 📁 services/
│   │   │   └── App.tsx
│   │   ├── package.json
│   │   └── tsconfig.json
│   │
│   ├── 📁 mobile-app/
│   │   ├── 📁 ios/
│   │   ├── 📁 android/
│   │   ├── 📁 shared/
│   │   └── package.json
│   │
│   ├── 📁 tests/
│   │   ├── 📁 unit/
│   │   ├── 📁 integration/
│   │   └── 📁 e2e/
│   │
│   ├── 📁 config/
│   │   ├── database.config.ts
│   │   ├── environment.config.ts
│   │   └── constants.ts
│   │
│   ├── .env.example
│   ├── package.json
│   ├── tsconfig.json
│   ├── README.md
│   └── CHANGELOG.md
│
├── 📁 Shared-Services/
│   ├── 📁 docs/
│   │   ├── ARCHITECTURE_OVERVIEW.md             [Pending Approval]
│   │   ├── DATABASE_SCHEMA.md                   [Pending Approval]
│   │   ├── API_SPECIFICATIONS.md                [Pending Approval]
│   │   ├── AUTHENTICATION_GUIDE.md              [Pending Approval]
│   │   ├── RBAC_SPECIFICATIONS.md               [Pending Approval]
│   │   ├── DATA_ISOLATION_POLICY.md             [Pending Approval]
│   │   ├── TESTING_STRATEGY.md                  [Pending Approval]
│   │   └── DEPLOYMENT_GUIDE.md                  [Pending Approval]
│   │
│   ├── 📁 src/
│   │   ├── 📁 authentication/
│   │   │   ├── 📁 jwt/
│   │   │   │   ├── jwt.service.ts
│   │   │   │   ├── jwt.strategy.ts
│   │   │   │   └── jwt.types.ts
│   │   │   ├── 📁 oauth/
│   │   │   │   ├── oauth.service.ts
│   │   │   │   └── oauth.types.ts
│   │   │   ├── 📁 password/
│   │   │   │   ├── password.service.ts
│   │   │   │   └── password.types.ts
│   │   │   ├── auth.controller.ts
│   │   │   ├── auth.routes.ts
│   │   │   └── auth.validators.ts
│   │   │
│   │   ├── 📁 rbac/
│   │   │   ├── 📁 roles/
│   │   │   │   ├── roles.service.ts
│   │   │   │   ├── roles.repository.ts
│   │   │   │   └── roles.types.ts
│   │   │   ├── 📁 permissions/
│   │   │   │   ├── permissions.service.ts
│   │   │   │   ├── permissions.repository.ts
│   │   │   │   └── permissions.types.ts
│   │   │   ├── 📁 access-control/
│   │   │   │   ├── access-control.service.ts
│   │   │   │   ├── access-control.middleware.ts
│   │   │   │   └── access-control.types.ts
│   │   │   ├── rbac.controller.ts
│   │   │   ├── rbac.routes.ts
│   │   │   └── rbac.validators.ts
│   │   │
│   │   ├── 📁 masters/
│   │   │   ├── 📁 client-master/
│   │   │   │   ├── client-master.service.ts
│   │   │   │   ├── client-master.repository.ts
│   │   │   │   └── client-master.types.ts
│   │   │   ├── 📁 beat-master/
│   │   │   │   ├── beat-master.service.ts
│   │   │   │   ├── beat-master.repository.ts
│   │   │   │   └── beat-master.types.ts
│   │   │   ├── 📁 branch-master/
│   │   │   │   ├── branch-master.service.ts
│   │   │   │   ├── branch-master.repository.ts
│   │   │   │   └── branch-master.types.ts
│   │   │   ├── 📁 user-master/
│   │   │   │   ├── user-master.service.ts
│   │   │   │   ├── user-master.repository.ts
│   │   │   │   └── user-master.types.ts
│   │   │   ├── masters.controller.ts
│   │   │   ├── masters.routes.ts
│   │   │   └── masters.validators.ts
│   │   │
│   │   ├── 📁 notifications/
│   │   │   ├── 📁 email/
│   │   │   │   ├── email.service.ts
│   │   │   │   └── email.types.ts
│   │   │   ├── 📁 sms/
│   │   │   │   ├── sms.service.ts
│   │   │   │   └── sms.types.ts
│   │   │   ├── 📁 whatsapp/
│   │   │   │   ├── whatsapp.service.ts
│   │   │   │   └── whatsapp.types.ts
│   │   │   ├── 📁 in-app/
│   │   │   │   ├── in-app.service.ts
│   │   │   │   └── in-app.types.ts
│   │   │   ├── notification.engine.ts
│   │   │   ├── notification.controller.ts
│   │   │   ├── notification.routes.ts
│   │   │   └── notification.types.ts
│   │   │
│   │   ├── 📁 audit/
│   │   │   ├── 📁 logging/
│   │   │   │   ├── audit-logger.service.ts
│   │   │   │   └── audit-logger.types.ts
│   │   │   ├── 📁 activity-tracking/
│   │   │   │   ├── activity-tracker.service.ts
│   │   │   │   └── activity-tracker.types.ts
│   │   │   ├── 📁 compliance/
│   │   │   │   ├── compliance-reporter.service.ts
│   │   │   │   └── compliance-reporter.types.ts
│   │   │   ├── audit.controller.ts
│   │   │   ├── audit.routes.ts
│   │   │   └── audit.types.ts
│   │   │
│   │   ├── 📁 ui-components/
│   │   │   ├── 📁 buttons/
│   │   │   ├── 📁 forms/
│   │   │   ├── 📁 modals/
│   │   │   ├── 📁 tables/
│   │   │   ├── 📁 cards/
│   │   │   └── 📁 layouts/
│   │   │
│   │   ├── 📁 utilities/
│   │   │   ├── 📁 validators/
│   │   │   ├── 📁 formatters/
│   │   │   ├── 📁 helpers/
│   │   │   └── 📁 constants/
│   │   │
│   │   ├── 📁 database/
│   │   │   ├── 📁 migrations/
│   │   │   │   └── 001_initial_shared_schema.sql
│   │   │   ├── 📁 schema/
│   │   │   │   ├── users.schema.sql
│   │   │   │   ├── roles.schema.sql
│   │   │   │   ├── permissions.schema.sql
│   │   │   │   ├── client-master.schema.sql
│   │   │   │   ├── beat-master.schema.sql
│   │   │   │   ├── branch-master.schema.sql
│   │   │   │   ├── notification-templates.schema.sql
│   │   │   │   └── audit-logs.schema.sql
│   │   │   └── connection.config.ts
│   │   │
│   │   ├── 📁 middleware/
│   │   │   ├── auth.middleware.ts
│   │   │   ├── rbac.middleware.ts
│   │   │   ├── audit.middleware.ts
│   │   │   └── error-handler.middleware.ts
│   │   │
│   │   ├── 📁 types/
│   │   │   ├── auth.types.ts
│   │   │   ├── rbac.types.ts
│   │   │   ├── master.types.ts
│   │   │   ├── notification.types.ts
│   │   │   ├── audit.types.ts
│   │   │   └── index.ts
│   │   │
│   │   └── 📁 config/
│   │       ├── database.config.ts
│   │       ├── environment.config.ts
│   │       └── constants.ts
│   │
│   ├── 📁 tests/
│   │   ├── 📁 unit/
│   │   ├── 📁 integration/
│   │   └── 📁 e2e/
│   │
│   ├── .env.example
│   ├── package.json
│   ├── tsconfig.json
│   ├── README.md
│   └── CHANGELOG.md
│
├── 📁 docs/
│   ├── PLATFORM_OVERVIEW.md
│   ├── ARCHITECTURE_GUIDE.md
│   ├── DATA_ISOLATION_POLICY.md
│   ├── SECURITY_POLICY.md
│   ├── DATABASE_STRUCTURE.md
│   ├── INTEGRATION_GUIDE.md
│   ├── DEPLOYMENT_GUIDE.md
│   ├── TESTING_STRATEGY.md
│   ├── CONTRIBUTION_GUIDELINES.md
│   ├── PROJECT_GOVERNANCE.md
│   └── CHANGELOG.md
│
├── 📁 infrastructure/
│   ├── 📁 docker/
│   │   ├── Dockerfile.shared
│   │   ├── Dockerfile.project1
│   │   ├── Dockerfile.project2
│   │   └── docker-compose.yml
│   ├── 📁 kubernetes/
│   │   ├── 📁 shared/
│   │   ├── 📁 project1/
│   │   ├── 📁 project2/
│   │   └── README.md
│   ├── 📁 terraform/
│   │   ├── shared/
│   │   ├── project1/
│   │   └── project2/
│   └── README.md
│
├── 📁 scripts/
│   ├── setup-database.sh
│   ├── run-migrations.sh
│   ├── seed-data.sh
│   └── test-isolation.sh
│
├── .gitignore
├── .github/
│   ├── 📁 workflows/
│   │   ├── ci-shared.yml
│   │   ├── ci-project1.yml
│   │   ├── ci-project2.yml
│   │   ├── security-scan.yml
│   │   ├── isolation-test.yml
│   │   └── deployment.yml
│   └── 📁 pull_request_template/
│       ├── shared_pr_template.md
│       ├── project1_pr_template.md
│       └── project2_pr_template.md
│
├── README.md
├── ARCHITECTURE.md
├── APPROVED_PRINCIPLES.md
├── LICENSE
└── CHANGELOG.md
```

---

## 📊 **DATABASE SCHEMA ARCHITECTURE**

### **Single PostgreSQL Server with Logical Separation**

```sql
-- Schema Isolation
CREATE SCHEMA IF NOT EXISTS shared;
CREATE SCHEMA IF NOT EXISTS project1_crm;
CREATE SCHEMA IF NOT EXISTS project2_patrol;

-- SHARED SCHEMA (Access by both projects)
-- Users, Roles, Permissions, Masters, Audit, Notifications

CREATE TABLE shared.users (
    user_id UUID PRIMARY KEY,
    username VARCHAR(255) UNIQUE NOT NULL,
    email VARCHAR(255) UNIQUE NOT NULL,
    password_hash VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    updated_at TIMESTAMP DEFAULT NOW(),
    updated_by UUID REFERENCES shared.users(user_id),
    is_active BOOLEAN DEFAULT TRUE
);

CREATE TABLE shared.roles (
    role_id UUID PRIMARY KEY,
    role_name VARCHAR(100) UNIQUE NOT NULL,
    description TEXT,
    project_scope VARCHAR(50), -- 'shared', 'project1', 'project2'
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id)
);

CREATE TABLE shared.permissions (
    permission_id UUID PRIMARY KEY,
    permission_name VARCHAR(255) UNIQUE NOT NULL,
    description TEXT,
    resource VARCHAR(100),
    action VARCHAR(50),
    project_scope VARCHAR(50),
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id)
);

CREATE TABLE shared.role_permissions (
    role_id UUID REFERENCES shared.roles(role_id),
    permission_id UUID REFERENCES shared.permissions(permission_id),
    PRIMARY KEY (role_id, permission_id)
);

CREATE TABLE shared.user_roles (
    user_id UUID REFERENCES shared.users(user_id),
    role_id UUID REFERENCES shared.roles(role_id),
    assigned_at TIMESTAMP DEFAULT NOW(),
    assigned_by UUID REFERENCES shared.users(user_id),
    PRIMARY KEY (user_id, role_id)
);

CREATE TABLE shared.client_master (
    client_id UUID PRIMARY KEY,
    client_name VARCHAR(255) NOT NULL,
    client_code VARCHAR(50) UNIQUE NOT NULL,
    contact_person VARCHAR(255),
    phone VARCHAR(20),
    email VARCHAR(255),
    address TEXT,
    city VARCHAR(100),
    state VARCHAR(100),
    country VARCHAR(100),
    postal_code VARCHAR(10),
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    updated_at TIMESTAMP DEFAULT NOW(),
    updated_by UUID REFERENCES shared.users(user_id),
    is_active BOOLEAN DEFAULT TRUE
);

CREATE TABLE shared.beat_master (
    beat_id UUID PRIMARY KEY,
    beat_code VARCHAR(50) UNIQUE NOT NULL,
    beat_name VARCHAR(255) NOT NULL,
    area_description TEXT,
    beat_supervisor_id UUID REFERENCES shared.users(user_id),
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    updated_at TIMESTAMP DEFAULT NOW(),
    updated_by UUID REFERENCES shared.users(user_id),
    is_active BOOLEAN DEFAULT TRUE
);

CREATE TABLE shared.branch_master (
    branch_id UUID PRIMARY KEY,
    branch_code VARCHAR(50) UNIQUE NOT NULL,
    branch_name VARCHAR(255) NOT NULL,
    branch_manager_id UUID REFERENCES shared.users(user_id),
    location TEXT,
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    updated_at TIMESTAMP DEFAULT NOW(),
    updated_by UUID REFERENCES shared.users(user_id),
    is_active BOOLEAN DEFAULT TRUE
);

CREATE TABLE shared.audit_logs (
    audit_id UUID PRIMARY KEY,
    user_id UUID REFERENCES shared.users(user_id),
    action VARCHAR(100) NOT NULL,
    resource_type VARCHAR(100),
    resource_id VARCHAR(255),
    old_values JSONB,
    new_values JSONB,
    project_scope VARCHAR(50),
    ip_address VARCHAR(45),
    user_agent TEXT,
    timestamp TIMESTAMP DEFAULT NOW(),
    status VARCHAR(20) -- 'success', 'failure'
);

CREATE TABLE shared.notification_templates (
    template_id UUID PRIMARY KEY,
    template_name VARCHAR(255) UNIQUE NOT NULL,
    template_type VARCHAR(50), -- 'email', 'sms', 'whatsapp', 'in-app'
    subject VARCHAR(255),
    body TEXT,
    project_scope VARCHAR(50),
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    is_active BOOLEAN DEFAULT TRUE
);

-- PROJECT 1 SCHEMA (CRM Only)
-- Client management, Sales, Payments, Marketing, Service, Renewals

CREATE TABLE project1_crm.clients (
    client_id UUID PRIMARY KEY,
    client_master_id UUID REFERENCES shared.client_master(client_id),
    contract_type VARCHAR(100),
    contract_value DECIMAL(15,2),
    contract_start_date DATE,
    contract_end_date DATE,
    renewal_due_date DATE,
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    updated_at TIMESTAMP DEFAULT NOW(),
    updated_by UUID REFERENCES shared.users(user_id)
);

CREATE TABLE project1_crm.sales (
    sale_id UUID PRIMARY KEY,
    client_id UUID REFERENCES project1_crm.clients(client_id),
    opportunity_name VARCHAR(255),
    value DECIMAL(15,2),
    stage VARCHAR(100),
    probability_percentage INTEGER,
    expected_close_date DATE,
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    updated_at TIMESTAMP DEFAULT NOW(),
    updated_by UUID REFERENCES shared.users(user_id)
);

CREATE TABLE project1_crm.payments (
    payment_id UUID PRIMARY KEY,
    client_id UUID REFERENCES project1_crm.clients(client_id),
    invoice_number VARCHAR(50) UNIQUE NOT NULL,
    amount DECIMAL(15,2),
    due_date DATE,
    payment_date DATE,
    status VARCHAR(50),
    payment_method VARCHAR(100),
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    updated_at TIMESTAMP DEFAULT NOW(),
    updated_by UUID REFERENCES shared.users(user_id)
);

CREATE TABLE project1_crm.marketing (
    campaign_id UUID PRIMARY KEY,
    campaign_name VARCHAR(255),
    target_segment VARCHAR(255),
    status VARCHAR(50),
    start_date DATE,
    end_date DATE,
    budget DECIMAL(15,2),
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    updated_at TIMESTAMP DEFAULT NOW(),
    updated_by UUID REFERENCES shared.users(user_id)
);

CREATE TABLE project1_crm.services (
    service_id UUID PRIMARY KEY,
    client_id UUID REFERENCES project1_crm.clients(client_id),
    service_name VARCHAR(255),
    status VARCHAR(50),
    priority VARCHAR(20),
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    updated_at TIMESTAMP DEFAULT NOW(),
    updated_by UUID REFERENCES shared.users(user_id)
);

CREATE TABLE project1_crm.renewals (
    renewal_id UUID PRIMARY KEY,
    client_id UUID REFERENCES project1_crm.clients(client_id),
    renewal_date DATE,
    status VARCHAR(50),
    renewal_value DECIMAL(15,2),
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    updated_at TIMESTAMP DEFAULT NOW(),
    updated_by UUID REFERENCES shared.users(user_id)
);

-- Dashboard counter table (updates only on saved remark/transaction)
CREATE TABLE project1_crm.dashboard_counters (
    counter_id UUID PRIMARY KEY,
    dashboard_id VARCHAR(50),
    counter_name VARCHAR(100),
    counter_value INTEGER,
    last_updated_at TIMESTAMP,
    last_updated_by UUID REFERENCES shared.users(user_id)
);

-- PROJECT 2 SCHEMA (Night Patrol Only)
-- Officer management, Duty, Beat assignments, Patrol visits, Incidents, Complaints, QRT

CREATE TABLE project2_patrol.officers (
    officer_id UUID PRIMARY KEY,
    user_id UUID REFERENCES shared.users(user_id),
    officer_badge_number VARCHAR(50) UNIQUE NOT NULL,
    rank VARCHAR(50),
    assigned_beat_id UUID REFERENCES shared.beat_master(beat_id),
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    updated_at TIMESTAMP DEFAULT NOW(),
    updated_by UUID REFERENCES shared.users(user_id)
);

CREATE TABLE project2_patrol.duties (
    duty_id UUID PRIMARY KEY,
    officer_id UUID REFERENCES project2_patrol.officers(officer_id),
    duty_date DATE NOT NULL,
    duty_start_time TIME,
    duty_end_time TIME,
    status VARCHAR(50), -- 'on_duty', 'off_duty', 'on_leave'
    remarks TEXT,
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    updated_at TIMESTAMP DEFAULT NOW(),
    updated_by UUID REFERENCES shared.users(user_id)
);

CREATE TABLE project2_patrol.patrol_visits (
    patrol_id UUID PRIMARY KEY,
    officer_id UUID REFERENCES project2_patrol.officers(officer_id),
    beat_id UUID REFERENCES shared.beat_master(beat_id),
    visit_date DATE NOT NULL,
    visit_time TIME NOT NULL,
    location_description TEXT,
    status VARCHAR(50),
    remarks TEXT,
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    updated_at TIMESTAMP DEFAULT NOW(),
    updated_by UUID REFERENCES shared.users(user_id)
);

CREATE TABLE project2_patrol.cctv_incidents (
    incident_id UUID PRIMARY KEY,
    beat_id UUID REFERENCES shared.beat_master(beat_id),
    incident_type VARCHAR(100),
    severity VARCHAR(50),
    description TEXT,
    incident_time TIMESTAMP,
    reported_by UUID REFERENCES shared.users(user_id),
    assigned_to UUID REFERENCES project2_patrol.officers(officer_id),
    status VARCHAR(50),
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    updated_at TIMESTAMP DEFAULT NOW(),
    updated_by UUID REFERENCES shared.users(user_id)
);

CREATE TABLE project2_patrol.complaints (
    complaint_id UUID PRIMARY KEY,
    client_id UUID REFERENCES shared.client_master(client_id),
    beat_id UUID REFERENCES shared.beat_master(beat_id),
    complaint_type VARCHAR(100),
    description TEXT,
    severity VARCHAR(50),
    status VARCHAR(50),
    assigned_to UUID REFERENCES project2_patrol.officers(officer_id),
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    updated_at TIMESTAMP DEFAULT NOW(),
    updated_by UUID REFERENCES shared.users(user_id)
);

CREATE TABLE project2_patrol.qrt_dispatch (
    qrt_id UUID PRIMARY KEY,
    incident_or_complaint_id VARCHAR(255),
    officer_ids UUID[], -- Array of officer IDs
    dispatch_time TIMESTAMP,
    response_status VARCHAR(50),
    estimated_arrival_time TIMESTAMP,
    actual_arrival_time TIMESTAMP,
    remarks TEXT,
    created_at TIMESTAMP DEFAULT NOW(),
    created_by UUID REFERENCES shared.users(user_id),
    updated_at TIMESTAMP DEFAULT NOW(),
    updated_by UUID REFERENCES shared.users(user_id)
);

-- Dashboard counter table (updates only on saved patrol visit/remark)
CREATE TABLE project2_patrol.dashboard_counters (
    counter_id UUID PRIMARY KEY,
    dashboard_id VARCHAR(50),
    counter_name VARCHAR(100),
    counter_value INTEGER,
    last_updated_at TIMESTAMP,
    last_updated_by UUID REFERENCES shared.users(user_id)
);

-- Create indexes for isolation and performance
CREATE INDEX idx_shared_users_active ON shared.users(is_active);
CREATE INDEX idx_project1_crm_clients ON project1_crm.clients(client_id);
CREATE INDEX idx_project2_patrol_officers ON project2_patrol.officers(officer_id);
CREATE INDEX idx_shared_audit_timestamp ON shared.audit_logs(timestamp);
CREATE INDEX idx_shared_audit_project_scope ON shared.audit_logs(project_scope);
```

---

## 🔐 **DATA ISOLATION ENFORCEMENT**

### **Strict Project Boundaries**

```
PROJECT 1 (CRM) ↔ SHARED ↔ PROJECT 2 (PATROL)

❌ PROJECT 1 → PROJECT 2: FORBIDDEN
   - No direct schema access
   - No data replication
   - No shared tables

❌ PROJECT 2 → PROJECT 1: FORBIDDEN
   - No direct schema access
   - No data replication
   - No shared tables

✅ BOTH ← SHARED: READ-ONLY ACCESS
   - Users (shared.users)
   - Roles (shared.roles)
   - Permissions (shared.permissions)
   - Client Master (shared.client_master) - for project 1
   - Beat Master (shared.beat_master) - for project 2
   - Branch Master (shared.branch_master) - both
   - Audit Logs (shared.audit_logs) - project-scoped
   - Notification Templates (shared.notification_templates) - project-scoped
```

---

## 📋 **DOCUMENTATION STATUS - ALL MARKED [Pending Approval]**

### **Shared Services (8 documents)**
- [ ] ARCHITECTURE_OVERVIEW.md [Pending Approval]
- [ ] DATABASE_SCHEMA.md [Pending Approval]
- [ ] API_SPECIFICATIONS.md [Pending Approval]
- [ ] AUTHENTICATION_GUIDE.md [Pending Approval]
- [ ] RBAC_SPECIFICATIONS.md [Pending Approval]
- [ ] DATA_ISOLATION_POLICY.md [Pending Approval]
- [ ] TESTING_STRATEGY.md [Pending Approval]
- [ ] DEPLOYMENT_GUIDE.md [Pending Approval]

### **Project 1 - TOPS Universal CRM (9 documents)**
- [ ] BLUEPRINT_v5.0.md [Pending Approval]
- [ ] DATABASE_SCHEMA.md [Pending Approval]
- [ ] API_SPECIFICATIONS.md [Pending Approval]
- [ ] DASHBOARD_REQUIREMENTS.md [Pending Approval]
- [ ] MOBILE_APP_SPECIFICATIONS.md [Pending Approval]
- [ ] BUSINESS_WORKFLOWS.md [Pending Approval]
- [ ] AGENT_DEFINITIONS.md [Pending Approval]
- [ ] DATA_MODELS.md [Pending Approval]
- [ ] TESTING_STRATEGY.md [Pending Approval]

### **Project 2 - TOPS Night Patrol (9 documents)**
- [ ] BLUEPRINT_v5.0.md [Pending Approval]
- [ ] DATABASE_SCHEMA.md [Pending Approval]
- [ ] API_SPECIFICATIONS.md [Pending Approval]
- [ ] DASHBOARD_REQUIREMENTS.md [Pending Approval]
- [ ] MOBILE_APP_SPECIFICATIONS.md [Pending Approval]
- [ ] BUSINESS_WORKFLOWS.md [Pending Approval]
- [ ] AGENT_DEFINITIONS.md [Pending Approval]
- [ ] DATA_MODELS.md [Pending Approval]
- [ ] TESTING_STRATEGY.md [Pending Approval]

### **Platform-Level (8 documents)**
- [ ] PLATFORM_OVERVIEW.md
- [ ] ARCHITECTURE_GUIDE.md
- [ ] DATA_ISOLATION_POLICY.md
- [ ] SECURITY_POLICY.md
- [ ] DATABASE_STRUCTURE.md
- [ ] INTEGRATION_GUIDE.md
- [ ] DEPLOYMENT_GUIDE.md
- [ ] TESTING_STRATEGY.md

**TOTAL: 34 Placeholder Documents (All marked [Pending Approval])**

---

## 🎯 **IMPLEMENTATION PHASES**

### **Phase 1: Shared Services Foundation**
- Setup Shared-Services module
- Implement Authentication Service
- Implement RBAC Service
- Setup Master Data Management
- Implement Notification Engine
- Implement Audit Engine
- Setup shared database schema
- Create common UI components

### **Phase 2: Project 1 – TOPS Universal CRM v5.0**
- Setup Project-1-TOPS-Universal-CRM module
- Implement CRM database schema
- Build CRM business logic
- Build CRM APIs
- Build 7 CRM dashboards
- Build CRM agents
- Create CRM mobile app
- Testing & validation

### **Phase 3: Project 2 – TOPS Night Patrol v5.0**
- Setup Project-2-TOPS-Night-Patrol module
- Implement Patrol database schema
- Build Patrol business logic
- Build Patrol APIs
- Build Main + 7 Beat dashboards
- Build Patrol agents
- Create Patrol mobile app
- Testing & validation

### **Phase 4: Integration, Security Validation, UAT & Production Release**
- Cross-project integration tests
- Security & isolation tests
- Shared platform integration tests
- User acceptance testing
- Production deployment
- Post-deployment validation

---

## ✅ **APPROVED PRINCIPLES CHECKLIST**

- ✅ Two completely independent enterprise projects
- ✅ No business logic mixing
- ✅ Single Source of Truth (SSOT) via shared schema
- ✅ Enterprise documentation before implementation
- ✅ Modular architecture
- ✅ Audit-safe implementation

---

## 🔐 **SECURITY & ISOLATION MEASURES**

### **Database Level**
- Schema-based isolation (project1_crm, project2_patrol, shared)
- Role-based access control (RBAC) via shared.user_roles
- Audit logging for all cross-schema access
- Foreign key constraints enforcing integrity
- Separate connections per project

### **Application Level**
- Middleware validation on project scope
- API routing isolation
- Request context verification
- Transaction isolation
- Error message sanitization

### **Deployment Level**
- Separate CI/CD pipelines per project
- Isolation tests in github workflows
- Environment-based access control
- Separate deployment processes

---

## 📊 **METRICS & MONITORING**

### **Isolation Metrics**
- Cross-schema access violations (should be zero in production)
- Audit log entries per project
- Data sync integrity checks
- API endpoint isolation validation

### **Performance Metrics**
- Query response times per project
- Database connection pool utilization
- API gateway throughput
- Dashboard load times

---

**REVISED ARCHITECTURE COMPLETE**

All corrections implemented:
- ✅ Single TOPS_ENTERPRISE_PLATFORM repository
- ✅ Three independent top-level modules
- ✅ Shared-Services with approved components only
- ✅ Complete database isolation with shared schema
- ✅ All documentation marked [Pending Approval]
- ✅ Four-phase implementation roadmap
- ✅ Security & isolation enforcement mechanisms

**Status: Ready for Final Approval** ✓

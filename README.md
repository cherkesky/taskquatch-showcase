# Taskquatch Showcase

Taskquatch is a hyperlocal marketplace connecting neighbors with trusted local providers.

This repository is a public, portfolio-style showcase for the product at [taskquatch.app](https://taskquatch.app). It presents the product concept, marketplace metrics, high-level architecture, and technical outcomes without exposing proprietary production source code.

## What This Repository Includes

- A static GitHub Pages-compatible showcase site
- Product overview and marketplace positioning
- Public-facing metrics and technical highlights
- Screenshot gallery with public-safe mockups and sanitized simulator captures
- A simplified architecture diagram
- Public-safe operations, reliability, growth, payments, and trust workflows
- Documentation describing the showcase scope

## What This Repository Excludes

This repository intentionally does not include:

- Production application source code
- Backend implementation details
- Credentials, secrets, environment files, or private infrastructure state
- Internal admin logic, private APIs, or proprietary business logic
- Customer, vendor, payment, or operational data

## Live Product

Visit the product website: [taskquatch.app](https://taskquatch.app)

## Showcase Preview

![Taskquatch Home Mockup](screenshots/home.svg)

## Product Areas

Taskquatch brings together the major workflows required to operate a local services marketplace:

- Task posting for neighbors who need help
- Local matching between posted work and trusted providers
- Marketplace payments powered by Stripe
- Vendor onboarding and profile setup
- Trust and safety workflows
- Operations tooling for marketplace support

## Simplified Architecture

![Simplified Taskquatch Architecture](assets/architecture.svg)

The public architecture view is intentionally high level:

- React Native powers the mobile customer and vendor experience.
- Web surfaces are delivered through static hosting and CDN-backed infrastructure.
- API Gateway exposes REST routes and WebSocket entry points for app traffic.
- AWS Lambda coordinates marketplace APIs, payments, notifications, and operations workflows.
- PostgreSQL stores relational marketplace data, with Redis used for caching.
- SQS queues and dead-letter queues support asynchronous processing.
- S3 stores public assets and file-oriented workflow data.
- DynamoDB supports realtime WebSocket connection state.
- Stripe and other external providers integrate through backend services.
- Terraform provisions the AWS infrastructure, domains, and permissions.

## Trust & Safety Workflow

Taskquatch includes identity verification as part of vendor onboarding and marketplace safety. The public showcase presents this only as a high-level workflow:

`Vendor Onboarding -> Secure Upload -> Protected Storage -> Verification Provider -> Operations Review -> Marketplace Access`

This section intentionally excludes internal routes, provider payloads, credentials, webhook details, storage paths, and proprietary review logic.

## Marketplace Operations

Taskquatch includes operational tooling and workflows for running a two-sided marketplace:

- Vendor approvals and onboarding review
- Task lifecycle visibility
- Customer support workflows
- Payout oversight and reconciliation support
- Content moderation and reporting
- Health/status visibility for key marketplace flows

Taskquatch includes support and alerting integrations such as live support chat and Slack-based operational notifications, helping shorten response times for customer issues, vendor workflows, and reliability events.

## Reliability & Automation

The platform uses background automation to keep marketplace activity moving:

- Queue-backed workflows with dead-letter handling
- Scheduled jobs for reminders, recurring tasks, and maintenance workflows
- Health checks for important API surfaces
- Error reporting for production awareness
- Notification processors for customer and provider communication

## Growth Systems

Taskquatch combines product and growth infrastructure to support local marketplace expansion:

- Referral flows
- Coupons and promotional incentives
- Marketing landing pages
- Lifecycle email and push messaging
- Local service/category content

## Payments & Payouts Workflow

The public showcase describes marketplace payments at a high level:

`Task Completed -> Payment Captured -> Platform Fee Applied -> Vendor Payout -> Reconciliation`

This intentionally avoids Stripe implementation details, payment identifiers, internal exceptions, and financial records.

## Realtime Updates

Taskquatch includes realtime task status infrastructure for app experiences where freshness matters. The public showcase describes this only at a capability level:

- WebSocket entry point
- Task status publishing
- Connection state tracking
- Mobile fallback behavior

## Admin Tooling

The showcase includes a sanitized admin dashboard mockup and broad internal tooling categories without exposing private dashboards, real operational data, or source code:

- User support
- Vendor review
- Task monitoring
- Content reports
- Payout oversight
- Health checks
- Marketing operations
- Data export support

## Case Study

Taskquatch was designed, built, and operated as an end-to-end local services marketplace:

- **Problem:** Neighbors need small local jobs completed quickly, while capable local providers need better access to nearby demand.
- **Solution:** Taskquatch connects customers and providers through task posting, matching, messaging, payments, verification, and operations tooling.
- **Outcome:** The product grew into a multi-city marketplace with thousands of users, hundreds of vendors, and daily marketplace activity.

## Technical Highlights

- React Native
- Node.js
- AWS
- Terraform
- Stripe
- Docker
- PostgreSQL

## Screenshots

The showcase includes public-safe screenshot cards for:

- Home, using a public-safe mockup
- Create Task, using a cropped simulator capture
- Tasks Tab, using a public-safe mockup
- Vendor Dashboard, using a public-safe mockup
- Messaging, using a sanitized simulator capture
- Admin Dashboard, using a sanitized mockup

Mockups can be replaced with approved public screenshots later if they contain no private user, vendor, payment, or operational data.

## Running Locally

No build system is required. Open `index.html` directly in a browser, or serve the folder with any static file server.

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.

## GitHub Pages

This repository is compatible with GitHub Pages. Set the Pages source to the repository root and publish from the default branch.

## About the Builder

Designed, built, and operated end-to-end by Guy Cherkesky.

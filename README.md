# GitHub Actions Workflow for Prisma Postgres

[Prisma Postgres v1 API documentation](https://api.prisma.io/v1/swagger-editor)

**Open-source GitHub Actions workflow for automated Prisma Postgres preview environments**

This repository contains a reusable GitHub Actions workflow that automates the creation and management of feature branch databases using Prisma Postgres. Originally developed for [MasterBoard](https://masterboardapp.com) — a comprehensive business management platform that helps companies streamline their operations, track performance, and make data-driven decisions.

## What it does

This workflow provides automated preview environment management for applications using Prisma and PostgreSQL:

### On Pull Request Creation/Updates:

- **Database Management**: Automatically creates isolated Prisma Postgres databases for each pull request
- **Schema Setup**: Applies database migrations and generates Prisma client
- **Data Seeding**: Seeds the database with test data for realistic preview environments
- **Vercel Deployment**: Deploys the application to Vercel with the new database connection
- **PR Comments**: Automatically comments on pull requests with preview URLs and database information

### On Pull Request Closure:

- **Cleanup**: Automatically deletes feature branch databases to prevent resource waste
- **Cost Management**: Ensures no orphaned databases remain after development is complete

## Features

- ✅ **Isolated Environments**: Each PR gets its own database instance
- ✅ **Automatic Cleanup**: Databases are removed when PRs are closed
- ✅ **Retry Logic**: Built-in retry mechanisms for reliable database operations
- ✅ **Environment Validation**: Comprehensive checks for required secrets and configuration
- ✅ **Concurrent Protection**: Prevents multiple workflow runs for the same PR

## About MasterBoard

[MasterBoard](https://masterboardapp.com) is a comprehensive business management platform specifically designed for the hydraulics repair industry. MasterBoard helps hydraulics repair companies streamline their entire operation:

### Core Business Management

- **Work Order Management**: Track hydraulic repair jobs from intake to completion
- **Equipment & Inventory Tracking**: Manage hydraulic components, seals, pumps, and parts inventory
- **Customer Relationship Management**: Maintain detailed customer profiles and service history
- **QuickBooks Integration**: Seamless financial management and accounting synchronization
- **Invoicing & Billing**: Automated billing for hydraulic repair services and parts

### Operational Excellence

- **Technician Scheduling**: Optimize field service routing and job assignments
- **Mobile Workforce Management**: Field technicians can update job status and capture documentation
- **Equipment Maintenance Tracking**: Preventive maintenance scheduling for customer hydraulic systems
- **Service History & Documentation**: Complete repair records and equipment service logs
- **Parts Procurement**: Automated ordering and supplier management for hydraulic components

### Analytics & Reporting

- **Business Performance Dashboards**: Track revenue, job completion rates, and technician productivity
- **Equipment Performance Analytics**: Monitor hydraulic system reliability and maintenance trends
- **Customer Insights**: Identify high-value customers and service opportunities
- **Operational Metrics**: Labor efficiency, parts utilization, and profit margin analysis

This workflow was extracted from MasterBoard's development infrastructure to help other teams implement similar preview environment automation.

## License

This project is open source and available under the terms specified in the LICENSE file.

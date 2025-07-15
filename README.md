# GitHub Actions Workflow for Prisma Postgres

**Open-source GitHub Actions workflow for automated Prisma Postgres preview environments**

This repository contains a reusable GitHub Actions workflow that automates the creation and management of feature branch databases using Prisma Postgres. Originally developed for [MasterBoard](https://masterboardapp.com) - a comprehensive business management platform that helps companies streamline their operations, track performance, and make data-driven decisions.

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

[MasterBoard](https://masterboardapp.com) is a modern business management platform that helps companies:

- Track key performance indicators and metrics
- Manage customer relationships and sales pipelines
- Automate workflows and business processes
- Generate insights through advanced analytics and reporting

This workflow was extracted from MasterBoard's development infrastructure to help other teams implement similar preview environment automation.

## License

This project is open source and available under the terms specified in the LICENSE file.

<h1 align="center">Acme Fintech Dashboard</h1>

<p align="center">
  A full-stack financial dashboard for managing invoices, customers, and revenue with Next.js App Router, Server Actions, PostgreSQL, and Auth.js.
</p>

<p align="center">
  <a href="https://nextjs.org/">
    <img src="https://img.shields.io/badge/Next.js-16.3.0-000000?style=flat-square&logo=next.js&logoColor=white" alt="Next.js">
  </a>
  <a href="https://www.typescriptlang.org/">
    <img src="https://img.shields.io/badge/TypeScript-5.7.3-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  </a>
  <a href="https://tailwindcss.com/">
    <img src="https://img.shields.io/badge/Tailwind_CSS-3.4.17-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS">
  </a>
  <a href="https://www.postgresql.org/">
    <img src="https://img.shields.io/badge/PostgreSQL-Serverless-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL">
  </a>
  <a href="https://authjs.dev/">
    <img src="https://img.shields.io/badge/Auth.js-v5-000000?style=flat-square&logo=auth0&logoColor=white" alt="Auth.js">
  </a>
  <a href="https://vercel.com/">
    <img src="https://img.shields.io/badge/Vercel-Deployment-000000?style=flat-square&logo=vercel&logoColor=white" alt="Vercel">
  </a>
</p>

---

## Overview

Acme Fintech Dashboard is a full-stack application for managing business invoices, customers, and revenue data from a single dashboard.

Users can authenticate securely, view financial metrics, search and filter records, create and update invoices, and manage customer information. Data is stored in PostgreSQL, while Server Actions handle secure server-side mutations.

The project follows the Next.js App Router architecture and focuses on practical full-stack patterns such as Server Components, Server Actions, authentication, relational data, validation, and asynchronous UI states.

---

## Features

- **Dashboard Analytics** — View revenue, invoice totals, and customer activity.
- **Invoice Management** — Create, update, delete, and track invoice records.
- **Customer Management** — Store and manage customer information.
- **Search & Pagination** — Search invoice data and navigate through paginated results.
- **Authentication** — Secure login and protected dashboard routes with Auth.js.
- **Server Actions** — Perform database mutations without building separate REST API endpoints.
- **Form Validation** — Validate submitted data with Zod before database operations.
- **Responsive UI** — Adapted for desktop and smaller screen sizes.
- **Loading & Error States** — Uses Suspense and route-level loading/error handling for smoother interactions.

---

## Tech Stack

| Category | Technology |
| :--- | :--- |
| **Framework** | Next.js 16 — App Router |
| **UI** | React 19 |
| **Language** | TypeScript |
| **Styling** | Tailwind CSS 3.4 |
| **Database** | Neon Serverless PostgreSQL |
| **Database Client** | postgres.js |
| **Authentication** | NextAuth.js v5 (Auth.js) |
| **Validation** | Zod |
| **Icons** | Heroicons |
| **Utilities** | use-debounce, next-themes |
| **Package Manager** | PNPM |
| **Deployment** | Vercel |

---

## How It Works

The application follows a simple full-stack flow:

```text
User
 │
 ▼
Next.js App Router
 │
 ├── Server Components
 │      └── Fetch dashboard and invoice data
 │
 ├── Client Components
 │      └── Handle interactive forms and UI state
 │
 ├── Server Actions
 │      └── Validate and process mutations
 │
 └── Auth.js
        └── Protect dashboard routes
              │
              ▼
        Neon PostgreSQL
```

---

For example, when a user creates an invoice:

```text
Invoice Form
     │
     ▼
Server Action
     │
     ▼
Zod Validation
     │
     ▼
PostgreSQL Mutation
     │
     ▼
Updated Dashboard
```

---

## Architecture

### Next.js App Router

The application uses Server Components for data fetching and Client Components where interactive browser behavior is required.

### Server Actions

Invoice and customer mutations are handled through Server Actions, keeping database operations on the server without requiring separate API routes.

### PostgreSQL

Relational data is stored in Neon PostgreSQL, with relationships between users, customers, and invoices.

### Authentication

Auth.js manages authentication and protects dashboard routes from unauthenticated access.

### Validation

Zod validates incoming form data before it reaches database operations.

---

## Project Structure

```text
nextjs-dashboard/
├── app/
│   ├── dashboard/
│   ├── login/
│   ├── lib/
│   └── ui/
├── public/
├── auth.config.ts
├── auth.ts
├── next.config.ts
├── package.json
└── tsconfig.json
```

---

## Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/abdul-rahman-0x/nextjs-dashboard.git
cd nextjs-dashboard
```

### 2. Install Dependencies
Ensure you have PNPM installed on your machine to build the workspace dependencies:
```bash
pnpm install
```

### 3. Configure Environment Variables
Create a `.env` file from the provided example:

```bash
cp .env.example .env
```

Open `.env` and configure your database and authentication keys:
```env
POSTGRES_URL="your-neon-postgres-url"
POSTGRES_USER="your-postgres-user"
POSTGRES_HOST="your-postgres-host"
POSTGRES_PASSWORD="your-postgres-password"
POSTGRES_DATABASE="your-postgres-database"

AUTH_SECRET="your-auth-secret"
```

### 4. Start the Development Server

```bash
pnpm dev
```
The application will be available at `http://localhost:3000`

### 5. Sign In
Use the seeded account to access the dashboard:

*   **Email:** `user@nextmail.com`
*   **Password:** `123456`

---

## Developer

Built by **[Abdul Rahman](https://github.com/abdul-rahman-0x)**



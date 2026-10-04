# Goods Management System

A modern goods and inventory management dashboard for tracking stock movements, product details, purchases, sales, suppliers, customers, and employee records.

## UI Preview

<div align="center">
  <img src="docs/images/dashboard-ui.svg" alt="Goods Management Dashboard" width="1000" />
</div>

<div align="center">
  <img src="docs/images/inventory-module.svg" alt="Inventory Management Module" width="1000" />
</div>

<div align="center">
  <img src="docs/images/business-module.svg" alt="Business Management Module" width="1000" />
</div>

## Features

- Inventory tracking with add, edit, and delete actions
- Product, supplier, customer, and employee management
- Purchase and sales record tracking
- Inventory overview with arrivals, sales, revenue, and profit totals
- CSV and Excel export support
- PostgreSQL-backed persistence with Drizzle ORM
- Module-based dashboard for operations and reporting

## Tech Stack

- Next.js 16
- React 19
- TypeScript
- PostgreSQL
- Drizzle ORM
- XLSX
- Tailwind CSS

## Project Structure

```text
goods-management-system-development/
├── src/
│   ├── app/
│   │   ├── api/
│   │   └── page.tsx
│   ├── components/
│   ├── db/
│   └── lib/
├── data/
├── docs/
│   └── images/
├── .env
├── drizzle.config.json
├── package.json
├── next.config.ts
├── tsconfig.json
└── README.md
```

## Getting Started

### 1. Install dependencies

```bash
npm install
```

### 2. Configure the database

Create or update your environment file with a PostgreSQL connection string:

```env
DATABASE_URL="postgresql://postgres:postgres@example123/app_db"
```

Make sure PostgreSQL is running locally on port 5432 and the database `app_db` exists.

### 3. Start the app

```bash
npm run dev
```

Then open:

```text
http://localhost:3000
```

## Database Notes

The project uses Drizzle with schema files in the `src/db` folder. The app automatically bootstraps tables and syncs initial data when needed.

## Export Features

- Inventory CSV export via `/api/download/csv`
- Combined Excel export via `/api/download/xlsx`

## License

This project is for educational and business management use.

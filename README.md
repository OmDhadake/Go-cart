# GoCart

GoCart is a full-stack e-commerce storefront built with Next.js, Redux, Prisma, and PostgreSQL. It supports product browsing, cart management, checkout, seller dashboards, admin management, and order tracking.

## Features

- Modern storefront with featured products, latest arrivals, and best-selling items
- Product detail pages with ratings, pricing, and add-to-cart flow
- Cart and checkout experience with address selection and coupon support
- Seller dashboard to manage products, orders, and stock status
- Admin dashboard for store and sales oversight
- Prisma-based data model for users, products, orders, addresses, ratings, coupons, and stores

## Tech Stack

- Next.js 15
- React 19
- Redux Toolkit
- Prisma ORM
- PostgreSQL
- Tailwind CSS
- Lucide Icons

## Project Structure

- app/ - routes and page-level UI for public, store, and admin views
- components/ - reusable UI components for products, orders, navbar, hero, and dashboards
- lib/ - Redux store and feature slices
- prisma/ - Prisma schema and database models

## Getting Started

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a local environment file:
   ```bash
   cp .env.example .env.local
   ```
4. Update the environment variables for your PostgreSQL database connection.
5. Run database migrations (if Prisma is set up locally):
   ```bash
   npx prisma migrate dev
   ```
6. Start the development server:
   ```bash
   npm run dev
   ```

## Environment Variables

The app uses the following public variable for currency display:

```env
NEXT_PUBLIC_CURRENCY_SYMBOL=Rs
```

You can also point the app to your database with:

```env
DATABASE_URL=your_postgresql_connection_string
DIRECT_URL=your_direct_postgresql_connection_string
```

## Notes

- The project currently uses placeholder data and UI logic in several areas, so backend integrations can be completed progressively.
- The default currency label is set to Rs for the storefront and dashboard views.

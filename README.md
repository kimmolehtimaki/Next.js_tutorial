## Next.js App Router Application

This is application built as a part of the Laurea University of Applied Sciences Fullstack course, Spring 2026. Application is completed by following tasks in Next.js 'App Router' tutorial. 
For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.

This README.md is created with the help of Github Copilot AI agent.

Application is a modern web dashboard built with Next.js 15, React, and TypeScript, showcasing best practices for building full-stack applications with the App Router, server-side rendering, and database integration.

## Application Features

- **Authentication**: Secure login with NextAuth.js
- **Dashboard Overview**: Real-time metrics and revenue charts
- **Customer Management**: Browse and manage customer records
- **Invoice Management**: Create, view, edit, and delete invoices
- **Search & Filter**: Find customers and invoices quickly
- **Responsive Design**: Mobile-first design with Tailwind CSS
- **Server-Side Rendering**: Optimized performance with Next.js SSR
- **Database Integration**: PostgreSQL

## Tech Stack

- **Framework**: Next.js 15
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **UI Components**: Heroicons
- **Authentication**: NextAuth.js
- **Database**: PostgreSQL
- **Package Manager**: pnpm

## Getting Started

### Prerequisites

- Node.js 18+ 
- pnpm or npm
- PostgreSQL database

### Installation

1. Install pnpm:
```bash
npm install -g pnpm
```

2. Set up your environment variables and database connection string:

3. (Optional) Seed the database with sample data:
-refer to Next.js tutorial for sample data

### Development

Start the development server:
```bash
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Production Build

Build for production:
```bash
pnpm build
```

Start the production server:
```bash
pnpm start
```

## Project Structure

```
nextjs-dashboard/
├── app/                      # Next.js App Router
│   ├── layout.tsx           # Root layout
│   ├── page.tsx             # Home page
│   ├── dashboard/           # Dashboard routes
│   ├── login/               # Authentication
│   ├── lib/                 # Utilities and data
│   └── ui/                  # Reusable components
├── public/                  # Static assets
├── auth.ts                  # NextAuth configuration
├── tailwind.config.ts       # Tailwind CSS config
├── tsconfig.json            # TypeScript config
└── package.json             # Dependencies
```

## Key Pages

- **Home** (`/`) - Landing page with login
- **Dashboard** (`/dashboard`) - Main dashboard overview
- **Customers** (`/dashboard/customers`) - Customer list
- **Invoices** (`/dashboard/invoices`) - Invoice management
- **Create Invoice** (`/dashboard/invoices/create`) - Create new invoice
- **Edit Invoice** (`/dashboard/invoices/[id]/edit`) - Edit existing invoice

## Authentication

The app uses NextAuth.js for secure authentication. Default login credentials can be found in tutorial, Chapter 14

## Troubleshooting

### Database Connection Issues

If you encounter database connection errors:
1. Verify your `DATABASE_URL` in `.env.local`
2. Ensure PostgreSQL is running
3. Check database credentials
4. Run migrations: `pnpm db:migrate`

### Port Already in Use

If port 3000 is already in use:
```bash
pnpm dev -- -p 3001
```

### Dependencies Issues

Clear the cache and reinstall:
```bash
rm -rf node_modules pnpm-lock.yaml
pnpm install
```

## Learning Resources

- [Next.js Documentation](https://nextjs.org/docs)
- [Next.js Learn Course](https://nextjs.org/learn)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [NextAuth.js Documentation](https://next-auth.js.org)

## License

This project is part of the Next.js Learn course and is provided as-is for educational purposes.

## Support

For issues and questions, refer to the [Next.js Discussion Forums](https://github.com/vercel/next.js/discussions) or the official documentation.

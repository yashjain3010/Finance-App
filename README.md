<a name="readme-top"></a>

# Track your income and expenses with Finance.

## :bangbang: Folder Structure

Here is the folder structure of this app.

```bash
finance-dashboard/
  |- app/
    |-- (auth)/
    |-- (dashboard)/
    |-- api/
    |-- apple-icon.png
    |-- favicon.ico
    |-- globals.css
    |-- icon1.png
    |-- icon2.png
    |-- layout.tsx
  |- components/
    |-- ui/
  |- config/
    |-- index.ts
  |- db/
    |-- drizzle.ts
    |-- schema.ts
  |- drizzle/
  |- features/
    |-- accounts/
    |-- categories/
    |-- summary/
    |-- transactions/
  |- hooks/
    |-- use-confirm.tsx
  |- lib/
    |-- hono.ts
    |-- utils.ts
  |- providers/
    |-- query-provider.tsx
    |-- sheet-provider.tsx
  |- public/
    |-- data.csv
    |-- github.svg
    |-- logo.svg
  |- scripts/
    |-- seed.ts
  |- .env.example
  |- .env.local
  |- .eslintrc.json
  |- .gitignore
  |- .prettierrc
  |- bun.lockb
  |- components.json
  |- drizzle.config.ts
  |- environment.d.ts
  |- middleware.ts
  |- next.config.mjs
  |- package-lock.json
  |- package.json
  |- postcss.config.js
  |- tailwind.config.ts
  |- tsconfig.json
```

<br />

## :toolbox: Getting Started

1. Make sure **Git** and **NodeJS** is installed.
2. Clone this repository to your local computer.
3. Create `.env.local` file in **root** directory.
4. Contents of `.env.local`:

```env
# .env.local

# disabled next.js telemetry
NEXT_TELEMETRY_DISABLED=1

# clerk auth keys
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
CLERK_PUBLISHABLE_KEY=pk_test_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
CLERK_SECRET_KEY=sk_test_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

# clerk redirect url
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up

# neon db url
DATABASE_URL=postgresql://<username>:<password>@<hostname>/<database>?sslmode=require

# app base url
NEXT_PUBLIC_APP_URL=http://localhost:3000

```

Obtain Clerk Authentication Keys

   1. **Source**: Clerk Dashboard or Settings Page
   2. **Procedure**:
      - Log in to your Clerk account.
      - Navigate to the dashboard or settings page.
      - Look for the section related to authentication keys.
      - Copy the `NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY` and `CLERK_SECRET_KEY` provided in that section.

Retrieve Neon Database URI

   1. **Source**: Database Provider (e.g., Neon, PostgreSQL)
   2. **Procedure**:
      - Access your database provider's platform or configuration.
      - Locate the database connection details.
      - Replace `<username>`, `<password>`, `<hostname>`, and `<database>` placeholders in the URI with your actual database credentials.
      - Ensure to include `?sslmode=require` at the end of the URI for SSL mode requirement.

Specify Public App URL

   1. **Procedure**:
      - Replace `http://localhost:3000` with the URL of your deployed application.

Save and Secure:

   - Save the changes to the `.env.local` file.

Install Project Dependencies using `npm install --legacy-peer-deps` or `yarn install --legacy-peer-deps`.
 
 
 Migrate database:

In terminal, run `npm run db:generate` to generate database client and `npm run db:migrate` to make sure that your database is up-to-date along with schema.

Run the Seed Script:

In the same terminal, run the following command to execute the seed script:

```bash
npm run db:seed
```

This command uses `npm` to execute the Typescript file (`scripts/seed.ts`) and writes transaction data in database.

Verify Data in Database:

Once the script completes, check your database to ensure that the transaction data has been successfully seeded.

Now app is fully configured 👍 and you can start using this app using either one of `npm run dev` or `yarn dev`.

**NOTE:** Please make sure to keep your API keys and configuration values secure and do not expose them publicly.

## :gear: Tech Stack

[![React JS](https://skillicons.dev/icons?i=react "React JS")](https://react.dev/ "React JS") [![Next JS](https://skillicons.dev/icons?i=next "Next JS")](https://nextjs.org/ "Next JS") [![Typescript](https://skillicons.dev/icons?i=ts "Typescript")](https://www.typescriptlang.org/ "Typescript") [![Tailwind CSS](https://skillicons.dev/icons?i=tailwind "Tailwind CSS")](https://tailwindcss.com/ "Tailwind CSS") [![Vercel](https://skillicons.dev/icons?i=vercel "Vercel")](https://vercel.app/ "Vercel") [![Postgresql](https://skillicons.dev/icons?i=postgres "Postgresql")](https://www.postgresql.org/ "Postgresql")

## :raised_hands: Contribute

You might encounter some bugs while using this app. You are more than welcome to contribute. Just submit changes via pull request and I will review them before merging. Make sure you follow community guidelines.

## :gem: Acknowledgements

Useful resources and dependencies that are used in Finance.

- [@clerk/backend](https://www.npmjs.com/package/@clerk/backend): ^1.1.3
- [@clerk/nextjs](https://www.npmjs.com/package/@clerk/nextjs): ^5.0.8
- [@hono/clerk-auth](https://www.npmjs.com/package/@hono/clerk-auth): ^2.0.0
- [@hono/zod-validator](https://www.npmjs.com/package/@hono/zod-validator): ^0.2.1
- [@hookform/resolvers](https://www.npmjs.com/package/@hookform/resolvers): ^3.3.4
- [@neondatabase/serverless](https://www.npmjs.com/package/@neondatabase/serverless): ^0.9.3
- [@paralleldrive/cuid2](https://www.npmjs.com/package/@paralleldrive/cuid2): ^2.2.2
- [@radix-ui/react-checkbox](https://www.npmjs.com/package/@radix-ui/react-checkbox): ^1.0.4
- [@radix-ui/react-dialog](https://www.npmjs.com/package/@radix-ui/react-dialog): ^1.0.5
- [@radix-ui/react-dropdown-menu](https://www.npmjs.com/package/@radix-ui/react-dropdown-menu): ^2.0.6
- [@radix-ui/react-label](https://www.npmjs.com/package/@radix-ui/react-label): ^2.0.2
- [@radix-ui/react-popover](https://www.npmjs.com/package/@radix-ui/react-popover): ^1.0.7
- [@radix-ui/react-select](https://www.npmjs.com/package/@radix-ui/react-select): ^2.0.0
- [@radix-ui/react-separator](https://www.npmjs.com/package/@radix-ui/react-separator): ^1.0.3
- [@radix-ui/react-slot](https://www.npmjs.com/package/@radix-ui/react-slot): ^1.0.2
- [@radix-ui/react-tooltip](https://www.npmjs.com/package/@radix-ui/react-tooltip): ^1.0.7
- [@tanstack/react-query](https://www.npmjs.com/package/@tanstack/react-query): ^5.35.5
- [@tanstack/react-table](https://www.npmjs.com/package/@tanstack/react-table): ^8.16.0
- [class-variance-authority](https://www.npmjs.com/package/class-variance-authority): ^0.7.0
- [clsx](https://www.npmjs.com/package/clsx): ^2.1.1
- [date-fns](https://www.npmjs.com/package/date-fns): ^3.6.0
- [drizzle-orm](https://www.npmjs.com/package/drizzle-orm): ^0.30.10
- [drizzle-zod](https://www.npmjs.com/package/drizzle-zod): ^0.5.1
- [hono](https://www.npmjs.com/package/hono): ^4.3.4
- [lucide-react](https://www.npmjs.com/package/lucide-react): ^0.378.0
- [next](https://www.npmjs.com/package/next): 14.2.3
- [next-themes](https://www.npmjs.com/package/next-themes): ^0.3.0
- [query-string](https://www.npmjs.com/package/query-string): ^9.0.0
- [react](https://www.npmjs.com/package/react): ^18
- [react-countup](https://www.npmjs.com/package/react-countup): ^6.5.3
- [react-currency-input-field](https://www.npmjs.com/package/react-currency-input-field): ^3.8.0
- [react-day-picker](https://www.npmjs.com/package/react-day-picker): ^8.10.1
- [react-dom](https://www.npmjs.com/package/react-dom): ^18
- [react-hook-form](https://www.npmjs.com/package/react-hook-form): ^7.51.4
- [react-icons](https://www.npmjs.com/package/react-icons): ^5.2.1
- [react-papaparse](https://www.npmjs.com/package/react-papaparse): ^4.4.0
- [react-select](https://www.npmjs.com/package/react-select): ^5.8.0
- [react-use](https://www.npmjs.com/package/react-use): ^17.5.0
- [recharts](https://www.npmjs.com/package/recharts): ^2.12.7
- [sonner](https://www.npmjs.com/package/sonner): ^1.4.41
- [tailwind-merge](https://www.npmjs.com/package/tailwind-merge): ^2.3.0
- [tailwindcss-animate](https://www.npmjs.com/package/tailwindcss-animate): ^1.0.7
- [zod](https://www.npmjs.com/package/zod): ^3.23.8
- [zustand](https://www.npmjs.com/package/zustand): ^4.5.2
- [@types/node](https://www.npmjs.com/package/@types/node): ^20
- [@types/react](https://www.npmjs.com/package/@types/react): ^18
- [@types/react-dom](https://www.npmjs.com/package/@types/react-dom): ^18
- [dotenv](https://www.npmjs.com/package/dotenv): ^16.4.5
- [drizzle-kit](https://www.npmjs.com/package/drizzle-kit): ^0.21.2
- [eslint](https://www.npmjs.com/package/eslint): ^8
- [eslint-config-next](https://www.npmjs.com/package/eslint-config-next): 14.2.3
- [eslint-plugin-unused-imports](https://www.npmjs.com/package/eslint-plugin-unused-imports): ^3.2.0
- [pg](https://www.npmjs.com/package/pg): ^8.11.5
- [postcss](https://www.npmjs.com/package/postcss): ^8
- [prettier](https://www.npmjs.com/package/prettier): ^3.2.5
- [prettier-plugin-tailwindcss](https://www.npmjs.com/package/prettier-plugin-tailwindcss): ^0.5.14
- [tailwindcss](https://www.npmjs.com/package/tailwindcss): ^3.4.1
- [typescript](https://www.npmjs.com/package/typescript): ^5

## :books: Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## :page_with_curl: Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

## :star: Give A Star

You can also give this repository a star to show more people and they can use this repository.

# Finance-App

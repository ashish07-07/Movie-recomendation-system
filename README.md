This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.


Use of Next-Auth for singin with google
![nextauth](nextauth.png)

Setting Up Prisma
Follow these steps to set up Prisma in your project:

1. Install Prisma
Install Prisma via npm:

npm install prisma

2. Initialize Prisma Schema
Initialize the Prisma schema:
npx prisma init

3. Create a Simple User Schema
Define a simple user model in your Prisma schema file (prisma/schema.prisma):
model User {
  id        Int     @id @default(autoincrement())
  username  String  @unique
  password  String
}

4. Replace .env with Your Own Postgres URL
Update the .env file with your PostgreSQL database URL:

DATABASE_URL="postgresql://johndoe:randompassword@localhost:5432/mydb?schema=public"

5. Migrate the Database
Apply the database migrations:

npx prisma migrate dev --name init_schema

6. Generate the Client
Generate the Prisma client:
npx prisma generate










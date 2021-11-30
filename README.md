## Introduction

A personal boilerplate based on Next.js.

features：Next.js, TypeScript, GraphQL, Prisma, Tailwind CSS

## How do I build

I built this boilerplate in the following order.

- [Next.js](https://nextjs.org/docs/basic-features/typescript): start with typescipt version create-next-app
- [TypeScript](https://github.com/vercel/next.js/tree/canary/examples/with-typescript): follow the typescript writing style for this simple example
- [ESLint + Prettier](https://paulintrognon.fr/blog/typescript-prettier-eslint-next-js): ESLint and Prettier with VSCode integration
- [Tailwind CSS](https://tailwindcss.com/docs/guides/nextjs): setting up Tailwind CSS in a Next.js project
- [GraphQL (client)](https://www.apollographql.com/blog/apollo-client/next-js/next-js-getting-started/): use Apollo Client in Next.js
- [GraphQL (server)](https://github.com/vercel/next.js/blob/canary/examples/api-routes-graphql/pages/api/graphql.js): use Apollo Server in Next.js
- [Prisma (basic)](https://www.prisma.io/blog/fullstack-nextjs-graphql-prisma-oklidw1rhw#add-prisma-to-your-project): basic setup (e.g. schema, migrating, seeding)
- [Prisma (GraphQL)](https://www.prisma.io/blog/fullstack-nextjs-graphql-prisma-2-fwpc6ds155#initialize-prisma-client): prisma with GraphQL integration based on Nexus

## Getting started

Before getting start, please make sure you have created an empty database (e.g. PostgreSQL). Then, rename `.env.example` to `.env` and edit the environment variable. This will enable Prisma database connection, and the GraphQL communicate between client and server.

1. Install npm dependencies

```
npm install
```

2. Create and seed the database

```
npx prisma migrate dev --name init
```

3. Seed the database with the sample data in `prisma/seed.ts`

```
npx prisma db seed
```

4. Start the app

```
npm run dev
```

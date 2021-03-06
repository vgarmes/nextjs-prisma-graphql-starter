`yarn add next-auth @prisma/client @next-auth/prisma-adapter`
`yarn add prisma --dev`

`createdb [DATABASE_NAME]`

`npx prisma init`

Configure your NextAuth.js to use the Prisma Adapter(`pages/api/auth/[...nextauth].ts`)

Create Prisma schema (prisma/schema.prisma)

Create SQL migration file and execute it:
`npx prisma migrate dev`

# Useful Prisma commands

`npx prisma db push`: useful for schema prototyping, where the goal is to synchronize a new schema with a development database. As your schema evolves, you will want to create and maintain a migration history, to do that you will use Prisma migrate (next command)
`npx prisma migrate dev`: create and apply migrations

# Issues

[NexusGraphQLSchema is no longer a GraphQLSchema with nexus@1.2.0](https://github.com/graphql-nexus/nexus/issues/1019): GraphQL 16 will produce type errors when using schema generated by Nexus

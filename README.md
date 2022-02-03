# Postgres docker + Prisma

Use this docker-compose as a simple way to have a containerized postgres instance (so you don't need to configure anything):

## Installation

- Requirements: docker

- Copy the `docker-compose.yml` file to your project

- Store the following URL in an ENV variable

```
DATABASE_URL="postgresql://user:password@localhost:8432/development_db?schema=public"
```

- Copy the `datasource db` config from the `prisma/schema.prisma` file to your prisma schema, so it uses the `DATABASE_URL` variable as the prisma db source, or just hardcode it :)

```
datasource db {
  provider = "postgresql"
  url      = env("DATABASE_URL")
}
```

- Run `> docker-compose up` in your terminal to start the service.

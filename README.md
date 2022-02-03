# Postgres docker + Prisma

Use this docker-compose as a simple way to have a containerized postgres instance (so you don't need to configure anything):

## Installation

- Copy the `docker-compose.yml` file to your project

- Store the following URL in an ENV variable

```
DATABASE_URL="postgresql://user:password@localhost:8432/development_db?schema=public"
```

- Use `DATABASE_URL` variable as the prisma db source, or just hardcode it :)

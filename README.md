# Express + MongoDB API template (object-oriented style)

A TypeScript starter for Express APIs organized around classes, with real-time support built in.

## What is included

- **Server setup class:** security, standard, route, error-handling and Socket.IO setup each in their own method
- **Security middleware:** helmet, hpp, CORS, cookie sessions and compression
- **Real time:** Socket.IO with the Redis adapter, so events reach clients across several server instances
- **Errors:** a global error handler with typed error classes (bad request, not found, not authorized, server error) and HTTP status codes; async route errors are caught with `express-async-errors`
- **Logging:** bunyan
- **Tooling:** ESLint, Prettier, path aliases via `tsconfig-paths`, nodemon for development

## Structure

```
src/
  app.ts            entry point
  setupServer.ts    middleware, routes, error handling, sockets
  setupDatabase.ts  mongoose connection
  routes.ts         route registration
  config.ts         environment config with a `validateConfig` check
  shared/globals/helpers/error-handler.ts
```

## Run

```bash
cp .env.example .env   # fill in the values
npm install
npm run dev
```

Needs MongoDB and Redis running locally.

See also the [functional version](https://github.com/minhnguyen99x/MTD__project-template__express-mongo-fp) of this template.

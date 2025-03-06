# Build
FROM node:23.9-bookworm-slim AS build
WORKDIR /app
COPY ./package.json ./
COPY ./pnpm-lock.yaml ./
RUN corepack enable
RUN pnpm i --frozen-lockfile
COPY . .
RUN pnpm build

# Production Dependencies
FROM node:23.9-bookworm-slim AS dependencies
WORKDIR /app
COPY ./package.json ./
COPY ./pnpm-lock.yaml ./
RUN corepack enable
RUN pnpm i --production --frozen-lockfile

# Runtime
FROM node:23.9-bookworm-slim AS runtime
USER node:node
WORKDIR /app
COPY --from=dependencies --chown=node:node /app/node_modules ./node_modules
COPY --from=build --chown=node:node /app/package.json /app/build ./
EXPOSE 3000
CMD ["node", "index.js"]
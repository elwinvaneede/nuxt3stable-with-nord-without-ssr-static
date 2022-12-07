# Nuxt 3 with Nord without SSR (static deployment)

POC for [Nuxt 3 stable](https://nuxt.com/) together with Nord using client-side rendering (CSR) and deployed on static hosting.

Integrated [vue-i18n](https://vue-i18n.intlify.dev/) through a plugin since the Nuxt 3 module is still under development.
Linked it with `useHead()` to set the correct `lang` and `dir` attributes on the `<html>` element.

## Setup

Make sure to install the dependencies:

```bash
# yarn
yarn install

# npm
npm install

# pnpm
pnpm install --shamefully-hoist
```

## Development Server

Start the development server on http://localhost:3000

```bash
npm run dev
```

## Production

Build the application for production:

```bash
npm run generate
```

Locally preview production build:

```bash
npm run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.

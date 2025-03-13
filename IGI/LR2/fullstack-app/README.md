# Turbo Monorepo for Nodejs and React full stack app

**Hi 🖐**this is full stack app version 2.0, check out the previous repo 👉 [Form Hub](https://github.com/yanliu1111/docker-fullstackapp-react-nodejs-postgres), which used docker to run the frontend and backend in two separate repo. This repo is using [Turborepo](https://turbo-monorepo.vercel.app/) to run the frontend and backend in one repo. The docker setup is still there, but restructured the whole app to use turborepo.

Fun fact, turborepo is created by the same person who created [Nextjs](https://nextjs.org/).

## 📎 Run the app

Install the required dependencies with `yarn install` in the `root` folder, `frondend` folder and `backend` folder.

Go to the root folder, run `yarn dev` and `docker-compose up` to start the app.

## 📕 Learning Notes:

1. When you move the backend and frontend to monorepo, the first two things: 1 delete git root and node_modules, 2 change the package name in package.json.
2. Turbo setting for frontend, we only want to build and run the things we required for frontend.

```json
    "build": "turbo run build --filter=frontend",
    "dev": "turbo run dev --filter=frontend --parallel",
```

## 📝 Summary for app stucture

Very exciting, this monorepo full stack app is working with many new features, I would like to summarize their functions for this app and build whole app structure for better understanding.

<img 
    style="display: block; 
           margin-left: auto;
           margin-right: auto;"
    src="roadmap.jpg" 
    alt="roadmap">
</img> <br>

## ❓ Issues：

There is alter in Github "Your repository has dependencies with security vulnerabilities." I think it is because of the turborepo, I will continue to troubleshoot this issues. 👩‍🔧

Update: the dependencies issues is fixed, have fun dependabot[bot] helped me update everything antomatically. GitHub is an amazing playground 🚀

💖 Hope this repo can help you to understand how to use turborepo to build a full stack app.

## 📚 Resources:

**The following is from the original Turborepo introduction**

## Turborepo starter

This is an official Yarn v1 starter turborepo.

## What's inside?

This turborepo uses [Yarn](https://classic.yarnpkg.com/) as a package manager. It includes the following packages/apps:

### Apps and Packages

- `docs`: a [Next.js](https://nextjs.org) app
- `web`: another [Next.js](https://nextjs.org) app
- `ui`: a stub React component library shared by both `web` and `docs` applications
- `eslint-config-custom`: `eslint` configurations (includes `eslint-config-next` and `eslint-config-prettier`)
- `tsconfig`: `tsconfig.json`s used throughout the monorepo

Each package/app is 100% [TypeScript](https://www.typescriptlang.org/).

### Utilities

This turborepo has some additional tools already setup for you:

- [TypeScript](https://www.typescriptlang.org/) for static type checking
- [ESLint](https://eslint.org/) for code linting
- [Prettier](https://prettier.io) for code formatting

### Build

To build all apps and packages, run the following command:

```
cd my-turborepo
yarn run build
```

### Develop

To develop all apps and packages, run the following command:

```
cd my-turborepo
yarn run dev
```

### Remote Caching

Turborepo can use a technique known as [Remote Caching](https://turborepo.org/docs/core-concepts/remote-caching) to share cache artifacts across machines, enabling you to share build caches with your team and CI/CD pipelines.

By default, Turborepo will cache locally. To enable Remote Caching you will need an account with Vercel. If you don't have an account you can [create one](https://vercel.com/signup), then enter the following commands:

```
cd my-turborepo
npx turbo login
```

This will authenticate the Turborepo CLI with your [Vercel account](https://vercel.com/docs/concepts/personal-accounts/overview).

Next, you can link your Turborepo to your Remote Cache by running the following command from the root of your turborepo:

```
npx turbo link
```

## Useful Links

Learn more about the power of Turborepo:

- [Pipelines](https://turborepo.org/docs/core-concepts/pipelines)
- [Caching](https://turborepo.org/docs/core-concepts/caching)
- [Remote Caching](https://turborepo.org/docs/core-concepts/remote-caching)
- [Scoped Tasks](https://turborepo.org/docs/core-concepts/scopes)
- [Configuration Options](https://turborepo.org/docs/reference/configuration)
- [CLI Usage](https://turborepo.org/docs/reference/command-line-reference)

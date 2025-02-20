---
title: FAQ
description: Frequently asked questions about Create T3 App
layout: ../../layouts/docs.astro
lang: en
---

Here are some commonly asked questions about Create T3 App.

## What's next? How do I make an app with this?

We try to keep this project as simple as possible, so you can start with just the scaffolding we set up for you, and add additional things later when they become necessary.

If you are not familiar with the different technologies used in this project, please refer to the respective docs. If you still are in the wind, please join our [Discord](https://t3.gg/discord) and ask for help.

- [Next.js](https://nextjs.org/)
- [NextAuth.js](https://next-auth.js.org)
- [Prisma](https://prisma.io)
- [Tailwind CSS](https://tailwindcss.com)
- [tRPC](https://trpc.io)

## What learning resources are currently available?

Although the resources listed below are some of the best that exist for the T3 Stack, the community (and [Theo](https://youtu.be/rzwaaWH0ksk?t=1436)) recommend that you just start using the stack and learn along the way by building with it.

If you are considering Create T3 App, chances are you might have already used some of the parts of the stack. So why not just dive in head first and learn the other parts while you build something?

Now, we realize this path doesn't work for everyone. So, if you feel like you've tried the recommendation and would still like some resources, or you just aren't confident doing it by yourself and/or feel overwhelmed by the stack, checkout these awesome tutorials on Create T3 App:

### Articles

- [Build a full stack app with Create T3 App](https://www.nexxel.dev/blog/ct3a-guestbook)
- [A first look at Create T3 App](https://dev.to/ajcwebdev/a-first-look-at-create-t3-app-1i8f)
- [Migrating your T3 App into a Turborepo](https://www.jumr.dev/blog/t3-turbo)
- [Integrating Stripe into your T3 App](https://blog.nickramkissoon.com/posts/integrate-stripe-t3)

### Videos

- [T3 Stack Tutorial - FROM 0 TO PROD FOR $0 (Next.js, tRPC, TypeScript, Tailwind, Prisma & More)](https://www.youtube.com/watch?v=YkOSUVzOAA4) **(recommended)**
- [Jack Herrington - Build a Note Taking app with the T3 Stack](https://www.youtube.com/watch?v=J1gzN1SAhyM)
- [Build a Twitter Clone with the T3 Stack - tRPC, Next.js, Prisma, Tailwind & Zod](https://www.youtube.com/watch?v=nzJsYJPCc80)
- [Build a Blog With the T3 Stack - tRPC, TypeScript, Next.js, Prisma & Zod](https://www.youtube.com/watch?v=syEWlxVFUrY)
- [Build a Live Chat Application with the T3 Stack - TypeScript, Tailwind, tRPC](https://www.youtube.com/watch?v=dXRRY37MPuk)
- [The T3 Stack - How We Built It](https://www.youtube.com/watch?v=H-FXwnEjSsI)
- [An overview of the Create T3 App (Next, Typescript, Tailwind, tRPC, Next-Auth)](https://www.youtube.com/watch?v=VJH8dsPtbeU)

## Why are there `.js` files in the project?

As per [T3-Axiom #3](/en/introduction#typesafety-isnt-optional), we take typesafety as a first class citizen. Unfortunately, not all frameworks and plugins support TypeScript which means some of the configuration files have to be `.js` files.

We try to emphasize that these files are JavaScript for a reason, by explicitly declaring each file's type (`cjs` or `mjs`) depending on what's supported by the library it is used by. Also, all the `js` files in this project are still typechecked using a checkJs option in the compiler (tsconfig).

## I'm struggling to add i18n to my app. Is there any reference I can use?

We have decided against including i18n by default in `create-t3-app` because it's a very opinionated topic and there are many ways to implement it.

However, if you struggle to implement it and want to see a reference project, we have a [reference repo](https://github.com/juliusmarminge/t3-i18n) that shows how you can add i18n to a T3 App using [next-i18next](https://github.com/i18next/next-i18next).

## Why are we using `/pages` and not `/app` from Next.js 13?

As per [T3-Axiom #2](/en/introduction#bleed-responsibly), we love bleeding edge stuff but value stability, your entire router is hard to port, [not a great place to bleed](https://youtu.be/mnwUbtieOuI?t=1662). While `/app` is [a glimpse into the future](https://youtu.be/rnsC-12PVlM?t=818), it's not ready for production; The API is in beta and expected to have breaking changes.

For a list of supported, planned, and worked on features in the `/app` dir, visit the [beta Next.js docs](https://beta.nextjs.org/docs/app-directory-roadmap#supported-and-planned-features).

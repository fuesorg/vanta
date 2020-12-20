<h1 align="center">
  Vanta
</h1>

<p align="center">
  <a href="https://vercel.com/dashboard/fues/projects" target="_blank">
    <img src="https://assets.vercel.com/image/upload/front/favicon/round-2/144x144.png" height="24px" alt="vercel badge">
  </a>
  &nbsp;
  <a href="https://github.com/fuesorg/nextburger/blob/master/LICENSE">
    <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="nextburger: This project is released under the MIT license." />
  </a>
  <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" alt="PRs welcome!" />
</p>

> Vanta is a free Nuxt template that gives you an easy way to start a blog + store that uses modern technologies like Stripe, static-site JAMstack architecture, CSS grid layout, responsive design, and fuzzy search — based on the Bael brutalist aesthetic.

## Quickstart

Vanta runs using [Stripe](https://stripe.com), [Nuxt.js](https://nuxtjs.org), [Vue.js](https://vuejs.org), and deployed with [Vercel](https://vercel.com).

## Deploy with Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/git/external?repository-url=https%3A%2F%2Fgithub.com%2Fvercel%2Fnext.js%2Ftree%2Fcanary%2Fexamples%2Fhello-world)


## Build Setup

``` bash
# install dependencies
$ npm install # Or yarn install

# serve with hot reload at localhost:3000
$ npm run dev # Or yarn dev

# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```

## Edit content

Access `yourwebsite.com/admin`, e.g. `localhost:3000/admin`.

## Manage dynamic routes

When you use Netlify CMS' `folder` type, you actually create dynamic routes. For example, when creating a blog,
you render different content files with the same template. And for the blog to know which content to render,
it looks at the url and gets the specific content file. That's a dynamic route.

So If you create a `folder` type with Netlify CMS, add the folder as glob to the `dynamicRoutes` variable
in the `nuxt.config.js`.

MIT License


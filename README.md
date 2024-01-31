# Next.js / Sanity Website engine

<!-- Deploy button -->

[![Deploy with Vercel](https://vercel.com/button)][vercel-deploy]

<!-- Variables -->

[vercel-deploy]: https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FAratramba%2Fnextjs-sanity-website-engine&project-name=https%3A%2F%2Fgithub.com%2FAratramba%2Fnextjs-marketing-website&repository-name=https%3A%2F%2Fgithub.com%2FAratramba%2Fnextjs-marketing-website&demo-title=Nextjs+marketing+website&demo-description=quickly+spin+up+a+marketing+website+with+blocks%2C+presets+and+various+page+types&demo-url=https%3A%2F%2Fnextjs-sanity-website-engine.vercel.app&demo-image=https%3A%2F%2Fcdn.sanity.io%2Fimages%2Fundefined%2Fundefined%2F44130bebbd7f097a2152100aca4882586ae295e0-1200x750.jpg&integration-ids=oac_hb2LITYajhRQ0i4QznmKH7gx&external-id=%3Btemplate%3Dnextjs-sanity-website-engine

> At Mawla Digital agency we used to use this package to rapidly spin up new websites. It helped us reduce 70% of the boilerplate website code. We no longer use it internally, but there's still lots that can be learned from it. This package isn't actively maintained anymore.

This package is a website engine built with Next.js and Sanity meant for rapid marketing website development. It uses Tailwind for styling and Storybook for component development. It can easily be deployed on Vercel. It features a CLI to create pages and blocks and a CLI to create a new project.

Most of the configuration is stored in the CMS, like navigation, footer, favicons, theming, social media links, etc. This way the client can easily change the content of the website without having to touch the code.

## Get started

- `yarn` installs dependencies
- `yarn dev` runs next.js
- `yarn cms` runs sanity
- `yarn storybook` runs storybook
- `yarn test` runs tests

- `yarn create-page` runs the cli to add a page
- `yarn create-block` runs the cli to create a block

## Environment variables

```
NEXT_PUBLIC_SANITY_PROJECT_ID="xxx" # sanity project id
SANITY_STUDIO_API_PROJECT_ID="xxx" # sanity project id
NEXT_PUBLIC_SANITY_DATASET="production" # sanity dataset
SANITY_STUDIO_API_DATASET="production" # sanity dataset
SANITY_PREVIEW_SECRET="xxx" # random string
SANITY_WEBHOOK_SECRET="xxx" # random string
SANITY_STUDIO_PROJECT_PATH="http://localhost:3000/" # make this / on Vercel
SANITY_API_WRITE_TOKEN="xxx" # sanity api write token
SANITY_API_READ_TOKEN="xxx" # sanity api read token
process.env.NEXT_MAX_FUNCTION_DURATION=10 # set this to 60+ if not Vercel Hobby plan
```

## Stack

The Engine is built using these technologies:

- [Next.js](https://nextjs.org/) (Page router) Frontend
- [Sanity.io](https://www.sanity.io/) CMS
- [GROQ](https://www.sanity.io/docs/overview-groq) Query Language
- [Storybook](https://storybook.js.org/) Static block development
- [Typescript](https://www.typescriptlang.org/) Javascript Type Checking
- [TailwindCSS](https://tailwindcss.com/) Interface styling

Both the frontend app and the Sanity Studio are hosted on the same domain on Vercel.

### Features

- storybook
- live cms preview
- sanity copy paste blocks between pages
- nested page structure in cms
- automatic routing
- verified internal linking
- sanity change block types
- sanity block presets
- sanity block json editor
- landing pages
- blogs, press releases, etc
- pricing
- faq
- testimonials
- redirects
- scripts injection
- navigation
- footer
- favicons from cms
- theming from cms
- social media links from cms
- cli to create pages
- cli to create blocks
- cli to create presets
- automatic sitemap.xml
- 15 base building blocks
- endless block combinations
- automatic opengraph image
- algolia index
- …

## CLI

The CLI is what speeds up all of the development work. Using the CLI you can add new blocks and page types without doing any coding. Once the initial setup is done you can confidently start styling and adding logic.

## Sitemap

Routes are at the core of the engine. The engines uses one catch all slug for all routes. All routes are directly resolved in the page query.

## Next.js

While Next.js is used as a framework, there is not much specific Next.js knowledge needed to get a project off the ground. Because we use a single catch all slug next.js page for all routes, there is no need to get into the page rendering logic unless you really want to.

## Live Previews

- Every page can be previewed before it's published.

### Conventions

- Schema names are prefixed with their type: 'page._', 'block._', 'preset.\_'.
- Article names are the single form of the type: 'page.blog', 'page.pressrelease'.
- Overview names are the plural form of the type: `page.blogs`, 'page.pressreleases'.
- Block names are given numbers. As purposes changed too often we decided to go with generic numbers rather than actual names. This way we can easily change the purpose of a block without having to change the name. The number is the order in which the block was created. The first block is `block1`, the second `block2` and so on.

## Sites using this engine

- https://allsorter.com
- https://panoramix.vercel.app
- https://saasgrowthwebsites.com
- https://sgw-template-saas-1.vercel.app
- https://gilleducation.com
- https://frescocooks.com

![image](https://github.com/Aratramba/nextjs-sanity-website-engine/assets/580312/a9e88eb9-3301-404c-9432-c385b76261c5)
![image](https://github.com/Aratramba/nextjs-sanity-website-engine/assets/580312/53be7c93-1a8e-4919-9fef-dc1e5edbaf1e)
![1-website3](https://github.com/Aratramba/nextjs-sanity-website-engine/assets/580312/e2c15b5d-4120-4cc5-a138-f57778820600)
![1-website4](https://github.com/Aratramba/nextjs-sanity-website-engine/assets/580312/b272161b-60de-4d14-9ca3-730c830f3771)
![1-website5](https://github.com/Aratramba/nextjs-sanity-website-engine/assets/580312/4755e553-16a4-4e4f-8a86-3e81f339029f)
![1-website6](https://github.com/Aratramba/nextjs-sanity-website-engine/assets/580312/f765dbf1-fed9-4fad-91e9-f4f559ef304f)
![1-website7](https://github.com/Aratramba/nextjs-sanity-website-engine/assets/580312/b9663034-480d-4a1d-a421-4999c32160eb)
![1-website8](https://github.com/Aratramba/nextjs-sanity-website-engine/assets/580312/ac8b2197-e968-4d3b-aad2-d045d52a3435)
![1-website9](https://github.com/Aratramba/nextjs-sanity-website-engine/assets/580312/1c124d67-7df5-483c-8544-d1da76810afa)

https://github.com/Aratramba/nextjs-sanity-website-engine/assets/580312/4cfc2df5-7f62-480e-bdf4-52f5bf7a482d

https://github.com/Aratramba/nextjs-sanity-website-engine/assets/580312/3d2a9684-5e73-4a35-8217-caf61f18b4f5

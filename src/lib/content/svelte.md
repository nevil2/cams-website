
# Learning SVELTE

Main website for Svelte: https://svelte.dev/

and for SvelteKit: https://kit.svelte.dev/

They have excellent tutorial: https://learn.svelte.dev/tutorial/welcome-to-svelte

It might be easier to learn Svelte first, and then the additional functionality provided by SvelteKit.


## Create Svelte App

A Svelte app (without SvelteKit) can be created with Vite.

This will create an SPA (Single Page App) which is rendered in the browser.

`npm create vite@latest svelte-demo`

choose:
 - Svelte
 - Javascript

`cd svelte-demo` to go to directory  
`npm install` to install software  
`code .` to open VS Code (editor)  
`npm run dev` to run locally in development mode


**To build:**

`npm run build`

This puts the build in the **dist** folder

**To deploy on Netlify**

Drag **dist** folder into upload box on Netlify.

This site is built with vite, svelte and svelte-navigator (for page navigation).


## Create SvelteKit App

SvelteKit is a meta framework around Svelte which enables:
- routing (i.e. different web pages based on directory structure)
- choice of deployment (full stack, static, client-side, server-side, pre-rendering during build, hybrid rendering, etc)
- deployment mode will depend on cloud provider and adapter chosen, as well as code configuration.

`npm create svelte@latest sveltekit-demo`

choose:
 - SvelteKit demo app
 - JavaScript with JSDoc comments
 - None

`cd sveltekit-demo` to go to directory  
`npm install` to install software  
`code .` to open VS Code (editor)  
`npm run dev` to run locally in development mode

**To deploy on Netlify**

`git init && git add -A && git commit -m "Initial commit`

Go to GitHub or GitLab and create a new repository.
Follow instructions to link and push.

Go to Netlify.  Choose new site, deployed from GitHUb/GitLab.  Follow instructions / process.

Site will be rebuilt on Netlify whenever new code is push to Git repository.


## Useful Libraries

### [Svelte-Query](https://sveltequery.vercel.app/overview)

Where page data is collected on demand from an API, requests may be repeated each time the page renders, and each time one returns to a page.

Svelte-Query enables requests to be cached, minimising network requests.

### [Marked](https://marked.js.org/)

If some page content is html or markdown, Marked can be used to render it correctly.

### [Leaflet](https://leafletjs.com/)

This is main library used to render maps (other than the Google Maps) in webpages.

### [TailwindCSS](https://tailwindcss.com/)

This enables CSS to be written inline in short-hand as a series of classes.


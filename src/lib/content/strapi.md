<base target="_blank">

### Strapi CMS

[![alt h](strapi-logo.svg)](https://strapi.io/) is the leading open-source, NodeJS, headless Content Management System (CMS): 

 -	Software package with an admin panel for adding, updating and deleting content
 -	Allows different users of admin panel to have different rights
 -	Provide API endpoints for front-end applications to collect content
 -  Allows authenticated member login
 -	Control access of different users (public, club member, specific club officers) to content
 -	Allows customisation of the API where necessary
 -	Can be configured to work with different databases / image stores
 -	Free for self-hosting.  (There is some modest hosting costs).


### Custom Servers

The websites can interact direct with other Club servers for New Routes, Munros, Himalayan Index, etc, enabling additional functionality to be integrated inot the website.


### Server-side Pre-rendering & Client-side On-demand Rendering

SvelteKit enables:
- Cloudflare to prerender the main pages at build time, enabling fast and efficient loading
- The user's browser to collect and render 'occasional' public content direct from Strapi
- Member only content to be collected from and rendered by the browser direct from Strapi only after the member has logged in


Other pages describe the [technology](/tech) used and method of [deployment](/deploy).
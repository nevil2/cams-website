<base target="_blank">

| Functionality    | SMC | PC | CC | AC | FRCC |
| --------------- | --- | -- | -- | -- | ---- |
| Contact forms   | ✓   | ✓ | ✓  | ✓  | ✓   |
| Membership      | ✓   | ✓ | ✓  | ✓  | ✓   |
| Applications    |    | ✓ | ✓  | ✓  | ✓   |
| Hut Booking     |    | ✓ | ✓  |   | ✓   |
| Bunk Room       |    |  |   | ✓  |    |
| Meets Management  |    | ✓ | ✓  | ✓  | ✓   |
| Lectures & Exhibitions  |    | ✓ | ✓  | ✓  | ✓   |
| Guidebook Shop            |    |    | ✓  |   | ?   |
| General Shop            |    |    |   | ✓  |    |
| Forums          |    | ✓ | ✓  |   | ?   |
| Keys & KeyFobs            |    |    | ✓  |   | ?   |
| Create/send Newsletters |    |   |  ✓  | ✓  |     |
| Member to member Emails   |    |   |    | ✓  |     |
| Stripe payments |    | ✓ | ✓  | ✓  | ✓   |
| GoCardless direct debits |    | ✓ | ✓  | ✓  |    |
| Interbacs direct debits |    |   |    |    |  ✓  |
 


[![image alt N](SMCwebsitehome.jpg)](https://smc.org.uk)
[![image alt N](Pinnacle_Club.jpg)](https://pinnacleclub.co.uk)

Websites are being built for individual clubs with [![alt h](svelte-logo.svg)](https://svelte.dev/) **Svelte** / [![alt h](svelte-kit-logo.svg)](https://kit.svelte.dev/)
using [![alt h](strapi-logo.svg)](https://strapi.io/) CMS (content management system).

These websites can include systems for:
 - club membership
 - hut booking
 - meets management
 - guidebook shop
 - forums

Along with custom functionality such as New Routes, Munro Compleator & Himalayan Index.

Each Club owns its own site and code base whilst potentially benefiting from a common approach:
 - Common solutions
 - Reuseable code
 - Secure transfer between clubs (e.g. for shop or bookings)
 - Cross fertilisation (ideas, improvements, bugs)
 - Cross club support / maintenance

Our approach aims to provide:
 - Reduced Club Admin
 - Reduced Presure on Web Manager (easy updating of content through STRAPI)
 - Better functionality
 - Design Freedom for better branding
 - Faster and more responsive website
 - Lower Maintenance

<hr>

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



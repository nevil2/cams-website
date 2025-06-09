# Deployment

## GIT Repositories

All code is stored in Git repositiories either on [![alt h](github-mark.svg) GitHub](https://github.com/) 
or [![alt h](gitlab-logo.svg) GitLab](https://gitlab.com). When new code is pushed to production or development branch:
- Sveltekit applications are automatically deployed
- Strapi and Hono appications are built into [![alt b](docker-vector-logo.svg)](https://hub.docker.com/) containers and pushed to the revelant Container registry using GitHub Actions or GitLab CI/CD, from where they are typically automatically deployed.  

## Svelte / Sveltekit

[![alt l](cloudflare-logo.svg)](https://www.cloudflare.com/en-gb/) Pages or Workers is used to automatically deploy the majority of applications

Few applications are still on [![alt bb](/netlify-logo.svg)](https://www.netlify.com/).

## Strapi and Bespoke servers

[![alt b](digital-ocean-logo.svg)](https://www.digitalocean.com/) app platform is used to automatically deploy [![alt h](strapi-logo.svg)](https://strapi.io/) the application from its container registry, supported by its **PostgreSQL Managed Database Service** and **S3 storage**.


## Hono (Routes database)

[![alt b](digital-ocean-logo.svg) droplets](https://www.digitalocean.com/) (Linux-based virtual machines) are currently used for deployment. This allows use of local SQLite database, but involves work to set up, update, maintain, monitor and, in the rare event of a crash, require manual restart.  The techonolgies which need configuring include:

<p class="flex">
  <img class="mr-4" src="/ubuntu.svg" width="100" />
  <img class="mr-4" src="/docker-vector-logo.svg" width="100" /> 
  <img class="mr-4" src="/NGINX-logo.svg" width="100" />
  <img class="mr-4" src="/certbot-logo.svg" width="100" />
  <img class="mr-4" src="/ssh-com-logo.svg" width="100" />
</p>


### S3 Standard Storage

[![alt b](digital-ocean-logo.svg) Spaces](https://www.digitalocean.com/) is used to provide the  [S3 storage](https://en.wikipedia.org/wiki/Amazon_S3) needed 
to load, store or backup files, documents and images use.


### S3 Archive Storage

[![alt b](google-cloud-logo.svg) Archive Storage]() is used as a seperate low cost method to back up all content in the S3 Standard Storage.

### Managed Database Service

Either [![alt b](digital-ocean-logo.svg)](https://www.digitalocean.com/) and/or [![alt b](Neon_logo.svg)](https://www.neon.tech/) PostgreSQL Managed Database Service is used to support [![alt h](strapi-logo.svg)](https://strapi.io/) and other applications.
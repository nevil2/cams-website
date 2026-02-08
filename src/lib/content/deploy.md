# Deployment

## [![alt l](github-mark.svg) GitHub](https://github.com/)

All code is stored in Git repositories in club specific accounts. Code pushed to GitHub triggers either:
- Cloudflare to deploy the commit, or
- GitHub Actions to build the commit into a [![alt b](docker-vector-logo.svg)](https://hub.docker.com/) container and push it to the relevant Container registry.

GitHub actions are also used for:
- backup of Cloudflare D1 databases
- webhook triggered from Strapi to rebuild and deploy a club website

## [![alt l](cloudflare-logo.svg)](https://www.cloudflare.com/en-gb/)

Each club has its own Cloudflare account which is used for:
1. Domain registration and management, DNS and domain specific rules
2. Cloudflare Workers which in turn can use KV storage, D1 database, R2 object storage, Observability logs and Analytics Engine
3. Cloudflare Turnstile as CAPTCHA replacement

All Sveltekit applications and the bespoke Hono servers are deployed on Cloudflare.


## [![alt l](digital-ocean-logo.svg)](https://www.digitalocean.com/)

1. **App platform** is used to automatically deploy [![alt h](strapi-logo.svg)](https://strapi.io/) the application from its container registry, supported by its **PostgreSQL Managed Database Service** and **S3 storage**.
2. **Droplets** (Linux-based virtual machines) are currently used the routes database servers, as they have persistent storage which  allows use of local SQLite database.  VM require more work the managed platforms to set up, update, maintain, monitor and, in the rare event of a catastrophic crash, manually restart.  Technologies which need configuring include:
  <div class="flex ml-8 pb-4 gap-4">
    <img src="/ubuntu.svg" width="50" />
    <img src="/docker-vector-logo.svg" width="50" /> 
    <img src="/NGINX-logo.svg" width="50" />
    <img src="/certbot-logo.svg" width="50" />
    <img src="/ssh-com-logo.svg" width="50" />
  </div>

1. **Spaces** is used to provide the [S3 storage](https://en.wikipedia.org/wiki/Amazon_S3) needed 
to load, store or backup files, documents and images use.
1. **PostgreSQL Managed Database Service** is used to support [![alt h](strapi-logo.svg)](https://strapi.io/)
2. **Container Registry** and **Firewalls** are used to support the above.


## Others

[![alt b](google-cloud-logo.svg) Archive Storage](https://cloud.google.com/storage) provides a separate low cost S3 storage to back up all content in the S3 Standard Storage.

[![alt b](Neon_logo.svg)](https://www.neon.tech/) is used by some clubs as an alternative to Digital Ocean PostgreSQL Managed Database Service

[![alt b](aws.svg) Amazon Simple Email Service](https://aws.amazon.com/ses/) is used to send emails from the web servers.

[![alt b](zeptomail.svg)](https://www.zoho.com/zeptomail/) is used by one club as an alternative to AWS SES.

[![alt b](stripe.svg)](https://stripe.com/gb) is used for Card payments

[![alt h](gocardless.svg)](https://gocardless.com/) is used for Direct Debit payments

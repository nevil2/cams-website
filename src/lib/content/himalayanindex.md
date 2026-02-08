
![Himalayan Index application](HimalayanIndex.jpg)

## Himalayan Index

A [replacement](https://ac-hi.topoeditor.com/) for the [Alpine Club's](http://www.alpine-club.org.uk/) ageing [Himalayan Index](http://www.alpine-club.org.uk/hi/) is in development.  This will enable remote updating on the database by a variety of volunteers.

- frontend built with [![Svelte logo h](svelte-logo.svg)](https://svelte.dev/) **Svelte**,
[![alt h](tailwindcss-logo.svg)](https://tailwindcss.com/),
[![alt h](typescript-logo.svg)](https://www.typescriptlang.org/) **Typescript**,
**HTML** and **CSS**

- api built with [![alt h](fastapi-logo.svg) FastAPI](https://fastapi.tiangolo.com/) / [![alt h](pydantic-logo.svg) Pydantic](https://docs.pydantic.dev/) / [![alt h](sqlalchemy-logo.png)](https://www.sqlalchemy.org/) / [![alt h](python-logo.svg)](https://www.python.org/)


It uses two SQL databases for performance:

- for public use, an [![alt h](sqlite-logo.gif)](https://www.sqlite.org/) database is loaded from S3 storage into memory.  This gives optimum response.
- for editors, [![alt h](Neon_logo.svg)](https://www.neon.tech/) [![alt h](postgresql-logo.svg)](https://www.postgresql.org/) service is used (free tier).

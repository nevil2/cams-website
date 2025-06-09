<base target="_blank">

![image alt N](DigitalGuide.jpg)

## Digital Guide

This is a web-based routes database application specially designed:
 - for Guidebook producers, allowing multiple descriptions of routes from different guidebooks
 - for future web and mobile publishing

Access to the core application is restricted.

The core application has been extended with:
 - [Feeder web application](https://smc.org.uk/climbs/submission) for collecting new route details direct from climbers
 - [TopoEditor](https://topoeditor.com) software for creating interactive topos suitable for print, web and mobile 
 - [Public web application](https://smc.org.uk/climbs/newroutes) for disemminating new route information

Future extensions are likely to include:
 - Adobe InDesign and Illustrator scripts or plugins to facilate guidebook production
 - Additional public web applications
 - Mobile publishing (possibly through an existing mobile app)
 - Comprehensive analysis of first ascent data

<hr>

## Technology

The core and new route full-stack applications are built with
[![alt h](nuxt-logo.svg)](https://nuxt.com/) / 
[![alt h](vue-logo.svg) VueJS](https://vuejs.org/) /
[![alt h](nuxt-logo.svg)](https://nuxt.com/) /
[![alt h](nodejs-logo.svg)](https://nodejs.org/en/about/) /
[![alt h](express-logo.png)](https://expressjs.com/).

<!-- TopoEditor is built with [![alt h](vue-logo.svg) VueJS](https://vuejs.org/).  It is integrated into above applications as well as deployed as a separate site (using ![alt h](vite-logo.svg) [ViteJS](https://vitejs.dev)).

The SMC new routes site frontend uses ![alt h](react-logo.svg) [React](https://reactjs.org/) and backend uses [![alt h](fastapi-logo.svg) FastAPI](https://fastapi.tiangolo.com/) / [![alt h](pydantic-logo.svg) Pydantic](https://docs.pydantic.dev/) / [![alt h](sqlalchemy-logo.png)](https://www.sqlalchemy.org/) / [![alt h](python-logo.svg)](https://www.python.org/). -->

## Deployment

The main Climbing Database Applications are currently being run on Linux-based virtual machines (one for each club).  The entry level has sufficent CPU, RAM and memory (providing pre-built containers are used) and is very cost effective as: 
 - Climbing Databases can be stored and run from the internal memory (provided appropriate backup is organised)
 - More than one service can be run on one virtual machine (e.g. [New Route Reporting](https://report.smc.org.uk/).)

Virtual machines require some work to set up, update, maintain and monitor (compared to 'serverless' used for other applications).

<div class="flex">
  <a class="mr-4" href="https://ubuntu.com/"><img  src="/ubuntu.svg" width="120" /></a>
  <a class="mr-4" href="https://hub.docker.com/"><img src="/docker-vector-logo.svg" width="120" /></a>
  <a class="mr-4" href="https://www.nginx.com/"><img src="/NGINX-logo.svg" width="100" /></a>
  <a class="mr-4" href="https://certbot.eff.org/"><img src="/certbot-logo.svg" width="100" /></a>
  <a class="mr-4" href="https://en.wikipedia.org/wiki/Secure_Shell"><img src="/ssh-com-logo.svg" width="100" /></a>
</div>

All applications use S3 storage for images, documents and other files.

## Cloud Service Providers

<div class="flex items-center my-0">
  <img class="mr-4 mt-0" src="/digital-ocean-logo.svg" width="100" /> 
  is used as its offers simpler, lower cost, fixed price services compared to AWS, Microsoft Azure and Google Cloud.
</div>
<div class="flex items-center my-0">
  <img class="mr-4 mt-0" src="/google-cloud-logo.svg" width="100" />
  Archive Storage is used for backing up files, documents and images.
</div>

<div class="flex items-center my-0">
  <img class="mr-4 mt-0" src="/netlify-logo.svg" width="100" />
  <span>
    is used to host <a href="https://topoeditor.com"> https://topoeditor.com</a> 
    and <a href="https://newroutes.smc.org.uk">https://newroutes.smc.org.uk</a>
  </span>
</div>
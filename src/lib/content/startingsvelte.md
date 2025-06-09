If you are beginer to software development, you need to set up your environment first.

On Windows PC, you need:

1. Install WSL2 (Windows Subsystem for Linux) from Microsoft store
2. Install Visual Studio Code
3. Open a windows terminal and start Ubuntu
4. Install either fnm and nvm (fnm is newer and faster, but either will do).  These can install node and npm. 


Now that the enviroment is set up, to create a new Svelte project you can use vite. In command line, 

``npm create vite@latest``

It then asks:
Project name.  This will be the name of a new folder in which the project will be created.
Select a framework.  Select svelte if you want easiest framework to learn (also faster with smaller bundle size)
Select a variant.  Choose javascript if you want to keep things simple

It will then tell you to run:
>cd project-name  (goes to new subdirectory)
>npm install (this installs all the software that is included in package.json)
>npm run dev (this starts site in development mode – you will need to use localhost link to open site in browser)
Use control C when you wish to stop running dev mode.

I recommend opening VS code in project folder (before npm run dev) by typing:
``code .``

In dev mode, there is hot reloading – i.e. when you update and save code, it immediately changes webpage.

You can now play with editing code (at this point, Tailwind is not installed).

To build for production, run:
``npm run build``

In the project folder, there will now be a folder called ‘dist’.  This contains the built code.

To see result of build, run:
``npm run preview`` (there will be no hot-reloading)

To deploy the site to the web FOC, go to Netlify.com and set up an account.  I think it will lead you process of deploying first site.  You want to do manual deploy.  When it give you option to upload project, drag the dist folder (as mentioned above using windows explorer) into the upload box.  It should then deploy it and give you an url to access it.

Netlify charge for build time (free allowance 300 minutes per month) and bandwidth (100GB free per month).

As you will have pre-built your project with Vite, build time will be zero.  As for bandwidth, if project is 100KB zipped, that allows 1 million downloads per month.

## GIT

In order to backup your code, share it with others and manage different versions, developers normally use GIT, either GitHub or GitLab.


https://learn.svelte.dev/


JavaScript:
https://www.w3schools.com/js/default.asp
https://www.codecademy.com/learn/introduction-to-javascript


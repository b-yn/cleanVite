# cleanVite
A fresh Dockerized Vite-Vuejs app. Clone this repo, hit "Docker compose up" and you are set.


# How to use
I made sure to include the node_modules folder so that when you clone this repo, you don't need to install it inside your docker container.

1- clone the repo
2- run this command in the folder: `docker compose up`
3- and you are ready to go


sometimes there is an issue with `npm run dev`. The host is not able to communicte with docker container althogh the ports are forwarding. I tried `yarn dev` it worked with no problem. If still you had problems, try to add the following to your package.json file: 
```
"scripts": {
    "dev": "vite --host 0.0.0.0",
    "build": "vite build",
    "serve": "vite preview"
  },

```
(note the --host 0.0.0.0)




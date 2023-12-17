<h1 align="center">
  <a href="#">Fake Blog With Nuxt.js</a>
</h1>

<h3 align="center">
  Simple fake blog with Nuxt.js and json-server
</h3>

<h4 align="center"> 
	 Status: Finished
</h4>

<p align="center">
 <a href="#about">About</a> •
 <a href="#features">Features</a> •
 <a href="#layout">Layout</a> • 
 <a href="#how-it-works">How it works</a> • 
 <a href="#tech-stack">Tech Stack</a> •  
 <a href="#author">Author</a>
</p>

## About

> It is a simple fake blog it save the posts in a JSON file using json-server lib and rendering using `micromark` lib.

---

## Concepts to study during development

- [x] File system routing and dynamic routing
- [x] Data fetching and why Axios is not supported in Nuxt.js?
- [x] `SSR` and `SSG` with Nuxt.js, how it works?
- [x] More about `slot` Vue functionality
- [x] json-server with Nuxt.js
- [x] Nuxt Content for render markdown content and study other use cases of this lib also
- [x] Environment variables
- [x] More about nuxt.config.ts file and your options
- [x] Basic of page transitions with default functionality of Nuxt.js
- [x] SEO with Nuxt.js
- [x] Basic use of PrimeVue
- [x] Tailwind with Nuxt.js

---

## Features

- [x] See recent posts
- [x] See all posts
- [x] See post details with dynamic route

---

## Layout

### Homepage
<img src="https://github.com/Artur-Poffo/JSON-Blog-Nuxt.js/blob/main/public/README/Home.png?raw=true" alt="Print of Homepage" />

### All posts page
<img src="https://github.com/Artur-Poffo/JSON-Blog-Nuxt.js/blob/main/public/README/AllPosts.png?raw=true" alt="Print of All posts page" />

### Post page
<img src="https://github.com/Artur-Poffo/JSON-Blog-Nuxt.js/blob/main/public/README/Post.png?raw=true" alt="Print of post page" />

---

## How it works

### Pre-requisites

Before you begin, you will need to have the following tools installed on your machine:
[Git](https://git-scm.com), [Node.js](https://nodejs.org/en/) and the [pnpm](https://pnpm.io) package manager.

In addition, it is good to have an editor to work with the code like [VSCode](https://code.visualstudio.com/).

```bash
# Clone this repository
$ git clone https://github.com/Artur-Poffo/JSON-Blog-Nuxt.js.git

# Access the project folder cmd/terminal
$ cd JSON-Blog-Nuxt.js

# install the dependencies
$ pnpm i

# Run the application in development mode
$ pnpm dev

# This run then Nuxt app and the json-server API

# The server of Nuxt.js app will start at port: 3000 - go to http://localhost:3000
# If you want to access the JSON API - go to http://localhost:3333
```

---

## Tech Stack

The following tools were used in the construction of the project:

- Vue.js
- Typescript
- Nuxt.js
- Tailwind CSS
- vue-router
- heroicons/vue (Icons lib)
- Nuxt PrimeVue
- micromark (Render Markdown lib)
- json-server (Serve a JSON based API)

> See the file  [package.json](https://github.com/Artur-Poffo/JSON-Blog-Nuxt.js/blob/main/package.json)

---

## Author

- _**Artur Poffo - Developer**_

[![Linkedin Badge](https://img.shields.io/badge/-Artur-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/arturpoffo/)](https://www.linkedin.com/in/arturpoffo/)
[![Gmail Badge](https://img.shields.io/badge/-arturpoffop@gmail.com-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:tgmarinho@gmail.com)](mailto:arturpoffop@gmail.com)
---
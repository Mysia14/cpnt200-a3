# CPNT 200-a3 - JAMstack Deployment

## Author: 
Mysia Santana

## Links:
* [GH repo](https://github.com/Mysia14/cpnt200-a3)
* [Netlify App](https://hardcore-kare-6bcfa7.netlify.app/) :thumbdown:

 #### Code Review:
 - I had some diffiulties wiht the Nuxtjs setup as well the Vuetify, which made me delete my old repo e rebuild it. I got a little confused about the Vuetify and Tailwind. Both were added but I couldnt work properly with them.
 - I also had many vulnerabilities while downloading the dependiecies and even using "npm audit fix" I wasnt able to fixe them all.
 - The major problem was a error during deployment : `Error: /gallery not found at QueryBuilder.fetch (/opt/build at asyncData (pages/index.vue:26:0) at promisify (node_modules/.cache/nuxt/utils.js:304:0) at server.js:6976:23 at Array.map (<anonymous>)at module.exports.__webpack_exports__.default (node_modules/.cache/nuxt/server.js:231:0)`. Even have searched hot to fix through several websites refences, unfortunatelyI was not able to fix it. The two contents folders were not found. I also tried to add a webpack in the package.json file, as one of the websites have suggested, but no succes.
* Some wesites that I have searched through were: (https://content.nuxtjs.org/fetching/), (https://answers.netlify.com/t/page-not-found-after-deployment/2362/27), (https://github.com/typeorm/typeorm/issues/747), (https://gist.github.com/lilyx13),(http://www.ostack.cn/?qa=302034/),(https://laracasts.com/discuss/channels/vue/missing-stack-frames-in-vue-nuxt),(https://github.com/nuxt/nuxt.js/issues/6640), (https://www.dynamichands.nl/blog/query-builder-error-attribute-not-found-in-metadatacache/) and more.
- So after so many tries I wonder if I missed to run or install something so the app could run properly.
- Even the deployment is not working as expected the page can be listened on http://localhost:3000/.
 
## Attributions:
#### Code structure and help:
- [Ashlyn Knox](https://gist.github.com/lilyx13) 
##### Images:
- Fall Image[Pexel -  Craig Adderley](https://www.pexels.com/photo/concrete-road-between-trees-1563356/).
- Winter Image[Pexel -Pixabay](https://www.pexels.com/photo/snowy-forest-235621/)
- Spring Image[Pexel - Nathan Cowley from Pexels](https://www.pexels.com/photo/pink-flowers-photography-1128797/)
- Summer Image[Pexel - MarcTutorials from Pexel](https://www.pexels.com/photo/palm-trees-1152359/)
- Vuetify (https://vuetifyjs.com/en/getting-started/installation/)

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out the [documentation](https://nuxtjs.org).

## Special Directories

You can create the following extra directories, some of which have special behaviors. Only `pages` is required; you can delete them if you don't want to use their functionality.

### `assets`

The assets directory contains your uncompiled assets such as Stylus or Sass files, images, or fonts.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/assets).

### `components`

The components directory contains your Vue.js components. Components make up the different parts of your page and can be reused and imported into your pages, layouts and even other components.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/components).

### `layouts`

Layouts are a great help when you want to change the look and feel of your Nuxt app, whether you want to include a sidebar or have distinct layouts for mobile and desktop.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/layouts).


### `pages`

This directory contains your application views and routes. Nuxt will read all the `*.vue` files inside this directory and setup Vue Router automatically.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/get-started/routing).

### `plugins`

The plugins directory contains JavaScript plugins that you want to run before instantiating the root Vue.js Application. This is the place to add Vue plugins and to inject functions or constants. Every time you need to use `Vue.use()`, you should create a file in `plugins/` and add its path to plugins in `nuxt.config.js`.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/plugins).

### `static`

This directory contains your static files. Each file inside this directory is mapped to `/`.

Example: `/static/robots.txt` is mapped as `/robots.txt`.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/static).

### `store`

This directory contains your Vuex store files. Creating a file in this directory automatically activates Vuex.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/store).

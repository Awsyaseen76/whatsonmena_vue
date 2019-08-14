# Vue with Amplify

## Start from 0:
`npm install -g @vue/cli`
`npm install -g @aws-amplify/cli`

### Create a App:
- `vue create whatsonmena_amplify`
- Choose: Babel, Router, Vuex and Linter/Formatter
    the configurations for babel, eslint ... is in the package.json
- run the app
    `npm run serve`
#### The power of Prettier:
- config Prettier in package.json
    using single quote and tab 4 spaces not 2(default)
- put it in action from terminal:
    `npm run lint`

## Using Vuetify:
- `vue add vuetify`


## Try to put it on Docker
- create the Dockerfile
- terminal:
    `docker build -t dockerize-vue .`
    run it:
    `docker run -it -p 8080:80 --rm --name dockerize-vuejs dockerize-vue`
    go to:
    `localhost:8080`

###Notes:
1. if go to: `localhost:8080/home` it is not working
    but if we use the navbar its ok
2. the menu bar for the larg screen is not ok





---------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------

# whatsonmena_amplify

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

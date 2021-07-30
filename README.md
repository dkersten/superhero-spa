# superhero-app

## Project description
A single page web app that shows superheros and some of their stats from the [superhero API](https://akabab.github.io/superhero-api/). The app is built with Vue, styled in CSS, and data retrieved with Axios.

A live version can be viewed [here](https://sleepy-edison-f2e48a.netlify.app/)

## Project Focuses
I focused mainly on a clean, simple design that is fully responsive. Another important focus was making sure the app is accessible based on WCAG standards (I audited the app in Google Lighthouse and Axe dev tools).

## Future Additional Features
There are a few features I'd like to add if I had more time such as filtering based on the API data (such as gender - show just females, just males, or both). Another feature I'd like to add is a state management tool (Vuex), which would help make filtering easier. I would also like to add a fully accessible modal that would display all stats about a hero on user click. Finally I would like to give someone the ability to add new superheros (although this would depend on the permissions of the API (I did not see a create route in the API docs).



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

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

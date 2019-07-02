# Vue.js SVG Responsive Component 

> Simply Demonstrate a Vue.js component that returns a SVG file passed to the component as a property + turn the `img` html tag into a responsive/adaptative element using CSS rules

__Method:__

- we use a computed property to work with the SVG file into the component. 

**note:** _Computed properties_ sit halfway between properties of the data object and methods: we can access them **as if they were properties of the data object**, but they are specified as functions...
- we create a computed property function that returns the `.svg` file path using the `require()` method to `access` the assets folder
- we create the full path to the `.svg` source file using the value stored/passed as the property (props) of the component `this.SVGFile`
- we use the ES6 template literal syntax to construct the full path dynamically...
- we bind the value of the computed property to the `src` attribute of the `img` html tag...
- the `responsive-img` CSS class will let the `img` tag to automatically fit the size of its parent container


component `src\components\SVG-image.vue`
```
<template>
  <div>    
    <img class="responsive-img" alt="JS logo" :src="path">
  </div>
</template>

<script>
export default {
  name: 'SVG-image',
  props: {
    SVGFile: String
  },
  computed: {
    path(){
      return require( `@/assets/svg/${this.SVGFile}`)
    }
  }
}
</script>

<style lang="scss" scoped>

.responsive-img{
  max-width: 100%;
  height: auto;
}

</style>
```
Using the component `src\App.vue`

```
<template>
  <div id="app">
    <main>
      <SVGImage SVGFile='logo-js.svg'/>
    </main>
  </div>
</template>

//...
```
![gif](https://raw.githubusercontent.com/Drozerah/MyGitHubStorage/master/gif/svg-component/vue-svg-component.gif)

## Check it out !

### Get a local copy of this repository

```bash
$ git clone https://github.com/Drozerah/vue-svg-responsive-component.git
```

### Project setup
```bash
$ npm install
```

### Compiles and hot-reloads for development
```bash
$ npm run serve
```

### Compiles and minifies for production
```bash
$ npm run build
```
Once you are done with the compilation, simply:

```bash
$ cd dist
```
Then go live your `index.html` with your local development server...

That's it!

__Author__

- Thomas G. aka Drozerah - [GitHub](https://github.com/Drozerah)

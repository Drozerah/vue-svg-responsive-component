<template>
  <div id="app">
    <main>
      <Title msg="SVG Component"/>
      <SVGImage SVGFile='logo-js.svg'/>
    </main>
  </div>
</template>

<script>
import Title from './components/Title.vue'
import SVGImage from './components/SVG-image.vue'

export default {
  name: 'app',
  components: {
    Title,
    SVGImage
  }
}
</script>

<style>
body{
  height: 100%;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  width: 100%;
  height: 100%;
  color:#333;
}
main {
  width: 30%;
  margin: auto;
  background-color: #E7E7E7;
  padding:20px;
}
</style>

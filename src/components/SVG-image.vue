<template>
  <div>    
    <img class="responsive-img" alt="JS logo" :src="path">
    <ul>
      <li><span>src file:</span> {{SVGFile}} </li>
      <li><span>compiled path:</span> {{path}} </li>
    </ul>
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
ul{
  font-size: 1.5vw;
  margin-bottom: 0px;
  padding-left: 25px;
  li{
    span{
      color:grey;
    }
  }
}
</style>
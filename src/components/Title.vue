<template>
  <div class="title">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Title',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1{
  text-align: center;
  font-size:3vw;
}
</style>

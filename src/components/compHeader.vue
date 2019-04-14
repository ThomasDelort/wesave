<template>

<header class="header">
  <h1>Mes {{page}}</h1>
</header>

</template>

<script>
export default {
  name: 'compHeader',
  data () {
    return {
      title: page
    }
  },
  props: {
   page: {
    type: String,
    required: true
   }
  }
}
</script>

<style lang="scss">

 
.header {
  height: 20rem;
  background-image: linear-gradient(rgba(#000,0.25), rgba(#000,0.25)), url('../assets/header.jpeg');
  background-size: cover;
  background-position: bottom;
  position: relative;

  h1 {
    position: absolute;
    bottom: 40%;
    left: 50%;
    transform: translateX(-50%);
    text-align: center;
    font-size: 4.5rem;
  }
} 
</style>
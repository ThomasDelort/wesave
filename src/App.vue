<template>

  <!DOCTYPE html>
  <html lang="fr">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <meta http-equiv="X-UA-Compatible" content="ie=edge">
      <link href="https://fonts.googleapis.com/css?family=Lato" rel="stylesheet">

      <title>Test</title>
  </head>
  <body>
      <compHeader :page=page></compHeader>
      <compNav @clicked="ClickButton"></compNav>
      <compAlbums v-if="page === 'albums'"></compAlbums>
      <compPlaylists v-if="page === 'playlists'"></compPlaylists>
  </body>
  </html>

</template>

<script>
  import compHeader from './components/compHeader.vue'
  import compNav from './components/compNav.vue'
  import compAlbums from './components/compAlbums.vue'
  import compPlaylists from './components/compPlaylists.vue'

  let page = "albums";

  export default {
    name: 'app',
    components: {
      compHeader,
      compNav,
      compAlbums,
      compPlaylists
    },
    data () {
      return {
        page
      }
    },
      methods: {
      ClickButton: function(button) {
        if(button === "albums") {
          this.page = "albums";
        }
        if(button === "playlists") {
          this.page = "playlists";
        }
      }
    }
  }
</script>

<style lang="scss">

*,
*::after,
*::before {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}

html {
    // 1rem = 10px
    font-size: 62.5%; 
    font-family: 'Lato', sans-serif;
    background-color: #FFF;
  }

body {
  box-sizing: border-box;
  max-width: 114rem;
  margin: 0 auto;
  background-color: #212121;
  color: #FFF;
  height: 100vh;
}

</style>

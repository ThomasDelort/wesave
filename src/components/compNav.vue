<template>

    <nav>
        <button v-on:click="clickAlbum()" class="nav__btn-albums active">Mes albums</button>
        <button v-on:click="clickPlaylists()" class="nav__btn-playlists">Mes playlists</button>
    </nav>

</template>

<script>
export default {
  name: 'compNav',
    methods: {
    clickAlbum: function (button) {
      this.$emit('clicked', 'albums')
      document.getElementsByClassName('nav__btn-playlists')[0].classList.remove('active');
      document.getElementsByClassName('nav__btn-albums')[0].classList.add('active');
    },
    clickPlaylists: function (button) {
     this.$emit('clicked', 'playlists')    
      document.getElementsByClassName('nav__btn-albums')[0].classList.remove('active');
      document.getElementsByClassName('nav__btn-playlists')[0].classList.add('active');
    }
  }
}
</script>

<style lang="scss">

nav {

    &:after {
      content: "";
      display: table;
      clear: both;
    }
  
    background-color: #212121;
    padding: 2rem;
  
    button {
          padding: 2rem; 
          text-decoration: none;
          text-align: center;
          font-size: 1.5rem;
          display: block;
          float: left;
          background-color: #000;
          border: 0;
          color: #FFF;
          text-transform: uppercase;
          width: calc((100% - 2rem) / 2);
          outline: none;
          cursor: pointer;

          &:first-child{
              margin-right:2rem;
          }

          @media (max-width: 37.5em) { // 600px
            width: calc(100%);
            &:last-child {
                margin-top: 2rem;
            }
          }
  
          &.active {
              color: #fec107;
          }
      }
  }

</style>
<template>

<section class="albums">
        <table>
            <tr class="lists__head">
                <th class="lists__del"></th>
                <th class="lists__title"><span>Titres</span></th>
                <th class="lists__size"></th>
            </tr>
            <tr v-for="item in ALBUMS" :key="item.id" class="lists__element">
                <td class="lists__del"></td>
                <td class="lists__title">{{item.name}}</td>
                <td class="lists__size"></td>
            </tr>
        </table>
    </section>

</template>

<script>
  import { ALBUMS } from '../data.js'

export default {
  name: 'compAlbums',
  data () {
    return {
      ALBUMS
    }
  }
}
</script>

<style lang="scss">

.albums, .playlists {
    background-color: #212121;
    padding: 0 2rem;

    table {
        width: 100%;
        border: 0;
        border-spacing: 0;
    }

    tr:nth-child(odd) {
        background-color: #373737;
    }

    tr:first-child {
        background-color: #907114; 
    }
    
    th, td {
        font-size: 1.5rem;
        line-height: 6rem;
        height: 4rem;
        font-weight: normal;
    }
    th span {
        cursor: pointer;
    }
        
        .lists__del {
            width: 6rem;
            padding-left: 2rem;
            color: #000;
            font-weight: bold;
        }
        .lists__title {
            text-align: left;
        }
        .lists__size {
            width: 6rem;
            text-align: right;
            padding-right: 2rem;
        }
}

</style>
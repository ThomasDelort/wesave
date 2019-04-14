<template>

<section class="playlists">
        <table>
            <tr class="lists__head">
                <th class="lists__del"></th>
                <th class="lists__title"><span>Titres</span></th>
                <th class="lists__size"><span>Taille</span></th>
            </tr>
            <tr v-for="item in PLAYLISTS" :key="item.id" class="lists__element">
                <td class="lists__del">{{ item.size === 0 ? '&#10680;' : '' }}</td>
                <td class="lists__title">{{item.name}}</td>
                <td class="lists__size">{{item.size}}</td>
            </tr>
        </table>
    </section>

</template>

<script>
  import { PLAYLISTS } from '../data.js'

export default {
  name: 'compPlaylists',
  data () {
    return {
      PLAYLISTS
    }
  }
}
</script>
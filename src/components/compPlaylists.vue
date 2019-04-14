<template>

<section class="playlists">
        <table>
            <tr class="albums__head">
                <th class="albums__del"></th>
                <th class="albums__title"><span>Titres</span></th>
                <th class="albums__size"><span>Taille</span></th>
            </tr>
            <tr class="albums__element">
                <td class="albums__del"></td>
                <td class="albums__title">Album 1</td>
                <td class="albums__size">15</td>
            </tr>
            <tr class="albums__element">
                <td class="albums__del"></td>
                <td class="albums__title">Album 2</td>
                <td class="albums__size">10</td>
            </tr>
            <tr class="albums__element">
                <td class="albums__del">&#10680;</td>
                <td class="albums__title">Album 3</td>
                <td class="albums__size">0</td>
            </tr>
            <tr class="albums__element">
                <td class="albums__del">&#10680;</td>
                <td class="albums__title">Album 4</td>
                <td class="albums__size">0</td>
            </tr>
            <tr class="albums__element">
                <td class="albums__del"></td>
                <td class="albums__title">Album 5</td>
                <td class="albums__size">20</td>
            </tr>
        </table>
    </section>

</template>

<script>
export default {
  name: 'compPlaylists',
  data () {
    return {
      msg: ''
    }
  }
}
</script>
<template>

<section class="albums">
        <table>
            <tr class="albums__head">
                <th class="albums__del"></th>
                <th class="albums__title"><span>Titres</span></th>
                <th class="albums__size"></th>
            </tr>
            <tr class="albums__element">
                <td class="albums__del"></td>
                <td class="albums__title">Album 1</td>
                <td class="albums__size"></td>
            </tr>
            <tr class="albums__element">
                <td class="albums__del"></td>
                <td class="albums__title">Album 2</td>
                <td class="albums__size"></td>
            </tr>
            <tr class="albums__element">
                <td class="albums__del"></td>
                <td class="albums__title">Album 3</td>
                <td class="albums__size"></td>
            </tr>
            <tr class="albums__element">
                <td class="albums__del"></td>
                <td class="albums__title">Album 4</td>
                <td class="albums__size"></td>
            </tr>
            <tr class="albums__element">
                <td class="albums__del"></td>
                <td class="albums__title">Album 5</td>
                <td class="albums__size"></td>
            </tr>
        </table>
    </section>

</template>

<script>
export default {
  name: 'compAlbums',
  data () {
    return {
      msg: ''
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
        
        .albums__del {
            width: 6rem;
            padding-left: 2rem;
            color: #000;
            font-weight: bold;
        }
        .albums__title {
            text-align: left;
        }
        .albums__size {
            width: 6rem;
            text-align: right;
            padding-right: 2rem;
        }
}

</style>
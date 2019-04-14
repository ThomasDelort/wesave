<template>

<section class="playlists">
        <table>
            <tr class="lists__head">
                <th class="lists__del"></th>
                <th class="lists__title"><span v-on:click="orderedName()">Titres</span></th>
                <th class="lists__size"><span v-on:click="orderedSize()">Taille</span></th>
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

// variables et fonctions pour le tri des listes

let order = "nameDESC";

function dynamicSort(property) {
    var sortOrder = 1;
    if(property[0] === "-") {
        sortOrder = -1;
        property = property.substr(1);
    }
    return function (a,b) {
        var result = (a[property] < b[property]) ? -1 : (a[property] > b[property]) ? 1 : 0;
        return result * sortOrder;
    }
}

export default {
  name: 'compPlaylists',
  data () {
    return {
      PLAYLISTS
    }
  },
    methods: {
        orderedSize: function () {
            if(order === "sizeDESC"){
                PLAYLISTS.sort(dynamicSort("-size"))
                order = "sizeASC"
            } 
            else {
                PLAYLISTS.sort(dynamicSort("size"))
                order = "sizeDESC"
            }
        },
        orderedName: function () {
            if(order === "nameDESC"){
                PLAYLISTS.sort(dynamicSort("-name"))
                order = "nameASC"
            } 
            else {
                PLAYLISTS.sort(dynamicSort("name"))
                order = "nameDESC"
            }
        }
    }
}
</script>
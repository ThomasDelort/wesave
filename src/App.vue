<template>

<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link href="https://fonts.googleapis.com/css?family=Lato" rel="stylesheet">
    <link rel="stylesheet" type="text/css" href="./assets/style.css">

    <title>Test</title>
</head>
<body>
    <header class="header">
        <h1>Mes albums</h1>
    </header>
    <nav>
        <button class="nav__btn-albums active">Mes albums</button>
        <button class="nav__btn-playlists">Mes playlists</button>
    </nav>
    <section class="albums">
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

</body>
</html>

</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>

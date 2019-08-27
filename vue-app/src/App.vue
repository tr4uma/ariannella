<template>
  <div id="app">
    <Arianna :quotes="quotes" />
    <Credits />
  </div>
</template>

<script>
import Arianna from './components/Arianna.vue'
import Credits from './components/Credits.vue'


export default {
  name: 'app',
  components: {
    Arianna,
    Credits
  },
  data: () => {
    return {
      quotes: [
        `GIRIBOLDIIIIIIIIII!`,
        `Non dico mai cagate, cara!`,
        `Io no ragazzi, git lens parla`,
        `Fottiti giriboldi.
Scherzavo.`,
        `Ormai i branches li sento tutti miei.
Li prendo tutti`,
        `Fruck!`,
        `Gulpiamo!
Pfsiuw!`,
        `Già che siamo qua..`
      ]
    }
  }
}
</script>

<style>
* {
  padding: 0px;
  margin: 0px;
}
html {
  width: 100%;
  height: 100%;
}
body {
  width: 100%;
  height: 100%;
}
#app {
  font-family: Courier;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
  width: 100%;
  display: flex;
  justify-content: center;
  justify-items: center;
  flex-direction: column;
}
</style>

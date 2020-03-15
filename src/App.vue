<template>
  <div class="container" id="app">
    <PartyList></PartyList>
  </div>
</template>

<script>
import PartyList from './components/PartyList'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    PartyList
  },
  data () {
    return {
      url: 'http://data.riksdagen.se/personlista/?iid=&fnamn=&enamn=&f_ar=&kn=&parti=&valkrets=&rdlstatus=&org=&utformat=json&sort=sorteringsnamn&sortorder=asc&termlista='
    }
  },
  mounted () {
    axios
    .get(this.url)
    .then(response => console.log(response))
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

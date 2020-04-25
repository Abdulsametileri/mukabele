<template>
  <div id="app">
  <!--
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>-->
    <h3 v-if="katilimciMi">
      <a :href="streamyard">Canlı Yayına Katılmak İçin Tıklayın!</a>
    </h3>
    <h3 v-else>
      <a :href="youtube">Canlı Yayını İzlemek İçin Tıklayın!</a>
      <br>

      <h3>Geçmiş Yayınlarımız</h3>

      <a href="https://www.youtube.com/watch?v=oB1zixMQEro">RAMAZAN MUKABELESİ 1. CÜZ</a>
      <a href="https://www.youtube.com/watch?v=5jKn8cbNa-E">RAMAZAN MUKABELESİ 2. CÜZ</a>
    </h3>
  </div>
</template>

<script>
  export default {
    name: 'App',
    data() {
      return {
        katilimciMi: false,
        streamyard: 'https://streamyard.com/s8a64uv7xa',
        youtube: 'https://www.youtube.com/watch?v=2liZ3Q4auy0'
      }
    },
    created() {
      if (this.$route.path === "/katilimci") {
        this.katilimciMi = true;
      }
      else {
        this.katilimciMi = false;
      }
    }
  }
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>

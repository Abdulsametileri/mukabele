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
      <br>
      <a href="https://www.youtube.com/watch?v=5jKn8cbNa-E">RAMAZAN MUKABELESİ 2. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=cljLguKrwr8">RAMAZAN MUKABELESİ 3. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=ZqOqdJ1fRc4">RAMAZAN MUKABELESİ 4. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=Vg1BoPqmYVY">RAMAZAN MUKABELESİ 5. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=zE9Vveev2PQ">RAMAZAN MUKABELESİ 6. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=j7oN4K593Zk">RAMAZAN MUKABELESİ 7. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=DJhUI13_oMc">RAMAZAN MUKABELESİ 8. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=F2Il2Q0UeCc">RAMAZAN MUKABELESİ 9. CÜZ 1-10. Sayfalar</a>
      <br>
      <a href="https://www.youtube.com/watch?v=unK9FzJUffY">RAMAZAN MUKABELESİ 9. CÜZ 11-20. Sayfalar</a>
      <br>
      <a href="https://www.youtube.com/watch?v=VgMDhqH68ts">RAMAZAN MUKABELESİ 10. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=81_IRjjhcOA">RAMAZAN MUKABELESİ 11. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=SV9e2nI6R_k">RAMAZAN MUKABELESİ 12. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=yI6GFobaURI">RAMAZAN MUKABELESİ 13. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=kKdKvW03Ytw">RAMAZAN MUKABELESİ 14. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=Zh6IdjrYS4o">RAMAZAN MUKABELESİ 15. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=4fMYl76NL-0">RAMAZAN MUKABELESİ 16. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=fCOJoJlEUis">RAMAZAN MUKABELESİ 17. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=XJD9DxxzC8g">RAMAZAN MUKABELESİ 18. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=jT64JxyH-_o">RAMAZAN MUKABELESİ 19. CÜZ</a>
      <br>
      <a href="https://www.youtube.com/watch?v=U5ny1ywRHxY">RAMAZAN MUKABELESİ 20. CÜZ</a>
       <br>
      <a href="https://www.youtube.com/watch?v=PFdMGDOow60">RAMAZAN MUKABELESİ 21. CÜZ</a>
    </h3>
  </div>
</template>

<script>
  export default {
    name: 'App',
    data() {
      return {
        katilimciMi: false,
        streamyard: 'https://streamyard.com/6nvf8qfayv',
        youtube: 'https://www.youtube.com/watch?v=DOIlC3AzujU'
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

<template>
  <div id="app">
    <loading :active.sync="isLoading"></loading>
    <div id="nav">
      <router-link to="/">Home</router-link>|
      <router-link to="/about">About</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>
export default {
  data () {
    return {
      // 預設關閉
      isLoading: false
    }
  },
  mounted () {
    // // 畫面準備完打開
    // this.isLoading = true
    // // 2秒後關閉
    // setTimeout(() => {
    //   this.isLoading = false
    // }, 2000)
    this.$http.get('')
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

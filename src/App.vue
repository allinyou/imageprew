<template>
  <div id="app">
    <router-view/>
  </div>
</template>
<script>
export default {
  mounted() {
    
  }
};
</script>


<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
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
body{
  margin:0;
}

ul,li{
  padding: 0;
  margin:0;
  list-style: none;
}
.pswp--supports-fs .pswp__button--fs{
  display: none!important;
}
.pswp{
  background-color: black;
}
.pswp__counter,.pswp__button{
  opacity: 1!important;
}
</style>

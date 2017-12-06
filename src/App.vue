<template>
  <div id="app">
    <img src="./assets/logo.png" @click="click">
    <router-view/>
  </div>
</template>

<script>

export default {
  name: 'app',
  methods: {
    click () {
      console.log(this);
      store.commit('increment')
      console.log(store.state.count)
    }
  }
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

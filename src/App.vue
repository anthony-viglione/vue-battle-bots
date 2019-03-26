<template>
  <div id="app">
    <div id="top">
      <button>CREATE</button>
      <section>BATTLE BOTS</section>
      <button>COLLECTION</button>
      <hr>
    </div>
  </div>
</template>

<script>
import Create from './components/Create.vue';
import Collection from './components/Collection';

export default {
  name: 'app',
  data() {

  },
  components: {
    Create,
    Collection
  }
}
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
#top{
  display: flex;
}
</style>

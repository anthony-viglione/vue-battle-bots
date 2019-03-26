<template>
  <div id="app">
    <div id="top">
      <button @click='toggleView'>CREATE</button>
      <section>BATTLE BOTS</section>
      <button @click="toggleView">COLLECTION</button>
    </div>

    <section v-if="showCreate">
      <create/>
    </section>

    <section v-else>
      <collection/>
    </section>

  </div>
</template>

<script>
import Create from './components/Create.vue';
import Collection from './components/Collection';

export default {
  name: 'app',
  data() {
    return{
    showCreate:true
    }
  },
  methods:{
    toggleView: function() {
      this.showCreate = !this.showCreate
    }
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

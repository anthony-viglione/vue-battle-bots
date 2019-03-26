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
    showCreate:true,
    name:'',
    attack:0,
    health:0,
    allBots:[]
    }
  },
  methods:{
    toggleView: function() {
      this.showCreate = !this.showCreate
    },
    addBot: function () {
      const newBot = { name: this.name, attack:this. attack, health:this. health }
      this.allBots.push(newBot)
      this.name = '';
      this.attack = 0;
      this.health = 0;
      this.toggleView();
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

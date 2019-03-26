<template>
<div>
    <h1>CREATE</h1>
    <div>
        <input type="text" placeholder="Bot Name*" v-model="name">
        <input type="number" placeholder="Attack Value*" v-model="attack">
        <input type="number" placeholder="Health Value*" v-model="health">
        <div>
            <button>SUBMIT</button>
            <button>CLEAR</button>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name:"Create",
    data: function () {
        return{
            name:'',
            attack:0,
            health:0,
            allBots:[]

        }
    },
    methods:{
        addBot: function () {
            const newBot = { name: this.name, attack:this. attack, health:this. health }
            this.allBots.push(newBot)
            this.name = '';
            this.attack = 0;
            this.health = 0;

        }
    }
}
</script>

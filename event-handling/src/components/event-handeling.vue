
<script >
import { ref } from 'vue';
export default{
    setup() {
        return{
            name :  ref('abdullah'),
            count : ref(0),
        }
    },

    methods : {
        changeName() {
            this.name = 'Arman';
        },
       increment(){
         this.count += 1
         console.log('this is one')
       },
       decrement(){
         this.count -= 1
       },
       inrmt(num){
        this.count += num
       },
       dremnt(num){
        this.count -= num
       }
    },
    
}
</script>

<template>
    <h3>{{ name }}</h3>
    <div>
        <button @click="changeName" >change the name</button>
        <button v-on:click="name = 'fogozon'" >change the name fogo</button>
        <button v-on:mouseover=" name = 'gobro'">mouse over</button>
    </div>
    <h2>{{ count }}</h2>
    <div>
        <button v-on:click="count += 1">incriment</button>
        <button v-on:click="count -= 1">decriment</button>
    </div>
    <h2>{{ count }}</h2>
    <div>
        <button v-on:click="increment">incriment ff</button>
        <button v-on:click="decrement">decriment</button>
    </div>
    <h2>{{ count }}</h2>
    <div>
        <button v-on:click="inrmt(1)">incriment-1</button>
        <button v-on:click="inrmt(5)">incriment-5</button>
        <button v-on:click="dremnt(1)">decriment-1</button>
        <button v-on:click="dremnt(5)">decriment-5</button>
    </div>
    
</template>



<style scoped>
    .color-green{
        color: green;
    }
    .text-bold{
        font-size: 24px;
        font-weight: bold;
    }
</style>



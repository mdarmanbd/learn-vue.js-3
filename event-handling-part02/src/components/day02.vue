

<script >
export default {
    name: 'App',
    setup() {
        return {
          count : 0,
          name : 'hello',
          
        }
    },
    methods:{
       changeName() {
        this.name = 'rahul roy'
       },
       gopro(event) {
        this.cout = 2,
        console.log('Event',event)
       }
    }
}
</script>

<template>

   <h2>{{ count }}</h2>
   <div>
        <button @click="count += 1">increment</button>
        <button @click="count -= 1">dicrement</button>
        <button @click="gopro">dicrement consol</button>
   </div>

   <h2>{{ name }}</h2>
   <div>
    <button @mousemove="changeName">change name</button>
   </div>
   <div>

   </div>
</template>

<style scoped>
#app{
    text-align: center;
    background: red;
}
.day02{
    width: 100%;
    text-align: center;
    background: rgb(235, 232, 232);
}
.underline{
    text-decoration: underline;
}
.text-24{
    font-size: 24px;
}
.text-italic{
    font-style: italic;
}
.text-green{
    color: rgb(17, 142, 17);
}
.text-red{
    color: rgb(222, 6, 6);
}
</style>
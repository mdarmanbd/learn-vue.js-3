


<template>
    <section class="" style="background: gray;">
        <P style="color:aquamarine;text-align: center;">{{ state }}</P>
        <button @click="incriment">incriment</button>
        <button @click="dicriment">dicriment</button>
        <button @click="zero">zero</button>
        <button @click="multi">multi by 2</button>
        <button @click="divid">divid by 2</button>

    </section>     
</template>
<script>
export default {  
    
    data (){
        return {
           state: 0,
        }
    },
    methods: {
         incriment(){
            this.state = this.state + 5;
        },
        dicriment(){
            this.state = this.state - 5;
        },
        multi(){
            this.state = this.state * 2;
       },
       divid(){
        this.state = this.state / 2;
       },
       zero(){
        this.state = 0
       }
    }
    
}

</script>



<style scoped>
#app{
    text-align: center;
    background: red;
}
#block{
    display: block;
    padding: 3px 5px;
    font-size: 15px;
}
.padding-10{
    padding: 10px;
}
.green{
    color: green;
}
.line-through{
    text-decoration: line-through;
}
#hidden{
    display: none;
}
.color-red{
    color:red;
}
.text-15{
    font-size: 15px;
}
.text-bold{
    font-weight: bold;
}
.pr-5{
    padding-right: 5px;
}
</style>
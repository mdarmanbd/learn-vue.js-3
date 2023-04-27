
<script >
export default {
    setup() {
        return{
            multiplyNumber: 5,
            baseNumber: 10,
        }
    },

    methods : {
        add(){
            return 10+20+30
        },
        digit(a,b,c) {
            return a + b + c
        },
        multiply(num){
          return num * this.multiplyNumber
        },
    },
    
}
</script>

<template>
  <h2 class="color-green">{{ 1 + 2 + 3 }}</h2>
  <h2>{{ 10 + 20 + 20 }}</h2>
  <!--function call-->
  <h2>add the method - {{ add() }}</h2>
  <!--function call through the peramitter-->
  <h2>add more digite - {{ digit( 5,10,10) }}</h2>
<!--multiply the number using the data proparty-->
  <h2>multiply the number by data proparty - {{ multiply(2) }}</h2>
  <!--multiply the number using the data proparty-->
  <h2 class="color-green">multiply the number by data proparty - {{ multiply(baseNumber) }}</h2>
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



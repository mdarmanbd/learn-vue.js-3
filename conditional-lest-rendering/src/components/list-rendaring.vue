
<script >
export default {
    setup() {
        return{
            names : ['plz','click','the button'],
        }
    },
}
</script>

<template>
    <p>arman</p>
    <p>hello i see you devid</p>
    <h2 v-for="name in names" :key="name">{{ name }}</h2>
    <div v-for="name in names" :key="name">
        <p v-if="name === 'the button'" class="color-green text-bold">{{ name }}</p>
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


<!-- 
<script>
export default {
    setup() {
        return {
           number : 'ko',
           condition : true,
           showCondition : true,
        }
    },
}
</script> -->
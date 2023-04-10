



<template>
    <h2 v-if="number === 0">number is zero</h2>
    <h2 v-else-if="number > 0">the number is positive</h2>
    <h2 v-else-if="number < 0">the number is negative</h2>
    <h2 v-else>not a number</h2>
    <div v-if="condition">
        <p>i am a conditiona</p>
        <p>this is my fourth class</p>
    </div>

    <h2 v-show="showCondition">when the condition is false is hidden</h2>
    <h2 v-if="showCondition">besic defference the inspect elements.when the condition is false ,it's ignor the line.</h2>
</template>

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
</script>


<style scoped>

</style>
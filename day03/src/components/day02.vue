

<script >
export default {
    name: 'App',
    setup() {
        return {
            class : 2,
            hello : 'hello world',
            dynamicClass : 'info',
            isPromoted : true,
            isCondtion : false,
        }
    },
}
</script>

<template>
    <div class="day02">
        <p>i am {{ hello }}</p>
        <p v-text="hello"></p>
        <p class="underline text-24">text-decoration is an underline</p>
        <p v-bind:class="dynamicClass">add to the dynamic class by javascript</p> <!--dynamic class add see the inspect-->
        <p class="underline" v-bind:class="dynamicClass">add to the dynamic class by normal class & js</p>
        <p v-bind:class="isPromoted && 'text-italic  text-24' ">applyed the conditional class</p>
        <p v-bind:class="isCondtion ? 'text-green text-24' : 'text-red' ">apply the ternary conditonal operator on a class</p>
        <h3 v-bind:class="['text-24','text-italic','text-green']" style="font-weight:bold;">use the more class on a array</h3>
        <h2 v-bind:class="[isCondtion && 'underline' , isPromoted ? 'text-italic' : 'text-24']">logical & and the ternary operator applye at a time</h2>
        <h2 v-bind:class="{
            promoted : isPromoted,
            condition : !isCondtion,
            'text-italic' : isPromoted,
        }">apply the class on a object model</h2>
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
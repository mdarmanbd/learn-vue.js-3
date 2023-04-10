





<script>
  import { ref } from 'vue'
export default {
    setup() {
         const id = ref('elka')
        return {
            roll : 500,
            name : 'arman',
            greading : 'hello everyone',
            line:'hi birds',
           tagline : '<small>i will see you</small>',
           hack : "<a href='www.google.com'>this is link</a>",
           headingID : 'heading02',
           disabled: true,

           objectOfAttrs : {
                id: 'container',
                class: 'wrapper',
            }
        };
    },
}
</script>

<template>
    <div class="fotball">
        <p :id="id">Arsenal:1-2:BVB</p>
        <p>{{ name }}</p>
        <p> <span v-html="greading" style="color:aqua"></span> </p>
        <p v-bind:id="roll"></p>
        <p v-text="line"></p>
        <p v-html="tagline"></p>
        <p v-html="hack"></p>
        <p v-bind:id="headingID">Heading</p>
        <button :disabled="disabled">click here</button>
        <p v-bind="objectOfAttrs">s</p>
    </div>
    <div>
        <p v-html="tagline" style="color:red"></p>
    </div>
</template>

<style scoped>
template{
    width: 100%;
}
.fotball{
    background: rgb(6, 129, 6);
    width: 100%;
}
p{
    font-size: 20px;
    font-weight: bold;
    color: white;
}
.color-red{
    color: red;
}
#one{
    background: rebeccapurple;
}
</style>
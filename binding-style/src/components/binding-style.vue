

<script>
export default {
    setup() {
        return {
            info : '#14C1AF',
            font20 : '25px',
            golore : '#1475C1',
            styleObject : {
                color : '#C12C14',
                background : '#C19214',
                padding : '28px',
                marginTop : '10px',
            },
            secondObject : {
                borderRadius : '5px',
                fontStyle : 'italic',
                color : 'white',
            }
        }
    },
}
</script>

<template>
    <div>
        <h3 v-bind:style="{
            fontSize : font20, 
            background : golore, 
            color : '#C11414',  // direct css appaly
        }">using the inline css</h3>
        <h3 v-bind:style="styleObject">using the object style</h3>
        <h3 v-bind:style="[styleObject , secondObject]">using the multipul object style</h3>
    </div>
</template>

<style scoped>

</style>
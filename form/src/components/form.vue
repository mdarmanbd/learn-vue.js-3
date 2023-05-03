
<script setup>
    import { ref } from 'vue'
    const message = ref('')
    const multilineMessage = ref('')
    const checkTrue = ref('true');
    const checkFalse = ref('false');
    const checkedName = ref([]);
    const picked = ref('one');
    const select = ref('');
    const multiSelect = ref([""]);
    const selected = ref('');
    const options = ref([
        {text: 'one', value: 'A'},
        {text: 'two', value:'B'},
        {text:'three', value:'C'}
    ]);

</script>

<template>
<!--basic staturater-->    
   <P class="color-green text-bold"> 1.basic staturater :-</P>
   <p>this is message: {{ message }}</p>
   <input class="padding-10 color-green text-15" type="text" v-model="message" placeholder="eddit">
<!--multiline message-->
   <p class="color-green text-bold"> 2.multiline message :-</p>
   <p>this is multiline message: {{ multilineMessage }}</p>
   <textarea class="padding-10 color-green text-15" type="text" v-model="multilineMessage" placeholder="comments"></textarea>
<!--checkbox-->
    <p class="color-green text-bold"> 3.check box</p>
    <input type="checkbox" v-model="checkTrue">
    <label>{{ checkTrue }}</label>
    <input type="checkbox" v-model="checkFalse">
    <label>{{ checkFalse }}</label>
<!--checkbox in array-->
<div>checked name in array : {{ checkedName }}</div>
<input type="checkbox" value="bangladesh" v-model="checkedName">
<label for="bangladesh" class="pr-5">bangladesh</label>
<input type="checkbox" value="india" v-model="checkedName">
<label for="india" class="pr-5">india</label>
<input type="checkbox" value="pakistan" v-model="checkedName">
<label for="pakistan" class="pr-5">pakistan</label>
<!--radio-->
<div class="color-green text-bold">picked: {{ picked }}</div>
<input type="radio" value="one" v-model="picked">
<label class="pr-5" for="one">one</label>
<input  type="radio" value="two" v-model="picked">
<label class="pr-5" for="two">two</label>

<!--select option-->
<div class="color-green text-bold"> 4.select : {{ select }}</div>
<select v-model="select">
    <option disable value="">plz select one option</option>
    <option>a</option>
    <option>b</option>
    <option>c</option>
</select>

<!--multi select-->
<div class="color-green text-bold"> 5.multi select : {{ multiSelect }}</div>
<select v-model="multiSelect" multiple>
    <option>A</option>
    <option>B</option>
    <option>C</option>
</select>
<!--selected options-->
<p class="color-green text-bold" style="margin-top: 20px;"> 6.selected a option</p>
<select v-model="selected" >
    <option v-for="option in options" :value="option.value">
    {{ option.text }}   
    </option>
</select>
<div>selected: {{ selected }}</div>



</template>

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
.color-green{
    color: green;
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
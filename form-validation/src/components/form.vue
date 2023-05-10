


<template>
       
        <div class=" bg-slate-300 w-1/2 m-auto px-4 h-auto">
            <p class="text-center font-sans font-bold text-orange-600 py-3">Add a new blog</p>
            <div class="py-2">
                <p class="text-blue-900 font-normal font-19 pb-2">Blog title :</p>
                <input type="text" v-model="formData.title" placeholder="write a blog">
                <p class="color-red" v-if="formData.showTitle">wrong title</p>
            </div>
            <div class="py-2">
                <p class="text-blue-900 font-normal font-19 pb-2">Blog body :</p>
                <input type="text" v-model="formData.body">
                <p class="color-red" v-if="!formData.body  || formData.body.length < 2 ">plz put the vaild text</p>
            </div>
            <div class="py-2">
                <p class="text-blue-900 font-normal font-19 pb-2">Author :</p>
                <input type="text" v-model="formData.author">
                <p class="color-red" v-if=" formData.showAuthor ">put the vaild author name at lest 10 words</p>
            </div>
            <div class="py-2">
                <p class="text-blue-900 font-normal font-19 pb-2">Number :</p>
                <input type="text" v-model="formData.phoneNumber">
                <p class="color-red" v-if="formData.showNumber">phone number must be 2 digit</p>
            </div>
            <div class="py-2">
                <p class="text-blue-900 font-normal font-19 pb-2">Email :</p>
                <input type="text" v-model="formData.email">
                <p class="color-red" v-if="formData.emailWorning">plz put vaild email@</p>
            </div>
            <div class="py-2 text-center">
                <button @click="submit">save</button>
            </div>
            
        </div>

</template>

<script>
export default {        
    data (){
        return{
            showTitle : true,
            showElement: false,
            formData: {
                title: '',
                showTitle: false,
                body: '',
                author: '',
                showAuthor : false,
                phoneNumber : '',
                showNumber: false,
                email : '',
                emailWorning : false
            }
        }
    },


    methods: {
        submit() {
           if(this.formData.title.length < 2){
                this.formData.showTitle = true
           }else{
            this.formData.showTitle = false
           }

           if(this.formData.author.length < 2 || this.formData.author.length > 10 ){
                this.formData.showAuthor = true
           }else{
               this.formData.showAuthor = false
           }

           if(this.formData.phoneNumber.length != 2 ){
              this.formData.showNumber= true
           }else{
            this.formData.showNumber= false
           }

           if(this.formData.email.indexOf('@') == -1 || this.formData.email.length > 8){
                this.formData.emailWorning = true
           }else{
                this.formData.emailWorning = false
           }

           if(this.formData.title.length < 2 || this.formData.author.length < 2 || this.formData.author.length > 10 || this.formData.phoneNumber.length != 2 || this.formData.email.indexOf('@') == -1 || this.formData.email.length > 8 ){
                alert('plz give correct informetion')
           }else{
                alert('successfully submit')
                this.formData.title = '',
                this.formData.body = '',
                this.formData.author = '',
                this.formData.phoneNumber = '',
                this.formData.email = ''
           }


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
.color-green{
    color: green;
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
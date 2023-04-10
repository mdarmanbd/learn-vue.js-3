





<template>
    <!--single array use-->
    <h2 v-for="(nam , index) in names" :key="nam">{{ index }} {{ nam }} </h2>
    <h2 v-for="name in fullNames" :key="name">{{ name.first }} {{ name.last }}</h2>
    <!--double array use-->
        <div v-for="actor in actors" :key="actor.name">
            <h2>{{ actor.name }}</h2>
            <h3 v-for="movie in actor.movies" :key="movie">{{ movie }}</h3>
        </div>
    <!-- index , key , value applay at a time.  -->
    <h2 v-for="(value , key , index) in info" :key="value">{{ index }} {{ key }} {{ value }}</h2>
    <!--horizontal line or line break use-->
    <div v-for="name in names" :key="name">
        <h4>{{ name }}</h4>
        <hr/>
    </div>
</template> 

<script>
export default {
    setup() {
        return {
          names : ['hello','bird','i','see','you'],
          fullNames:[
            {first : 'object' , last : 'array'},
            {first : 'vue' , last : 'js'},
            {first : 'click' , last : 'me'}
          ],
          actors : [
            {
                name : 'christan bale',
                movies : ['batman','the spy'],
            },

            {
                name : 'di caporio',
                movies : ['titanik','blood dimon'],
            },
            
        ],
        
        info : {
            name : 'joba',
            title : 'house wife',
            age : 37,
        }

        }
      
    }
}
</script>


<style scoped>

</style>
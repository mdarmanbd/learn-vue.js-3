


<template>
    <!-- <button class="color-red" @click="increment">{{ number }}</button> -->
    <div :style="headerContainerObject">
        <form>
            <input type="date" :style="inputDateObject">
            <label>collection: </label>
            <input v-model="collectionNumber" type="number" :style="inputNumberObject" placeholder="collection" required>
            <label>sales: </label>
            <input v-model="salesNumber" type="number" :style="inputNumberObject" placeholder="sales" required>
        </form>
      
    </div>
    <div style="display: flex; justify-content: space-around;width: 100%;">
        <div style="background: #D7D6D2;width: 30%;padding-top: 10px;">
            <div :style="stockStyle">
                <h2>stock</h2>
                <p> {{ stock() }} </p>
            </div>
            
            <div :style="stockStyle">
                <h2>sales</h2>
                <p>{{ (salesNumber) }}</p>
            </div>
           
            <div :style="stockStyle">
                <h2>price</h2>
                <p >{{ price() }}</p>
            </div>
        </div>

        <div style="width: 70%;">
            <div :style="containerObject">
                <div :style="colunmObject">
                        <h2>food</h2>
                        <p>schedule</p>
                <ul :style="unorderListObject">
                    <li v-for="time in foodArray" :key="time">{{ time }}</li>
                    
                </ul>
                </div>
                <div :style="colunmObject">
                    <h2>medicine</h2>
                    <p>schedule</p>
                <ul :style="unorderListObject">
                    <li v-for="(time,index) in medicineArray" :key="index">{{ time }}</li>
                </ul>
                </div>
            </div>

            <div :style="containerObject">
                <div :style="colunmObject">
                    <h2>lighting</h2>
                    <p>schedule</p>
                    <ul :style="unorderListObject">
                    <li v-for="(time,index) in lightArray" :key="index">{{ time }}</li>
                    </ul>          
                </div>
                <div :style="colunmObject">
                    <h2>water</h2>
                    <p>schedule</p>
                    <ul :style="unorderListObject">
                        <li v-for="(time,index) in watterArray" :key="index">{{ time }}</li>
                    </ul> 
                </div>
            </div>

            <div :style="containerObject">
                <div :style="colunmObject">
                    <h2>egg collection</h2>
                    <p>schedule</p>
                    <ul :style="unorderListObject">
                        <li v-for="time in collectionArray" :key="time"> {{ time }}</li>
                    
                    </ul>
                </div>
                <div :style="colunmObject">
                    <h2>litter change</h2>
                    <p>schedule</p>
                    <ul :style="unorderListObject">
                    <li v-for="time in litterArray" :key="time">{{ time }}</li>
                    </ul>
                </div>
            </div>
            <div :style="containerObject">
                <div :style="colunmObject">
                    <h2>sales</h2>
                    <p>schedule</p>
                    <ul :style="unorderListObject">
                        <li v-for="(time,index) in salesArray" :key="index">{{ time }}</li>
                    
                    </ul>
                </div>
                <div :style="colunmObject">
                    <h2>stock</h2>
                    <p>schedule</p>
                    <ul :style="unorderListObject">
                        <li v-for="(time,index) in stockArray" :key="index">{{ time }}</li>

                    </ul>
                </div>
            </div>
        </div>
    
    </div>
    
</template>
<script>
export default {  
    data (){
        return {
            collectionNumber: 0 ,
            salesNumber: 0,
            number: 10,
            
            red: 'color-red',
            name:['food','medicine','lighting', 'temprature','egg colection','litter change','sales','stock'],
            foodArray:['8am','12pm','8pm'],
            medicineArray:['8am','8pm'],
            lightArray:['5pm','9pm'],
            collectionArray:['5pm'],
            litterArray:['8pm'],
            watterArray:['8am','12pm','8pm'],
            salesArray:['12pm','9pm'],
            stockArray:['8pm'],

            stockStyle:{
                paddingTop: '10px',
                textAlign: 'center',
                background: '#F7F4EC',
                color: 'black',
            },
            headerContainerObject:{
                paddingTop: '30px',
                paddingBottom: '8px',
                display: 'flex',
                justifyContent: 'center'
            },
            inputDateObject:{
                padding: '5px 10px',
                outline: 'none',
                marginRight:'10px'
            },
            inputNumberObject:{
                padding: '5px 5px',
                width: '100px',
                marginLeft: '5px',
                outline: 'none'
            },
            containerObject: {
                display:'flex',
                paddingTop: '10px'
            },
            colunmObject: {
                height: '250px',
                width: '550px',
                marginLeft:'10px',
                backgroundColor:'#dcdcdc',
                color:'black',
                textAlign:'center'
            },
            unorderListObject: {
                listStyle: 'none',
                paddingTop:'5px',
                paddingLeft: '10px',
                fontSize: '16px',
                textAlign: 'left'
            },
        }
    },
    methods: {
        increment() {
            this.number = this.number + 1; // 1 > 1, 2>2 , 3>3 , 4>4 , 5>5, 6>6, 7>7 , 8>8 , 9>9, 10>10, 11>0 
            if(this.number >= 11){
                this.number = 0
            }
        },

       stock(){
            return (10 + this.collectionNumber) - (this.salesNumber)
       },
       price(){
            return (15 * (this.salesNumber))
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
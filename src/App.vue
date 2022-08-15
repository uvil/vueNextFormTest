<script >
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'

// my-component.js
export default {
  data() {
    return { count: 1 }
  },
  methods: {

    next() {
      
      if(++this.count >=4)
        this.count=1

      console.log(this.count)
      
    }
  },
}


</script>

<template>
  <h1>Fyll i rutorna stegvis</h1>

  <form action="" id="form1" @submit.prevent="next">
  
   <fieldset :disabled="count!=1">
    <div>Steg 1</div>
    <div><input type="text" name="" id="" placeholder="text" ></div>
    <button type="submit"  >Till nästa steg</button>
   </fieldset>

   <div v-if="count!=1" class="overlay"></div>
  </form>

  <form action="" id="form2" @submit.prevent="next">
   <fieldset :disabled="count!=2">
    <div>Steg 2</div>
    <div><input type="text" name="" id="" placeholder="text" ></div>
    <button type="submit">Till nästa steg</button>
   </fieldset> 

   <div v-if="count!=2" class="overlay"></div>

  </form>
 

 <form action="" id="form3" @submit.prevent="next">
   <fieldset :disabled="count!=3">
    <div>Steg 3</div>
    <div><input type="text" name="" id="" placeholder="text" ></div>
    <button type="submit">Till nästa steg</button>
  </fieldset>

   <div v-if="count!=3" class="overlay"></div>

  </form>
 
 
</template>

<style scoped>
  h1{
    font-family: sans-serif;
    margin-bottom: 20px;
    text-align: center;
  }
  form{
    border: 1px solid grey;
    padding: 20px;
    border-radius: 10px;
    background: #eee; 
    text-align: center;
    margin-bottom: 30px;
     }

    form div{
      margin-bottom: 10px;
    }

    form fieldset{
      border: none;
    }

    .overlay{
      background: rgba(255,255,255,0.7);
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      border-radius: 10px;
    }

    #form1{ background: #cad2c5;}
    #form2{ background: #84a98c;}
    #form3{ background: #52796f;}

</style>

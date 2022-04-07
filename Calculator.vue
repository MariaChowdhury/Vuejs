<script setup>

</script>

<template>
  <div class="calculator">
     <div > Principal (P): $</div>
     <input v-model="text">
     <div> Annual Rate (R): %</div>
     <input v-model="text">
     <div> Compound (n):</div>
     <input v-model="text">
     <div> Time (t in years):</div>
     <input v-model="text">
     <button @click="calculate()" class="display" > Calculate</button>
     <div></div>
     <div>Answer:{{current}}</div>
     <div> </div>
     
  </div>
  
</template>

<script>
export default{
  data(){
    return{
      current: '123'
    }
    
  },
  methods:{
    clear() {
       this.current='';
    },
    calculate(){
      
    }
  }
}
  
</script>

<style scoped>
.calculator{
  width: 400px;
  display: grid;
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  grid-template-columns: repeat(2,150px);
  grid-template-rows: (1,50px);
}
.display{
  color: rgb(7, 7, 7);
  grid-column: 2;
  margin: 5px;
}

</style>

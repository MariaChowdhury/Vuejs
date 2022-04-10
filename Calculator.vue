<script setup>

</script>

<template>
  <div class="calculator">
     <div > Principal (P): $</div>
     <input :value="form.principal" @change="update_principal" type="number" class="form-control" name="principal" id="principal" placeholder="principal">

     <div> Annual Rate (R): %</div>
     <input :value="form.rate" @change="update_rate" type="number" class="form-control" name="rate" id="rate" placeholder="rate">

     <div> Compound (n):</div>
     <input :value="form.compound" @change="update_compound" type="number" class="form-control" name="compound" id="compound" placeholder="compound">

     <div> Time (t in years):</div>
     <input :value="form.year" @change="update_year" type="number" class="form-control" name="year" id="year" placeholder="year">

     <button @click="calculate()" class="display" > Calculate</button>
     <div>Answer:</div>
     <input :value="form.result" @change="update" type="number" class="form-control" name="result" id="result" placeholder="Answer">

  </div>
 
  
</template>

<script>
export default{
 
  data(){
    return{
       form: {
        principal: 0,
        rate: 0,
        compound: 0,
        year: 0
      }
      
    }
  },
  methods:{
    clear() {
       this.current='';
    },
      update_principal(event) {
        this.form.principal = event.target.value 
      },
      update_rate(event) {
        this.form.rate = event.target.value
      },
      update_compound(event) {
        this.form.compound = event.target.value
      },
      update_year(event) {
        this.form.year = event.target.value
      },
    
    calculate(){
      this.form.result=Number(this.form.principal)+
      Number(this.form.rate)+Number(this.form.compound)+Number(this.form.year)
      
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

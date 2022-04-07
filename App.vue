<script setup>
import Calculator from './components/Calculator.vue'
</script>

<template>
  <header>
    <h1 class="green" >Let's Calculate Compound Interest</h1>
    <div class="black"> </div>
    <div class="wrapper">
      <Calculator />
    </div>
  </header>
</template>

<style>
@import './assets/base.css';

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
}
.black {
  margin: 50px;
  text-decoration: none;
  color: rgb(15, 15, 15);
  transition: 0.4s;
}



</style>

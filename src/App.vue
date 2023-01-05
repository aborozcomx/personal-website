<template>
  <main>
    <div class="card">
        <img :src="personalInformation.image" :alt="personalInformation.username">
        <h1>{{ personalInformation.username }}</h1>
        <h4>{{ personalInformation.description }}</h4>
      </div>
  </main>
</template>

<script setup>
import logo from '@/assets/logo.jpg'
import { reactive } from 'vue'

const personalInformation = reactive({
  username: '@aborozcomx',
  description: 'Frontend Developer at Devtzal',
  image: logo
});

</script>

<style scope>
@import './assets/base.css';

main{
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
}

.card{
  border-radius: 12px;
  background: white;
  padding: 10px;
  width: 468px;
}

.card img{
  border-radius: 50%;
  display: block;
  margin: -50px auto 0;
  width: 85px;
  height: 85px;
}
h1, h4{
  text-align: center;
}

@media screen and (max-width: 468px){
  .card{
    width: 320px;
  }
}
</style>

<script setup>

import Componente from "./components/Componente.vue";

</script>

<template>

  <div class="interface_box">
    <h1 class="title">Calculadora VueJS</h1>
    <Componente class="componente"/>
  </div>

</template>

<style scoped>

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  color: #fff;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.interface_box{
  max-width: 480px;
  width: 90%;
  margin: 64px auto 0;
  text-align: center;
  background-color: #156;
  padding: 32px;
  border-radius: 16px;
  box-shadow: 0px 4px 8px #000;
}

.title{
  margin-bottom: 32px
}

</style>
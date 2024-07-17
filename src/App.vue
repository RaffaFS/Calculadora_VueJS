<script setup>

  import { reactive } from "vue";

  const estado = reactive({
    num1: 0,
    num2: 0,
    operacao: '',
    res: 0
  })

  function operar(){
    const a = estado.num1
    const b = estado.num2
    
    switch(estado.operacao){
      case 'soma':
        estado.res = a+b
        return estado.res
      case 'subtracao':
        estado.res = a-b
        return estado.res
      case 'multiplicacao':
        estado.res = a*b
        return estado.res
      case 'divisao':
        estado.res = a/b
        return estado.res
    }
  }

</script>

<template>

  <div class="interface_box">
    <h1>Calculadora VueJS</h1>
    <div class="type_box">
      <label for="operacao">Selecione o tipo de operação:</label>
      <select name="operacao" v-model="estado.operacao" @change="operar()" >
        <option value="soma">Soma</option>
        <option value="subtracao">Subtração</option>
        <option value="multiplicacao">Multiplicação</option>
        <option value="divisao">Divisão</option>
      </select>
    </div>
    <div class="input_box">
      <input @keyup="operar()" v-model="estado.num1" type="number" maxlength="6" minlength="1">
      <input @keyup="operar()" v-model="estado.num2" type="number" maxlength="6" minlength="1">
    </div>
    <div class="result_box">
      <p>
        Resultado: {{ estado.res }}
      </p>
    </div>
  </div>

</template>

<style scoped>
</style>
<script setup>
import { ref } from "vue";
const valor2 = ref("");
const valor1 = ref("");
</script>
<template>
  <main>
    <h1>Calculadora de Gorjetas</h1>

    <label>Valor da Conta?</label>
    <input type="number" v-model="valor1" />
    <label>Como foi o Serviço?</label>
    <select name="Qualidade do serviço" v-model="gorjeta" id="asd">
      <option value="5">5% (Péssimo)</option>
      <option value="10">10% (Ruim)</option>
      <option value="15">15% (Ok)</option>
      <option value="20">20% (Bom)</option>
      <option value="25">25% (Mais que Bom)</option>
      <option value="30">30% (Perfeito)</option>
    </select>
    <label>Quantas pessoas irão dividir?</label>
    <input type="number" v-model="valor2" />
    <h4>
      Valor da conta: R${{ (valor1 * (1 + gorjeta / 100)) / valor2 }} para cada
      pessoa
    </h4>
  </main>
</template>

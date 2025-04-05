<script setup>
import Calculator from './components/Calculator.vue'
</script>

<template>
  <header>
    <h1 class="mt-5">Calculadora Aritmética</h1>
  </header>

  <main>
    <Calculator />
  </main>
</template>

<style scoped>
header {
  text-align: center;
  margin-bottom: 2rem;
}

.logo {
  display: block;
  margin: 0 auto 1rem;
}

h1 {
  font-size: 1.5rem;
  color: #333;
}
</style>

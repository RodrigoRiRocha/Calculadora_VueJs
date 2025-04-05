<script setup>
import { ref, computed } from 'vue'

const num1 = ref(0)
const num2 = ref(0)
const operation = ref('+')

const result = computed(() => {
    const a = parseFloat(num1.value)
    const b = parseFloat(num2.value)

    switch (operation.value) {
        case '+':
            return a + b
        case '-':
            return a - b
        case '*':
            return a * b
        case '/':
            return b !== 0 ? a / b : 'Erro: Divisão por zero'
        default:
            return 'Operação inválida'
    }
})
</script>

<template>
    <div class="calculator container mt-5">
        <div class="mb-3">
            <label for="num1" class="form-label">Número 1:</label>
            <input id="num1" type="number" v-model="num1" class="form-control" />
        </div>

        <div class="mb-3">
            <label for="num2" class="form-label">Número 2:</label>
            <input id="num2" type="number" v-model="num2" class="form-control" />
        </div>

        <div class="mb-3">
            <label for="operation" class="form-label">Operação:</label>
            <select id="operation" v-model="operation" class="form-select">
                <option value="+">+</option>
                <option value="-">-</option>
                <option value="*">*</option>
                <option value="/">/</option>
            </select>
        </div>

        <div class="mt-4">
            <h3 class="text-primary">Resultado: {{ result }}</h3>
        </div>
    </div>
</template>

<style scoped>

</style>
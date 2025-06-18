<script setup>
import { ref } from 'vue'
const mensaje = ref('')
const n1 = ref(6)
const n2 = ref(50)

const fSumar = () => {
    let suma = n1.value + n2.value
    mensaje.value = `La suma es : ${suma}`
}

const fRestar = () => {
    let resta = n1.value - n2.value
    mensaje.value = `La resta es : ${resta}`
}
const fMultiplicar = () => {
    let multi = n1.value * n2.value
    mensaje.value = `La multi es : ${multi}`
}

const fDividir = () => {
    let divi = n1.value / n2.value
    mensaje.value = `La divi es : ${divi}`
}
//Operaqciones
</script>

<template>
    <div>
        <h1>{{ mensaje }}</h1>
        <button @click="fSumar" class="btn btn-primary m-1"> SUMAR</button>
        <button @click="fRestar" class="btn btn-primary m-1"> RESTAR</button>
        <button @click="fMultiplicar" class="btn btn-primary m-1"> MULTIPLICAR</button>
        <button @click="fDividir" class="btn btn-primary m-1"> DIVIDIR</button>
    </div>
</template>

<style scoped></style>
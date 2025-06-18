<script setup>
import { ref } from 'vue'
const mensaje = ref('')
const n1 = ref(0)
const n2 = ref(0)
const nombre = ref('')
//v-model : directiva fundamental de vue, 
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
        <form class="form-control">
            <div class="row g-2 align-items-end">
                <div class="mb-3 col-md-6">
                    <label for="n1">Ingresa tu nombre</label>
                    <input v-model="nombre" placeholder="Escribe tu nombre" class="form-control" type="text">
                    <p>Hola, {{ nombre }}</p>
                </div>

            </div>
            <div class="row g-2 align-items-end">
                <div class="mb-3 col-md-6">
                    <label for="n1">Ingresa un numero</label>
                    <input v-model.number="n1" class="form-control" type="number">
                </div>
                <div class="mb-3 col-md-6">
                    <label for="n2">Ingresa un numero</label>
                    <input v-model.number="n2" class="form-control" type="number">
                </div>
            </div>


        </form>
        <h1>{{ mensaje }}</h1>
        <button @click="fSumar" class="btn btn-primary m-1"> SUMAR</button>
        <button @click="fRestar" class="btn btn-primary m-1"> RESTAR</button>
        <button @click="fMultiplicar" class="btn btn-primary m-1"> MULTIPLICAR</button>
        <button @click="fDividir" class="btn btn-primary m-1"> DIVIDIR</button>
    </div>
</template>

<style scoped></style>
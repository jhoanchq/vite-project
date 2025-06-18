<script setup>
import { ref } from 'vue'
const mensaje = ref('Sumar')
const cambiarMensaje = () => {
    let suma = 6 + 10
    mensaje.value = `La suma es : ${suma}`
}
</script>

<template>
    <div>
        <h1>{{ mensaje }}</h1>
        <button @click="cambiarMensaje" class="btn btn-primary"> Cambiar Mensaje</button>
    </div>
</template>

<style scoped></style>
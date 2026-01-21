<script setup>
    defineProps({
        texto: {
            type: String,
            required: true
        }
    })

    const emitClick = (event) => {
        emitClick('clickBoton', null)
    }
</script>
<template>
    <button @click="$emit('clickBoton')">
        {{ texto }}
    </button>
</template>
<style scoped>
    button {
        background-color: red;
        color: white;
        padding: 10px;
        border-radius: 5px;
    }
</style>
<script setup>
import { ref } from 'vue'

const name = ref('') // data reaktif
</script>

<template>
  <input v-model="name" placeholder="Ketik nama kamu" />
  <p>Halo, {{ name }}!</p>
</template>

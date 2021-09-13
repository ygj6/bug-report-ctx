<script setup>
import { ref } from 'vue'

const msg = ref('Hello World!')
const _ = ref(0)
</script>

<template>
  <h1>{{ msg }}</h1>
  <input v-model="msg" ref="input">
  <!-- in dev mode will report 'Uncaught TypeError: Cannot read property '__isScriptSetup' of undefined',work fine in prod mode -->
  <button @click="$refs.input.focus()">
    Focus $refs.input
  </button>
</template>
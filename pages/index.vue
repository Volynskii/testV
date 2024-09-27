<template>
  <div>
    <h1>Pinia Counter</h1>
    <p>Count: {{ counter.count }}</p>
    <button @click="counter.increment">Increment</button>
    <button @click="counter.decrement">Decrement</button>
  </div>
</template>

<script setup lang="ts">
import { useCounterStore } from '~/stores/counter'

const counter = useCounterStore()
</script>

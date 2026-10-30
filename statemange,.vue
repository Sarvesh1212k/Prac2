
<template>
  <div>
    <h1>Pinia State Management</h1>

    <h2>Count: {{ counter.count }}</h2>

    <button @click="counter.increment()">Increment</button>
    <button @click="counter.decrement()">Decrement</button>
    <button @click="counter.reset()">Reset</button>
  </div>
</template>

<script setup>
import { defineStore } from 'pinia'

const useCounterStore = defineStore('counter', {
  state: () => ({
    count: 0
  }),

  actions: {
    increment() {
      this.count++
    },

    decrement() {
      this.count--
    },

    reset() {
      this.count = 0
    }
  }
})

const counter = useCounterStore()
</script>

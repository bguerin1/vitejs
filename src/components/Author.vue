<script setup>
import { reactive, computed } from 'vue'

const author = reactive({
  name: 'John Doe',
  books: [
    'Vue 2 - Brosseau',
    'Vue 3 - Test',
    'Vue 4 - Démo'
  ]
})

const publishedBooksMessage = computed(() => {
  return author.books.length > 0 ? 'Yes' : 'No'
})
</script>

<template>
  <p>
    Auteur : {{author.name}}
  </p>
  
  <ul>
    <li v-for="book in author.books">{{ book }}</li>
  </ul>

  <p>
  Nombre de livre : <span>{{ publishedBooksMessage }}</span>
  </p>
</template>
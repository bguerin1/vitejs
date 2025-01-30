<script setup>
    import { reactive, computed, ref } from 'vue'

    const search = ref("");
    
    const author = reactive({
      name: 'John Doe',
      books: [
        'Vue 2 - Cours Brosseau',
        'Vue 3 - Cours Test',
        'Vue 4 - Cours Démo',
        'Le seigneur des anneaux',
        'La plateforme',
        'Le labyrinthe'
      ]
    })

    const publishedBooksMessage = computed(() => {
      return filteredBooks.value.length
    })

    const filteredBooks = computed(() => {
      if(search.value != ""){
       return author.books.filter(it => it.includes(search.value));
      } else {
        return author.books;
      }
    })
</script>

<template>
  <p>
    Auteur : {{author.name}}
  </p>
  
  <input type="text" v-model="search" placeholder="Rechercher un livre" />

  <ul>
    <li v-for="book in filteredBooks">{{ book }}</li>
  </ul>

  <p>
  Nombre de livre : <span>{{ publishedBooksMessage }}</span>
  </p>
</template>
<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import Track from './components/Track.vue';
import Author from './components/Author.vue';
import Test from './components/Test.vue';
import Card from './components/Card.vue';
import ButtonP from './components/ButtonP.vue';
import Navbar from './components/Navbar.vue';
</script>

<template>
  <div>
    <a href="https://vite.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <div>
    <HelloWorld msg="Vite + Vue" />
    <Track />
    <Author />
    <Test />
  </div>
  <h1>-----------------------------------</h1>
  <div>
    <Card>Voici une card et son contenu</Card>
    <br>
    <ButtonP label="Clique moi !" color="btn btn-primary"/>
    <Navbar />
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>

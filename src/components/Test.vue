<template>
    <h1>Ceci est un composant</h1>
    <button type="button">{{ compteur }}</button>
    <input type="button" @click="compteur++" value="Cliquez ici !">
    <input type="button" @click="compteur--" value="Cliquez ici !">
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {compteur:0};
  },
});
</script>
  
<style scoped>
  h1 {
      color: red;
  }
</style>
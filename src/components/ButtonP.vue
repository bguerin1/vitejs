<template>
    <button :class="color"> {{ label }} </button>
</template>
  
<script setup lang="ts">
  import { defineProps } from "vue";
  
  const props = defineProps({
    label: {
      type: String,
      required: true,
    },
    color: {
      type: String,
      required: true,
    },
  });
</script>
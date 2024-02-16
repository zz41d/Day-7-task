<template>
    <input type="text" v-model="title" @keypress.enter="save" />
    <p>Total Notes: {{ totalNotes }}</p>
  </template>
  
  <script setup>
  import { useStore } from "vuex";
  import { ref, computed } from "vue";
  
  const store = useStore();
  const title = ref("");
  const totalNotes = computed(() => store.getters.totalNotes);
  
  const save = () => {
    store.dispatch("saveNote", title.value);
    title.value = "";
  };
  </script>
  
<template>
    <ul>
      <li v-for="(note, index) in notes" :key="index">{{ note }}</li>
    </ul>
  </template>
  
  <script setup>
  import { useStore } from "vuex";
  import {ref, computed } from "vue";
  
  const store = useStore();
  const notes = computed(() => store.state.notes);
  </script>
  
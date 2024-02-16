<template>
  {{ $store.state.title }}
  <Notes />
  <AddNewNote />
</template>

<script setup>
import Notes from "./components/Notes.vue";
import AddNewNote from "./components/AddNewNote";
</script>

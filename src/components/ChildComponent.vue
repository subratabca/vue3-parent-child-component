
  <script setup>
  //import { defineProps, defineEmits } from 'vue';
  
  const props = defineProps({
    message: String,
  });
  
const emit = defineEmits(['messageEmitted']);

const emitMessage = () => {
  const customMessage = 'Hello from Child!';
  emit("messageEmitted",customMessage);
};
  </script>

<template>
    <div>
      <h3>Child Component</h3>
      <p>Received message from parent: {{ message }}</p>
      <button @click="emitMessage">Emit Message</button>
    </div>
  </template>
  

  
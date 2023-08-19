<script setup>
//import { defineProps, ref } from 'vue';
import { ref } from 'vue';
import ChildComponent from './ChildComponent.vue';

const props = defineProps({
  message: String,
});

const receivedMessage = ref('');

const handleMessageEmitted = (customMessage) => {
  receivedMessage.value = customMessage;
};
</script>


<template>
  <div>
    <h2>Parent Component</h2>
    <p>Message from child: {{ receivedMessage }}</p>
    <ChildComponent :message="message" @messageEmitted="handleMessageEmitted" />
  </div>
</template>



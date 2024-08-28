<script setup lang="ts">
import { ref, computed } from "vue";
import Card from "./Card.vue";


const userInput = ref("もも\nみかん\nすいか\nなし\nバナナ");
const lines = computed(() => {
  return userInput.value.split(/\r?\n/);
});

const openWindow = () => {
  window.open("./print_page.html", "newwindow", "width=800,height=890");
};
</script>

<template>
  <textarea id="user-input" v-model="userInput"></textarea>
  <div id="result">
    <card :content="line" v-for="(line, idx) in lines" :key="idx">
    </card>
  </div>
  <button @click="openWindow">HIRAKU</button>
</template>

<style scoped>
#result {
  display: none;
}
#user-input {
  height: 200px;
  padding: 6px;
  display: block;
}
button {
  display: block;
  margin: 1em auto;
}
</style>


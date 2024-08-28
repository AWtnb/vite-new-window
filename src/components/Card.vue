<script setup lang="ts">
const props = defineProps<{
  content: string;
}>();
</script>

<template>
  <section class="sheet">
    <div class="box">
      {{ props.content }}
    </div>
  </section>
</template>

<style scoped></style>

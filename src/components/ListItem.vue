<template>
  <div>
    <li>{{ task }}</li>
    <button v-on:click="$emit('remove')">Deletar</button>
  </div>
</template>

<script>
export default {
  name: "ListItem",
  props: {
    task: String,
  },
  emits: ['remove']
};
</script>

<style scoped>
    div {
        display: flex;
        justify-content: space-around;
    }
</style>
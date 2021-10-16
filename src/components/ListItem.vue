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
        justify-content: space-between;
        max-width: 300px;
        align-items: center;
        margin: 5px auto;
        background: #2c3e50;
        border-radius: 5px;
        box-shadow: 0 0 2px 1px #d0d0d0;
        padding: 15px;
        color: whitesmoke;
    }
</style>
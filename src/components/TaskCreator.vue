<template>
  <div>
      <input v-model="newTask"/>
      <button v-on:click="addNewTask">Adicionar Tarefa</button>
  </div>
</template>

<script>
export default {
    name: 'TaskCreator',
    emits: ['add'],
    methods: {
        addNewTask(){
            this.$emit('add', this.newTask);
            this.newTask= '';
        }
    },
    data() {
        return {
            newTask: '',
        }
    }
}
</script>

<style>

</style>
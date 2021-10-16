<template>
  <ListItem v-for="(task, index) in this.tasks" :key="index" :task="task" @remove="$emit('remove', index)"/>
</template>

<script>
import ListItem from './ListItem.vue'

export default {
    name: 'MyList',
    props: {
        tasks: Array
    },
    components: {
        ListItem,
    },
    emits: ['remove']
}
</script>

<style>

</style>
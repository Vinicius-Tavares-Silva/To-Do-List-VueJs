<template>
    <ul>
        <ListItem v-for="(task, index) in this.tasks" :key="index" :task="task" @remove="$emit('remove', index)"/>
    </ul>
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

<style scoped>
    ul {
        margin: 20px auto;
        text-align: center;
        padding: 5px;
        list-style-type: none;
    }
</style>
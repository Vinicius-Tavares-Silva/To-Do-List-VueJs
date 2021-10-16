<template>
  <MyHeader autor="Vinicius Tavares" />
  <TaskCreator @add="this.tasks.push($event)"/>
  <MyList :tasks="this.tasks" @remove="this.tasks.splice($event, 1)" />
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import MyList from './components/MyList.vue';
import TaskCreator from './components/TaskCreator.vue';

export default {
  name: 'App',
  components: {
    MyHeader,
    MyList,
    TaskCreator,
  },
  data() {
    return {
      tasks: ['Estudar', 'Passear', 'Trabalhar'],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0px;
}
</style>

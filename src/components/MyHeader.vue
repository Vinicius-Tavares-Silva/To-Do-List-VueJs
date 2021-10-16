<template>
  <header id="header">
    <h1>TO DO LIST</h1>
    <h4>{{ autor }}</h4>
  </header>
</template>

<script>
export default {
    name: 'MyHeader',
    props: {
        autor: String
    }
}
</script>

<style>
    #header {
        background-color: #2c3e50;
        color: whitesmoke;
    }
</style>
<template>
  <cotation />
  <tables />
</template>

<script>
  import cotation from './components/cotation.vue'
  import tables from './components/tables.vue'

  export default {
    name: 'App',
    components: { cotation, tables },
  }
</script>

<style>
  #app {
    text-align: center;
    color: #2c3e50;
    font-size: 25px;
  }
</style>

<template>
  <div id="app">
    <AppHeader />
    <DataTable />
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import DataTable from './components/DataTable.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    DataTable
  }
}
</script>

<style>
/* Adicione seus estilos globais aqui */
</style>

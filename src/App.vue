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
#app {
  background-color: #d3d3d3; /* Cor de fundo da tela */
  padding: 20px; /* Espaçamento interno para a tela */
  min-height: 100vh; /* Garante que a tela ocupe a altura total da janela */
}

.data-table {
  width: 80%; /* Ajuste a largura da tabela */
  margin: auto; /* Centraliza a tabela na tela */
  overflow-x: auto;
}

table {
  width: 100%; /* A tabela ocupa toda a largura do contêiner data-table */
  border-collapse: collapse;
}

th, td {
  padding: 10px;
  border: 1px solid #ccc;
  text-align: left;
}

.filter-options {
  margin-bottom: 10px;
}
</style>

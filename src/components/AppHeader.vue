<template>
  <br>
  <div class="header">
    <button @click="exportToExcel">Sair</button>
    <button @click="exportToExcel">Excel</button>
    <button @click="exportToExcel">Ajuda</button>
    <input type="text" v-model="filter" placeholder="Filter" class="filter-input" />
  </div>
</template>

<script>
export default {
  name: 'AppHeader', // Atualize o nome do componente aqui
  data() {
    return {
      filter: ''
    }
  },
  methods: {
    exportToExcel() {
      // Lógica para exportar para Excel
    }
  }
}
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
  gap: 10px;
  position: relative; /* Define a base para o posicionamento absoluto */
}

.filter-input {
  position: absolute;
  top: 0;
  right: 0;
}
</style>

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
  background-color: #f0f0f0; /* Cor de fundo cinza claro */
  padding: 10px; /* Adiciona algum espaçamento interno */
  border-radius: 5px; /* Adiciona bordas arredondadas */
}

.filter-input {
  position: absolute;
  top: 10;
  right: 0;
}

button {
  background-color: #d0d0d0; /* Cor de fundo cinza para os botões */
  border: none;
  padding: 10px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #b0b0b0; /* Cor de fundo cinza mais escura quando o botão é hover */
}

.filter-input {
  padding: 5px;
  border: 1px solid #ccc; /* Borda cinza clara */
  border-radius: 5px;
}
</style>

<template>
  
  <div class="header">
    <button @click="exportToExcel">Sair</button>
    <button @click="exportToExcel">Excel</button>
    <button @click="exportToExcel">Ajuda</button>
    <input type="text" v-model="filter" placeholder="Filter" class="filter-input" />
  </div>
</template>

<script>
export default {
  name: 'AppHeader',
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
  gap: 5px; /* Reduzir o espaçamento entre os elementos */
  background-color: #d3d3d3; /* Cor de fundo cinza escuro */
  padding: 10px; /* Reduzir o espaçamento interno */
  border-radius: 5px; /* Adiciona bordas arredondadas */
  position: relative; /* Define a base para o posicionamento absoluto */
  max-width: 1696px; /* Define uma largura máxima para o contêiner */
  margin: 0 auto; /* Centraliza o contêiner horizontalmente */
}

.filter-input {
  padding: 5px;
  border: 2px solid #ccc; /* Borda cinza clara - ajustável */
  border-radius: 10px;
  position: absolute;
  top: 12px; /* Mantém a posição do filtro */
  right: 40px; /* Ajusta a posição do filtro para a esquerda */
  margin-left: 10px;
  z-index: 1; /* Garante que o filtro não se sobreponha aos botões */
}

button {
  background-color: #ffffff; /* Cor de fundo branca para os botões */
  border: 2px solid #696969; /* Borda cinza escura para os botões - ajustável */
  padding: 5px; /* Reduzir o espaçamento interno dos botões */
  margin: 3px; /* Reduzir a margem entre os botões */
  border-radius: 5px;
  cursor: pointer;
  color: #333333; /* Cor do texto dos botões para contraste */
}

button:hover {
  background-color: #e0e0e0; /* Cor de fundo cinza claro quando o botão é hover */
}
</style>

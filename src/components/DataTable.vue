<template>
  <br>
  <div class="data-table-container">
    <div class="data-table">
      <div class="filter-options">
        <label><input type="radio" v-model="itemType" value="bobina" /> Bobina</label>
        <label><input type="radio" v-model="itemType" value="fardo" /> Fardo</label>
      </div>
      <table>
        <thead>
          <tr>
            <th>Bobina</th>
            <th>Bobina Mãe</th>
            <th>Sta Atual</th>
            <th>Sta Sit Atual</th>
            <th>Sta PA Volume</th>
            <th>Contr Reg</th>
            <th>Pátio</th>
            <th>Pilha</th>
            <th>Data Atualização</th>
            <th>Qtd dia</th>
            <th>Ponto Entrega</th>
            <th>Dt Liberação</th>
            <th>Qtd dia</th>
            <th>Dt Rendimento</th>
            <th>Qtd dia</th>
            <th>Dt Entrada no PA</th>
            <th>Qtd dia</th>
            <th>Usuário</th>
          </tr>
        </thead>
        <tbody>
          <!-- Linhas de dados -->
          <tr v-for="item in filteredData" :key="item.bobina">
            <td>{{ item.bobina }}</td>
            <td>{{ item.bobinaMae }}</td>
            <td>{{ item.staAtual }}</td>
            <td>{{ item.staSitAtual }}</td>
            <td>{{ item.staPAVolume }}</td>
            <td>{{ item.contrReg }}</td>
            <td>{{ item.patio }}</td>
            <td>{{ item.pilha }}</td>
            <td>{{ item.dataAtualizacao }}</td>
            <td>{{ item.qtdDia1 }}</td>
            <td>{{ item.pontoEntrega }}</td>
            <td>{{ item.dtLiberacao }}</td>
            <td>{{ item.qtdDia2 }}</td>
            <td>{{ item.dtRendimento }}</td>
            <td>{{ item.qtdDia3 }}</td>
            <td>{{ item.dtEntradaNoPA }}</td>
            <td>{{ item.qtdDia4 }}</td>
            <td>{{ item.usuario }}</td>
          </tr>
          <!-- Linhas em branco -->
          <tr v-for="n in emptyRows" :key="'empty-' + n">
            <td v-for="col in 17" :key="'empty-col-' + col"></td>
          </tr>
          <!-- Mensagem quando não há dados -->
          <tr v-if="filteredData.length === 0 && emptyRows === 0">
            <td colspan="17" class="empty-message">Nenhum dado disponível</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DataTable',
  data() {
    return {
      itemType: 'bobina',
      items: [
        // Itens para exibir na tabela
      ],
      emptyRows: 15 // Número de linhas em branco
    }
  },
  computed: {
    filteredData() {
      return this.items.filter(item => item.type === this.itemType);
    }
  }
}
</script>

<style scoped>
.data-table-container {
  width: 95%; /* Ajuste para ocupar a maior parte da tela */
  margin: 0 auto; /* Centraliza o contêiner */
}

.data-table {
  width: 100%; /* A tabela ocupa toda a largura do contêiner */
  overflow-x: auto; /* Adiciona rolagem horizontal se necessário */
}

table {
  width: 100%; /* A tabela ocupa toda a largura do contêiner */
  border-collapse: collapse;
  background-color: #ffffff; /* Cor de fundo branca para a tabela */
  border: 2px solid #696969; /* Borda cinza escura ao redor da tabela */
  border-radius: 5px; /* Bordas arredondadas */
}

th, td {
  padding: 10px;
  border: 1px solid #ccc; /* Borda cinza clara para as células */
  text-align: left;
  background-color: #ffffff; /* Cor de fundo branca para todas as células */
}

th {
  background-color: #f0f0f0; /* Cor de fundo cinza claro para o cabeçalho da tabela */
}

td {
  background-color: #ffffff; /* Cor de fundo branca para as células */
}

.empty-message {
  text-align: center; /* Centraliza o texto na célula */
  color: #696969; /* Cor do texto */
  padding: 20px; /* Adiciona algum espaçamento interno */
}
</style>

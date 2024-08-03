<template>
<br>
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
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'DataTable',
  data() {
    return {
      itemType: 'bobina',
      items: [
        {
          bobina: '86185002',
          bobinaMae: '86185002',
          staAtual: 'N',
          staSitAtual: '0',
          staPAVolume: 'BLOQUEADO',
          contrReg: '22',
          patio: '90',
          pilha: '06/10/2022',
          dataAtualizacao: '1',
          qtdDia1: 'BQ',
          pontoEntrega: '30/09/2022',
          dtLiberacao: '7',
          qtdDia2: '30/09/2022',
          dtRendimento: '7',
          qtdDia3: '30/09/2022',
          dtEntradaNoPA: '7',
          qtdDia4: 'MM4367',
          usuario: '861786032',
          // Continue com os outros campos...
        },
        // Adicione mais itens conforme necessário...
      ]
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
.data-table {
  overflow-x: auto;
}

.table {
  width: 100%;
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

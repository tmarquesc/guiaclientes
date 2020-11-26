<template>
  <div id="app">
    <div v-for="cliente in clientes" :key="cliente.id">
      <Cliente :cliente="cliente"/>
      <hr>
      <h4>Edição: </h4>
      <input type="text" v-model="cliente.nome">
      <input type="text" v-model="cliente.email">
    </div>
  </div>
</template>

<script>
import Cliente from './components/Cliente';

export default {
  name: 'App',
  data(){
    return {
      clientes: [
        {
          id: 2,
          nome: "Victor Lima",
          email: "victor@lima.com",
          idade: 99
        },
        {
          id: 22,
          nome: "Michael Scott",
          email: "michael@lima.com",
          idade: 45
        },
        {
          id: 31,
          nome: "Ednaldo Pereira",
          email: "ednaldopereira@yahoo.com",
          idade: 34
        }
      ]
    }
  },
  components: {
    Cliente
  }
}
</script>

<style>

</style>

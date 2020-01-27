<template>
  <div id="app">
    <Ligacoes
    :ligacoes = "ligacoes"
    />
    <FormLigacao
    :ligacoes = "ligacoes"
    @limpar-lista = "limparLista"
    @inserir-lista = "inserirItemLista"
    />
     
    
  </div>
</template>

<script>

import Ligacoes from './components/Ligacoes'
import FormLigacao from './components/FormLigacao'

 
  export default {
    components: {
      Ligacoes,
      FormLigacao,
    },
    data() {
      return {
        ligacoes: [
          {
            id: 2424,
            solicitante: "",
            solicitado: "",
            urgente: false,
          },
          {
            id: 2425,
            solicitante: "Marcio",
            solicitado: "Fernando TI da Colcci",
            urgente: true,
          },
        ],
      };
    },
    methods: {
      limparLista(valor){
        this.ligacoes = valor
      },
      inserirItemLista(ligacao) {
        this.ligacoes.push(ligacao)
      }
    },
  };
</script>

<style>
</style>

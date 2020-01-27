<template>
     <table>
        <tr>
          <th>ID</th>
          <th>Solicitante</th>
          <th>Solicitado</th>
        </tr>
        <tr v-for="ligacao in ligacoes" :key="ligacao.id">
          <td> {{ ligacao.id }} </td>
          <td> {{ ligacao.solicitante }} </td>
          <td> {{ ligacao.solicitado }} </td>
          <span v-if="ligacao.urgente"> URGENTE !!! </span>
          <span v-else> (de boas) </span>

        </tr>
      </table>
</template>

<script>
export default {
    props: ['ligacoes']
}
</script>

<style>

</style>
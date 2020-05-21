<template>
  <div class="infracoes">

      <div v-for="(infracao, index) in infracoes" :key="index">
        <label for="data">Data da infração:</label>
        <input type="text" id="data" :value="infracao.DADOS_INFRACAO.DATAHORA" /><br>

        <label for="placa">Placa:</label>
        <input type="text" id="placa" :value="infracao.PLACA" /><br>
      </div>

  </div>
</template>

<script>
export default {
  computed: {
    infracoes: function() {
        return this.$store.state.infracoesVeiculo
    }  
  }
};
</script>

<style>
</style>
<template>
  <div id="app">
    <div>{{ contagem }}</div>
    <Counter v-model="contagem"/>
    <div>
      <p v-if="excedeuLimitePositivo">o numero nao pode passar de 10</p>
      <p v-if="excedeuLimiteNegativo">o numero nao pode passar de -5</p>
    </div>
  </div>
</template>

<script>
import Counter from './components/Counter.vue';
export default {
  name: 'App',
  components: {
    Counter
  },
  data() {
    return {
      contagem: 0
    }
  },
  computed: {
    excedeuLimitePositivo() {
      return this.contagem >= 10
    },
    excedeuLimiteNegativo() {
      return this.contagem <= -5
    }
  }
}
</script>

<style>

</style>

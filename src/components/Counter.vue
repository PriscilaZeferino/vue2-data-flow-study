<template>
  <div class="contador">
    <button @click="add">Adicionar</button>
    <button @click="remove">Remover</button>
  </div>
</template>

<script>
export default {
  name: 'counter-component',
  data() {
    return {
      count: 0
    }
  },
  props: {
    contador: Number
  },
  methods: {
    add() {
      if(this.count >= 10) return;
      this.count++;
      this.$emit('input', this.count);
    },
    remove() {
      if(this.count <= -5) return;
      this.count--;
      this.$emit('input', this.count);
    }
  }
}
</script>

<style scoped>
</style>

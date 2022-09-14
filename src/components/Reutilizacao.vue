<template>
  <div>
    <button @click="ativar">John Cena</button>
    <span v-show="ativou">Activated!</span>
  </div>
</template>
<script>
export default {
  name: 'reutilizacao',
  data() {
    return {
      ativou: false
    }
  },
  methods: {
    ativar() {
      this.ativou = !this.ativou
    }
  }
}
</script>

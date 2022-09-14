<template>
  <div>
    <button @click="primeiro($event), segundo($event), terceiro($event)">
      Activate John Cena's Power
    </button>
    <p>{{ multiplos_eventos }}</p>
  </div>
</template>

<script>
export default {
  name: 'MultiplosEventos',
  data() {
    return {
      multiplos_eventos: ''
    }
  },
  methods: {
    primeiro(e) {
      this.multiplos_eventos = 'John Cena is coming'
    },
    segundo(e) {
      setTimeout(() => (this.multiplos_eventos = 'Watch out watch out watch out!'), 1000)
    },
    terceiro(e) {
      setTimeout(() => (this.multiplos_eventos = ''), 2000)
    }
  }
}
</script>
<style scoped>
div {
  margin: 100px;
}
</style>

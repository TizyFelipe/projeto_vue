<template>
  <h1>Get to know him: {{ nome }}</h1>
</template>

<script>
export default {
  name: 'LifeCycle',
  data() {
    return {
      nome: 'Hes a wrestler'
    }
  },
  created() {
    setTimeout(() => {
      this.nome = 'A fighter'
    }, 1000)

    this.lifecycle()
  },
  mounted() {
    setTimeout(() => {
      this.nome = 'Hes John Cena'
    }, 2000)

    this.lifecycle()
  },
  methods: {
    lifecycle() {
      console.log('running')
    }
  }
}
</script>

<template>
  <div>
    <h1>John Cena</h1>
    <p>My name is {{ nome }} and i work as a {{ job }}</p>
    <MultiplosEventos />
    <Reutilizacao />
  </div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue'
import Reutilizacao from './Reutilizacao.vue'

export default {
  name: 'PrimeiroComponente',
  components: {
    MultiplosEventos,
    Reutilizacao
  },
  data() {
    return {
      nome: 'John Cena',
      job: 'Wrestler'
    }
  }
}
</script>

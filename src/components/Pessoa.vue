<template>
  <div>
    <h2>His name is: {{ nome }}</h2>
    <Info :email="email" :is_working="false" />
    <Form />
  </div>
</template>

<script>
import Info from './Info'
import Form from './Form'

export default {
  name: 'Pessoa',
  components: {
    Info,
    Form
  },

  data() {
    return {
      nome: 'John Cena',
      email: 'johnscenas@gmail.com'
    }
  }
}
</script>

<!--  -->

<template>
  <div>
    <h2>Type your Form:</h2>
    <form action="" @submit="enviarformulario($event)">
      <div>
        <input type="text" v-model="name" />
      </div>

      <div>
        <input type="text" v-model="email" />
      </div>

      <div>
        <Submit />
      </div>
    </form>
    <p>JOHN CENA</p>
    <p>JOHN CENA</p>
    <p>JOHN CENA</p>
  </div>
</template>

<script>
import InputText from './forms/InputText'
import Submit from './forms/Submit'

export default {
  name: 'Form',
  components: {
    InputText,
    Submit
  },

  data() {
    return {
      name: '',
      email: ''
    }
  },
  methods: {
    enviarformulario(e) {
      e.preventDefault()
      const name = this.name
      const email = this.email

      console.log('Formulario Enviado')
      console.log('The name is:' + name)
      console.log('The email is:' + email)
    }
  }
}
</script>
<style scoped>
p {
  margin: 150px;
}
</style>

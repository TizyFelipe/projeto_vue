<template>
  <div>
    <p v-if="is_working">I'm John Cena and i'm working as a wrestler</p>
    <p v-else>I'm loking for a fight</p>
    <p>I use the following moves:</p>
    <ul>
      <li v-for="(moves, index) in my_moves" v-bind:key="index">
        {{ moves }}
      </li>
      <!-- moves=technology / submission=language / -->
    </ul>
    <p>And i use the following submitions:</p>
    <ul>
      <li v-for="moves in submissions" :key="moves.id">
        {{ moves.submission }}
      </li>
    </ul>
    <div>
      <button @click="ShowEmail">{{ textoBotao }}</button>
    </div>
    <p v-show="mostrar_email">Send me an email to: {{ email }}</p>
    <p>
      To access my John Cena's portfolio
      <a v-bind:href="my_stats" target="_blank">just click here</a>
    </p>
    <Picture />
  </div>
</template>

<script>
import Picture from './Picture.vue'

export default {
  name: 'Info',
  components: {
    Picture
  },
  props: {
    email: String,
    is_working: Boolean
  },
  data() {
    return {
      mostrar_email: false,
      my_stats: 'https://www.wwe.com/superstars/john-cena',
      textoBotao: 'Show my e-mail',
      my_moves: ['Attitude adjustment', 'German Suplex', 'STF'],
      submissions: [
        { id: 1, submission: 'Rear Naked Choke' },
        { id: 2, submission: 'Black Widow' },
        { id: 3, submission: 'Eye Rake' }
      ]
    }
  },
  methods: {
    ShowEmail() {
      this.mostrar_email = !this.mostrar_email
      if (!this.mostrar_email) {
        this.textoBotao = 'Show my e-mail'
      } else {
        this.textoBotao = 'Hide my e-mail'
      }
    }
  }
}
</script>

<template>
  <img :src="avatar" :alt="description" />
  <MudarImagem @mudar-imagem="trocarImagem" />
</template>

<script>
import MudarImagem from '@/components/MudarImagem'

export default {
  name: 'Picture',
  components: {
    MudarImagem
  },
  data() {
    return {
      avatar: '/Img/avatar.png',
      description: 'John Cena'
    }
  },
  methods: {
    trocarImagem() {
      if (this.avatar === '/Img/avatar2.png') {
        this.avatar = '/Img/avatar.png'
      } else {
        this.avatar = '/Img/avatar2.png'
      }
    }
  }
}
</script>

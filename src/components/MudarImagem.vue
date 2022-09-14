<template>
  <div>
    <button @click="$emit('mudarImagem')">Change John Cena</button>
  </div>
</template>

<script>
export default {
  name: 'MudarImagem',
  emits: ['mudarImagem']
}
</script>

<template>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Projects</a></li>
    <li><a href="#">Contact</a></li>
    <li v-if="esta_logado"><a href="">My Profile</a></li>
  </ul>
</template>

<script>
export default {
  name: 'Header',
  props: ['esta_logado']
}
</script>

<style scoped>
ul {
  list-style: none;
  display: flex;
  background: #111;
}

li {
  margin-right: 10px;
}

a {
  color: #ddd;
  text-decoration: none;
  transition: 0.5s;
}

a:hover {
  color: turquoise;
}
</style>

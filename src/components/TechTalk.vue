<template>
  <div class="hello">
    <h1>{{ title }}</h1>
    <p>
      <strong>Hoje vamos falar um pouco sobre Vue.js e Typescript</strong>
    </p>
    <h3><a href="https://github.com/Globalsys-Developers/vuejs-typescript"> Link do repositorio</a></h3>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'TechTalk',
  props: {
    title: String
  }
})
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

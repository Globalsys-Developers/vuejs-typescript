<template>
  <div class="github-search">
    <input type="text" class="search" placeholder="Your github username"
      v-on:keyup.enter="$emit('searchUser', search)"
      v-model="search">
    <button
      class="action"
      @click="$emit('searchUser', search)">
      SEND
    </button>
  </div>
</template>
<script>
import Vue from 'vue'
export default Vue.extend({
  name: 'GithubSearch',
  data () {
    return {
      search: ''
    }
  }
})
</script>
<style scoped>
.github-search {
  margin: 20px;
}
.action {
  height: 33px;
  margin-left: 10px;
}
</style>

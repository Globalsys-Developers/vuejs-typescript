<template>
  <div class="container">
    <h1>{{ title }}</h1>
    <GithubSearch
      @searchUser="searchUser"/>
    <GithubCard
      :user="user"
      @closeCard="closeCard"
      />
      <h3 v-if="error">{{ error }}</h3>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import axios from 'axios'
import GithubSearch from '../GithubSearch/GithubSearch.vue'
import GithubCard from '../GithubCard/GithubCard.vue'

export default Vue.extend({
  name: 'Github',
  data () {
    return {
      user: {},
      error: '',
      title: 'Welcome to github playground api :)'
    }
  },
  methods: {
    searchUser: async function (search: string) {
      this.cleanErrorMessages()
      axios
        .get('https://api.github.com/users/' + search)
        .then(res => {
          this.user = { ...res.data }
        })
        .catch(() => {
          this.user = {}
          this.error = 'User not found'
        })
    },
    cleanErrorMessages: function () {
      this.error = ''
    },
    closeCard: function () {
      this.user = {}
    }
  },
  components: {
    GithubSearch,
    GithubCard
  }
})
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
input.search {
  border-radius: 3px;
}
</style>

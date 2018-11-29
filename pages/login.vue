<template>
  <div>
    <h2>login</h2>
    <p>
      <button type="button" @click="login">login</button>
      <nuxt-link to="/">Top</nuxt-link>
    </p>
  </div>
</template>

<script>
import Cookies from 'universal-cookie'

export default {
  methods: {
    login() {
      const cookies = new Cookies()
      cookies.set('credential', 'true', {maxAge: 90})
      this.$route.push('/')
    }
  }
}
</script>

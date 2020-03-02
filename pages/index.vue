<template>
  <div>
    <logo />
    <Thenavbar />
    <banner />
    <div class="container">
      <div class="lead">
        {{ author.info }}
      </div>
      <div class="w-100"></div>

      <h1 class="title">
        tttt
      </h1>
      <h2 class="subtitle">
        My shining Nuxt.js project
      </h2>
      <div class="links">
        <a href="https://nuxtjs.org/" target="_blank" class="button--green">
          Documentation</a
        >
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
          >GitHub</a
        >
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo'
import Banner from '~/components/banner'
import Thenavbar from '~/components/thenavbar'
import author from '~/static/data.json'
export default {
  components: {
    Logo,
    Banner,
    Thenavbar
  },
  // eslint-disable-next-line no-unused-vars
  asyncData({ req, params, store }) {
    return { author }
  },
  head: {
    title: 'Home page 🚀',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Home page description'
      }
    ]
  }
}
</script>
<style lang="scss">
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

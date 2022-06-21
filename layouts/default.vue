<template>
  <div>
    <Header />
      <no-ssr>
        <vue-particles class="animated-background" />
      </no-ssr>
      <Nuxt />
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'

export default { components: { Header, Footer } }
</script>

<style lang="scss">
@import '~/assets/scss/variables';

*,
html,
body {
  margin: 0px;
  padding: 0px;
  font-family: $space-mono;
  width: 100%;
  word-wrap: break-word;
}

.animated-background {
  position: fixed;
  height: 100%;
  background-color: $royal;
  top: 0px;
  left: 0px;
}
</style>

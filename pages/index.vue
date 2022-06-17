<template>
  <div>
    <Header />
        <div class="content">
          <Home />
        </div>
  </div>
</template>

<script>
import Header from '~/components/Header.vue'
import Home from '~/components/Home.vue'

export default {
  name: 'MainPage',
  components: { Header, Home},
}
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
  height: 100%;
  word-wrap: break-word;
}

.content {
  padding-top: 100px;
}
</style>

<template>
  <div>
    <Header />
      <vue-particles class="animated-background" />
      <Nuxt class="components" />
    </div>
</template>

<script>
import Header from '~/components/Header.vue'
export default { components: { Header } }
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


.components {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  top: 0px;
  left: 0px;
}

@import '~/assets/scss/variables';
.animated-background {
  position: fixed;
  height: 100%;
  background-color: $royal;
  top: 0px;
  left: 0px;
}
</style>

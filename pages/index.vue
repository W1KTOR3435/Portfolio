<template>
  <div class="components">
    <Main />
    <About />
  </div>
</template>

<script>
import Main from '~/components/Main.vue'
import About from '~/components/About.vue'

export default {
  name: 'MainPage',
  components: { Main, About },
  layout: 'default',
}
</script>

<style lang="scss" scoped>
.components {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-items: center;
  position: relative;
  top: 0px;
  left: 0px;

  @media (max-width: 768px) {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}
</style>

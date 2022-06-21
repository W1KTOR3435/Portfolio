<template>
  <div class="components">
    <Linkedin />
    <Github />
    <Email />
    <Phone />
  </div>
</template>

<script>
import Linkedin from '~/components/Linkedin.vue'
import Github from '~/components/Github.vue'
import Email from '~/components/Email.vue'
import Phone from '~/components/Phone.vue'

export default {
  name: 'ContactPage',
  components: { Linkedin, Github, Email, Phone },
}
</script>

<style lang="scss" scoped>
.components {
  width: 100%;
  display: grid;
  justify-items: center;
  grid-template-columns: 1fr 1fr;
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

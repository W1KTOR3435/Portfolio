<template>
  <div class="footer">
    <a
      href="https://www.linkedin.com/in/wiktor-kowalczyk/"
      target="_blank"
      class="footer__link"
    >
      Made by Wiktor Kowalczyk
    </a>
  </div>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style lang="scss">
@import '~/assets/scss/variables';

.footer {
  margin-top: 50px;
  position: relative;
  width: 100%;
  height: 50px;
  background-color: $torea;
  display: flex;
  justify-content: center;
  align-items: center;
}

.footer__link {
  display: flex;
  justify-content: center;
  align-content: center;
  color: $iron;
}
</style>

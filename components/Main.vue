<template>
  <div class="content">
    <div class="head__text name-text">
        Wiktor Kowalczyk
    </div>
    <div class="head__text heading-text">
        Frontend Developer
    </div>
  </div>
</template>

<script>
export default {
  name: 'Main',
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/variables';
.content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100%;
  color: $iron;
}

.head__text {
  display: flex;
  justify-content: center;
  align-items: center;
}

.name-text {
  font-size: 75px;
  @media (max-width: 768px) {
    font-size: 60px;
    text-align: center;
  }
}

.heading-text {
  font-size: 25px;
  @media (max-width: 768px) {
    font-size: 20px;
    text-align: center;
  }
}
</style>

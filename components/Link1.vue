<template>
  <div class="main">
    <div class="main__top">
      <img src="~/assets/linkedin.svg" class="main__top__logo" />
    </div>
    <div class="main__bot">
      LinkedIn
    </div>
  </div>
</template>

<script>
export default {
  name: 'Link1',
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/variables';

.main {
  margin-top: 150px;
  background-color: rgb(4, 6, 13, 0.5);
  display: flex;
  flex-direction: column;
  width: 80%;
  height: 500px;
}

.main__top{
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.main__bot{
  height: 100%;
  display: flex;
  align-items: top;
  justify-content: center;
  color: $iron;
  font-size: 50px;
}

.main__top__logo {
  width: 50%;
}
</style>

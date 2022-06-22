<template>
  <div class="content">
    <h2 class="content__section-top">About me</h2>
    <div class="content__section-bot">
      <div class="content__section-bot__left">
        Hi, my name's Wiktor. My interest is learning practical IT skills mostly
        about Frontend Development. I'm currently in high school, but I'm open
        to participating in projects that will help me develop my skills and
        build portfolio.
      </div>
      <div class="content__section-bot__right">
        <img src="~/assets/coding.svg" class="img" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'About',
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/variables';

.content {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  height: 100vh;
  width: 100%;
}

.content__section-top {
  width: 100%;
  height: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 40px;
  color: $iron;
}

.content__section-bot {
  width: 100%;
  display: grid;
  justify-items: center;
  grid-template-columns: 1fr 1fr;

  @media (max-width: 1000px) {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}

.content__section-bot__left {
  width: 90%;
  height: 100%;
  display: flex;
  align-items: center;
  font-size: 30px;
  color: $iron;
  max-height: 400px;
  //background-color: rgb(4, 6, 13, 0.5);

  @media (max-width: 1050px) {
    font-size: 25px;
    margin-bottom: 50px;
    background-color: transparent;
  }

  @media (max-width: 400px) {
    font-size: 20px;
    margin-bottom: 50px;
    background-color: transparent;
  }
}

.content__section-bot__right {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  max-height: 400px;
}

.img {
  width: 70%;
  max-height: 400px;
}
</style>

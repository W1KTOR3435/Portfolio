<template>
  <div class="main">
    <div class="main__top">
      <img src="~/assets/email.svg" class="main__top__logo" />
    </div>
    <div class="main__bot">
      E-mail
      <a href="mailto:wkow3435@gmail.com" target="_blank" class="main__bot__link">
        <input type="button" class="main__bot__link__btn" value="Open"/>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Email',
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/variables';

.main {
  margin-top: 50px;
  background-color: rgb(4, 6, 13, 0.5);
  display: flex;
  flex-direction: column;
  width: 80%;
  height: 500px;
  max-width: 400px;
  
  @media (max-width: 768px) {
    height: 400px;
  }
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
  align-items: center;
  flex-direction: column;
  color: $iron;
  font-size: 40px;
}

.main__bot__link{
  display: flex;
  justify-content: center;
  text-decoration: none;
}

.main__bot__link__btn{
  width: 80%;
  color: $iron;
  border: 1px solid $iron;
  background-color: transparent;
  font-size: 30px;
}

.main__top__logo {
  width: 50%;
}
</style>

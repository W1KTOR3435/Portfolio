<template>
  <div class="main">
    <div class="main__top">
      <img src="~/assets/linkedin.svg" class="main__top__logo" />
    </div>
    <div class="main__bot">
      LinkedIn
      <button type="button" class="main__bot__btn" value="Open">
        <a href="https://www.linkedin.com/in/wiktor-kowalczyk/" target="_blank" class="main__bot__btn__link">
          Open
        </a>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Linkedin',
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
  max-width: 400px;

  @media (max-width: 768px) {
    height: 400px;
  }
}

.main__top {
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.main__bot {
  height: 100%;
  display: flex;
  align-items: center;
  flex-direction: column;
  color: $iron;
  font-size: 40px;
}

.main__bot__btn__link {
  width: 100%;
  height: 100%;
  color: $iron;
  display: flex;
  justify-content: center;
  text-decoration: none;
  background-color: transparent;
  font-size: 30px;
  transition: background-color 500ms;
  
  &:hover{
    color:$royal;
    background-color: $iron;
  }

  &:active{
    color:$iron;
    background-color: $torea;
  }
}

.main__bot__btn {
  margin-top: 50px;
  width: 80%;
  border: 2px solid $iron;
  background-color: transparent;

  @media (max-width: 780px) {
    margin-top: 0px;
  }
}

.main__top__logo {
  width: 50%;

   @media (max-width: 780px) {
    padding-top: 50px;
  }
}
</style>

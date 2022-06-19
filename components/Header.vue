<template>
  <header>
    <nav>
      <Nuxt-link to="/" class="img-link">
        <img src="~/assets/logo.png" alt="logo" class="img" />
      </Nuxt-link>
      <ul v-show="!mobile" class="navigation">
        <li>
          <NuxtLink class="box" to="/">
            <div class="btn btn-one">
              <span> Home </span>
            </div>
          </NuxtLink>
        </li>
        <li>
          <NuxtLink class="box" to="/contact">
            <div class="btn btn-one">
              <span> Contact </span>
            </div>
          </NuxtLink>
        </li>
      </ul>
      <button
        v-show="mobile"
        class="hamburger"
        :class="{ 'hamburger--is-open': hamburgerOpen }"
        @click="
          toggleMobileNav()
          hamburgerOpen = !hamburgerOpen
        "
      />
      <transition name="mobile-nav">
        <ul v-show="mobileNav" class="dropdown-nav">
          <Nuxt-link to="/" class="img-link">
            <img src="~/assets/logo.png" alt="logo" class="img-mobile" />
          </Nuxt-link>
          <li>
            <NuxtLink class="btn-mobile" to="/"> Home </NuxtLink>
          </li>
          <li>
            <NuxtLink class="btn-mobile" to="/contact"> Contact </NuxtLink>
          </li>
        </ul>
      </transition>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      mobile: null,
      mobileNav: null,
      windowWidth: null,
      hamburgerOpen: false,
    }
  },

  mounted() {
    window.addEventListener('resize', this.checkScreen)
    this.checkScreen()
  },

  methods: {
    toggleMobileNav() {
      this.mobileNav = !this.mobileNav
    },

    awayMobileNav() {
      this.mobileNav = false
    },

    checkScreen() {
      this.windowWidth = window.innerWidth
      if (this.windowWidth <= 768) {
        this.mobile = true
        return
      }
      this.mobile = false
      this.mobileNav = false
    },
  },
}
</script>
<style lang="scss">
@import '~/assets/scss/variables';

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: $torea;
  z-index: 2;
  width: 100%;
  height: 100px;
  position: fixed;
  transition: 0.5s ease all;
  @media (max-width: 768px) {
    height: auto;
  }

  nav {
    position: relative;
    right: 0px;
    display: flex;
    align-items: center;
    flex-direction: row;
    transition: 0.3s ease all;
    width: 100%;
    @media (min-width: 768px) {
      height: 100%;
    }
    @media (max-width: 768px) {
      justify-content: space-between;
    }

    //desktop buttons and navigation
    .navigation {
      display: flex;
      align-items: center;
      flex: 1;
      justify-content: flex-end;
    }

    .box {
      text-decoration: none;
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .btn {
      line-height: 50px;
      height: 50px;
      text-align: center;
      width: 150px;
      cursor: pointer;
    }
    .btn-one {
      color: #fff;
      transition: all 0.3s;
      position: relative;
    }
    .btn-one span {
      transition: all 0.3s;
    }
    .btn-one::before {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 1;
      opacity: 0;
      transition: all 0.3s;
      border-top: 1px solid rgb(255, 255, 255, 0.5);
      border-bottom: 1px solid rgb(255, 255, 255, 0.5);
      transform: scale(0.1, 1);
    }
    .btn-one:hover span {
      letter-spacing: 2px;
    }
    .btn-one:hover::before {
      opacity: 1;
      transform: scale(1, 1);
    }
    .btn-one::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 1;
      transition: all 0.3s;
    }
    .btn-one:hover::after {
      opacity: 0;
      transform: scale(0.1, 1);
    }

    //logo
    .img {
      margin-left: 10px;
      width: 100px;
      height: auto;
    }

    .img-mobile {
      margin-left: 10px;
      width: 100px;
      height: auto;
    }

    .img-link {
      height: 100px;
    }

    li {
      min-width: 150px;
      text-transform: uppercase;
      height: 100px;
      text-align: center;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    //burger menu
    .hamburger {
      z-index: 1;
      background-color: $torea;
      position: relative;
      display: flex;
      height: 80px;
      width: 80px;
      border: 0;
      cursor: pointer;
      pointer-events: all;
      outline: none;

      &:before,
      &:after {
        content: '';
        position: absolute;
        top: 32px;
        left: 20px;
        background-color: $iron;
        width: 40px;
        height: 4px;
        transition: transform 300ms ease-out;
      }

      &:after {
        top: auto;
        bottom: 32px;
      }

      &--is-open {
        &:before {
          transform: translateY(6px) rotate(135deg);
        }
        &:after {
          transform: translateY(-6px) rotate(45deg);
        }
      }
    }
    //mobile nav
    .dropdown-nav {
      display: flex;
      align-items: center;
      flex-direction: column;
      position: fixed;
      width: 100%;
      height: 100%;
      background-color: $torea;
      top: 0;
      left: 0;
    }
    .btn-mobile {
      color: $iron;
      text-decoration: none;
      font-size: 50px;
    }
    // animations
    .mobile-nav-enter-active {
      animation: slideIn 1s;
    }
    .mobile-nav-leave-active {
      animation: slideOut 2s;
    }

    @keyframes slideIn {
      from {
        left: -800px;
      }
      to {
        left: 0px;
      }
    }
    @keyframes slideOut {
      from {
        left: 0px;
      }
      to {
        left: -800px;
      }
    }
  }
}
</style>

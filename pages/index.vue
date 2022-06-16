<template>
  <div>
    <Header />
    <HomePage />
  </div>
</template>

<script>
import Header from '~/components/Header.vue';
import HomePage from '~/components/HomePage.vue';
export default {
    name: "IndexPage",
    components: { Header, HomePage }
}
</script>

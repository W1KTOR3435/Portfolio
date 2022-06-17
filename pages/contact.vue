<template>
  <div>
    <Header />
    <Contact />
  </div>
</template>

<script>
import Header from '~/components/Header.vue';
import Contact from '~/components/Contact.vue';
export default {
    name: "ContactPage",
    components: { Header, Contact }
}
</script>
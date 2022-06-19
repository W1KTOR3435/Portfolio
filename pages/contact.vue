<template>
  <div>
    <Link1 />
    <Link2 />
    <Link3 />
  </div>
</template>

<script>
import Link1 from '~/components/Link1.vue'
import Link2 from '~/components/Link2.vue'
import Link3 from '~/components/Link3.vue'

export default {
  name: 'ContactPage',
  components: { Link1, Link2, Link3 },
}
</script>

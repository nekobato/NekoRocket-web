<template>
  <section class="top-section">
    <Logo class="logo" shrink="3"/>
  </section>
</template>
<script>
import Logo from '~/components/Parts/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style scoped>
.top-section {
  display: flex;
  align-items: center;
  justify-content: center;
}
.logo {
  margin: 0 auto;
}
</style>

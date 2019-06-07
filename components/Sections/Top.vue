<template>
  <section class="top-section">
    <Logo class="logo" />
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

<style lang="scss" scoped>
$logo-width: 1500px;
$logo-height: 681px;

.top-section {
  display: flex;
  align-items: center;
  justify-content: center;
}
.logo {
  margin: 0 auto;
  width: 500px;
  @media screen and (max-width: 1000px) {
    width: 80%;
  }
}
</style>

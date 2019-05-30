<template>
  <div :style="imageStyle">
    <img class="logo-image" src="~/assets/logo.png">
  </div>
</template>

<script>
// 1500 x 681
export default {
  props: ['shrink'],
  computed: {
    imageStyle() {
      return {
        width: `${1500 / this.shrink}px`,
        height: `${681 / this.shrink}px`
      }
    }
  }
}
</script>


<style lang="scss" scoped>
$logo-width: 1500px;
$logo-height: 681px;

.logo-image {
  width: 100%;
  height: 100%;
}
</style>

<template>
  <div class="container">
    <ResetCSS/>
    <nuxt/>
  </div>
</template>
<script>
import ResetCSS from '~/components/Utils/ResetCSS.vue'
export default {
  components: {
    ResetCSS
  }
}
</script>

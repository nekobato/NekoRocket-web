<template>
  <h2>
    <span class="title-en">{{ en }}</span>
    <span class="title-ja">{{ ja }}</span>
  </h2>
</template>

<script>
export default {
  props: ['en', 'ja']
}
</script>

<style lang="scss" scoped>
h2 {
  padding: 24px 0 0 24px;
  text-align: left;
}
.title-en {
  display: block;
  font-size: 32px;
  font-weight: bold;
  color: hsla(0, 0, 30%, 1);
}
.title-ja {
  display: block;
  margin-top: 8px;
  font-size: 16px;
  font-weight: bold;
  color: hsla(0, 0, 50%, 1);
}
</style>

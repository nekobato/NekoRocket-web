<template>
  <section class="vision-section">
    <SectionTitle en="Vision" ja="私たちのビジョン"/>
    <div class="texts">
      <p>
        Treasure the individuals’ story
        <br>生の情報を紡いでいく。誰かのストーリーをみんなで大切にする。
      </p>
      <p>
        Majority=Minority
        <br>変わった人も普通の人も同じくらい大事。
      </p>
      <p>
        Keep yourself safe and warm
        <br>他者と同じくらい自分と会話する。無理は禁物、他者に無理を強いるのも禁止。
      </p>
      <p>
        Anyone can learn and play
        <br>大人も遊んで、学んでよい。子供でも背伸びして大人になってよい。
      </p>
    </div>
  </section>
</template>
<script>
import SectionTitle from '~/components/Parts/SectionTitle.vue'
import LogoImage from '~/components/Parts/Logo.vue'

export default {
  components: {
    SectionTitle,
    LogoImage
  }
}
</script>

<style lang="scss" scoped>
.texts {
  padding: 48px 0 0 24px;
}
.vision-section {
  p {
    margin: 0 0 40px;
    font-size: 20px;
    font-weight: bold;
    line-height: 40px;
    letter-spacing: 1px;
    text-align: left;
  }
}
</style>

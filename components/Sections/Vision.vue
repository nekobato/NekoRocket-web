<template>
  <section class="vision-section">
    <SectionTitle en="Vision" ja="私たちのビジョン" />
    <div class="texts">
      <div class="text-group">
        <p class="en">Treasure the individuals’ story</p>
        <p class="ja">
          生の情報を紡いでいく。<br
            class="on-mobile"
          />誰かのストーリーをみんなで大切にする。
        </p>
      </div>
      <div class="text-group">
        <p class="en">Majority=Minority</p>
        <p class="ja">変わった人も普通の人も同じくらい大事。</p>
      </div>
      <div class="text-group">
        <p class="en">Keep yourself safe and warm</p>
        <p class="ja">
          他者と同じくらい自分と会話する。<br
            class="on-mobile"
          />無理は禁物、<br class="on-mobile" />他者に無理を強いるのも禁止。
        </p>
      </div>
      <div class="text-group">
        <p class="en">Anyone can learn and play</p>
        <p class="ja">
          大人も遊んで、学んでよい。<br
            class="on-mobile"
          />子供でも背伸びして大人になってよい。
        </p>
      </div>
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
  text-align: left;
}
.text-group {
  margin: 0 0 40px;
}
.vision-section {
  p {
    font-size: 20px;
    font-weight: bold;
    line-height: 40px;
    letter-spacing: 1px;
    &.ja {
      color: hsla(0, 0, 0, 0.72);
    }
    @media screen and (max-width: 1000px) {
      font-size: 16px;
      line-height: 24px;
    }
  }
}
</style>

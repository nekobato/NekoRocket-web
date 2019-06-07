<template>
  <section class="about-us-section">
    <SectionTitle en="About Us" ja="ネコロケット について" />
    <div class="texts">
      <p>
        私たちのまちには、
        <br class="on-mobile" />そこにしかない、独自の魅力があります。
      </p>
      <p>
        私たちのまちには、今後、
        <br class="on-mobile" />より多くの、異なる背景を持つ人々が、
        <br />ふと通り過ぎるように遊びにきたり、
        <br class="on-mobile" />長期的に仕事のため
        <br class="on-mobile" />滞在しにきたりするでしょう。
      </p>
      <p>
        こうした多様な人たちが集うまちには、
        <br />新しく大きな魅力を生み出すと同時に、
        <br class="on-mobile" />時に問題も起こすことが予想されます。
      </p>
      <p>
        ネコロケットは
        <br />そうしたまちに起こる変化に備えた
        <br class="on-mobile" />音声ガイドアプリの開発を行う団体です。
      </p>
    </div>
  </section>
</template>

<script>
import SectionTitle from '~/components/Parts/SectionTitle.vue'

export default {
  components: {
    SectionTitle
  }
}
</script>

<style lang="scss" scoped>
.texts {
  padding: 64px 0 0;
  > p {
    margin-top: 24px;
    font-size: 24px;
    font-weight: bold;
    line-height: 48px;
    letter-spacing: 1px;
    &:first-child {
      margin-top: 0;
    }
    @media screen and (max-width: 1000px) {
      font-size: 14px;
      line-height: 28px;
      padding: 0 8px;
    }
  }
}
.on-mobile {
  display: none;
  @media screen and (max-width: 1000px) {
    display: inline;
  }
}
</style>

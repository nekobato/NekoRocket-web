<template>
  <section class="logo-section">
    <SectionTitle en="Logo" ja="ロゴについて" />
    <div class="logo-description-container">
      <div class="logo-container">
        <LogoImage class="logo-image" />
      </div>
      <div class="logo-description">
        <span class="title">団体名、ネコロケットに込めた想い</span>
        <p class="text">
          ネコ：
          <br />まち(地域)を歩く一個人を表します。ゆったりとマイペース。
          <br />「地域猫」などの言葉もあります。
        </p>
        <p class="text">
          ロケット：
          <br />ちょっと近未来的ですが、地球の誰でも乗せてくれる乗り物。
          <br />多様性や地球、グローバルな社会を表します。
        </p>
        <div class="reference">
          <a class="reference-link" href="https://hisashikiguchi.com/">
            木口恒事務所さん HP
            <OpenInNew class="icon-open-in-new" />
          </a>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import LogoImage from '~/components/Parts/Logo.vue'
import SectionTitle from '~/components/Parts/SectionTitle.vue'
import OpenInNew from '~/components/Icons/OpenInNew.vue'

export default {
  components: {
    LogoImage,
    SectionTitle,
    OpenInNew
  }
}
</script>

<style lang="scss" scoped>
.logo-description-container {
  display: flex;
  align-items: center;
  padding: 160px 0;
  @media screen and (max-width: 1000px) {
    flex-direction: column;
    padding: 40px 0;
  }
  .logo-container {
    flex-shrink: 0;
    padding-left: 24px;
    width: 50%;
    height: 100%;
    .logo-image {
      width: 250px;
    }
    @media screen and (max-width: 1000px) {
      padding: 0 0 40px;
      width: 100%;
    }
  }
  .logo-description {
    flex-shrink: 0;
    width: 50%;
    text-align: left;
    height: 100%;
    @media screen and (max-width: 1000px) {
      padding: 0 16px;
      width: 100%;
    }
  }
  .title {
    font-size: 16px;
    font-weight: bold;
  }
  .text {
    margin-top: 16px;
    font-size: 16px;
    line-height: 32px;
  }
  .reference {
    margin-top: 32px;
  }
  .icon-open-in-new {
    width: 16px;
    height: 16px;
    fill: hsla(0, 0, 60%, 1);
  }
}
</style>

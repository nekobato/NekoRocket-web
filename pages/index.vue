<template>
  <section class="container">
    <div class="sections">
      <TopSection id="top" class="section" :style="sectionStyle"/>
      <AboutUsSection id="aboutus" class="section" :style="sectionStyle"/>
      <VisionSection id="vision" class="section" :style="sectionStyle"/>
      <ProjectSection id="project" class="section" :style="sectionStyle"/>
      <LogoSection id="logo" class="section" :style="sectionStyle"/>
      <FooterSection id="footer"/>
    </div>
    <Menu class="menu"/>
  </section>
</template>

<script>
import debounce from 'lodash.debounce'
import TopSection from '~/components/Sections/Top.vue'
import AboutUsSection from '~/components/Sections/AboutUs.vue'
import VisionSection from '~/components/Sections/Vision.vue'
import ProjectSection from '~/components/Sections/Project.vue'
import LogoSection from '~/components/Sections/Logo.vue'
import FooterSection from '~/components/Sections/Footer.vue'
import Menu from '~/components/Parts/Menu.vue'

export default {
  data() {
    return {
      windowHeight: 0
    }
  },
  components: {
    TopSection,
    AboutUsSection,
    VisionSection,
    ProjectSection,
    LogoSection,
    FooterSection,
    Menu
  },
  computed: {
    sectionStyle() {
      return {
        minHeight: `${this.windowHeight}px`
      }
    }
  },
  mounted() {
    this.windowHeight = window.innerHeight
    window.addEventListener(
      'resize',
      debounce(() => {
        this.windowHeight = window.innerHeight
      }, 0.3)
    )
  }
}
</script>

<style lang="scss" scoped>
.container {
  position: relative;
  margin: 0 auto;
  width: 1000px;
  min-height: 100vh;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.section {
  position: relative;
  min-height: 480px;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

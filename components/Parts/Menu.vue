<template>
  <nav>
    <div class="launcher" @click="toggleMenu">
      <MenuImage class="launcher-image" />
    </div>
    <transition name="fade">
      <ul class="contents-list" v-show="isVisible">
        <li>
          <a href="#top">TOP</a>
        </li>
        <li>
          <a href="#aboutus">ABOUT US</a>
        </li>
        <li>
          <a href="#vision">VISION</a>
        </li>
        <li>
          <a href="#project">PROJECTS</a>
        </li>
        <li>
          <a href="#logo">LOGO</a>
        </li>
      </ul>
    </transition>
  </nav>
</template>
<script>
import MenuImage from '~/components/Icons/Menu.vue'
export default {
  components: {
    MenuImage
  },
  data() {
    return {
      isVisible: false
    }
  },
  methods: {
    toggleMenu() {
      this.isVisible = !this.isVisible
    }
  }
}
</script>
<style lang="scss" scoped>
nav {
  position: fixed;
  top: 16px;
  margin-left: -64px;
  width: 64px;
  height: 64px;
  text-align: right;
  @media screen and (max-width: 1000px) {
    top: 0;
    left: 4px;
    margin-left: 0;
  }
}
.launcher {
  padding: 8px;
  width: 64px;
  height: 64px;
  cursor: pointer;
  .launcher-image {
    width: 48px;
    height: 48px;
    fill: hsla(0, 0, 0, 0.8);
  }
}
.contents-list {
  position: absolute;
  top: 64px;
  right: 0;
  width: auto;
  text-align: right;
  li a {
    font-size: 24px;
    line-height: 40px;
    text-decoration: none;
    color: hsla(0, 0, 20%, 0.6);
    font-weight: bold;
    white-space: nowrap;
  }
  @media screen and (max-width: 1000px) {
    text-align: left;
    left: 16px;
    rigth: auto;
  }
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>

<template>
  <div class="project-item">
    <span class="label">{{ label }}</span>
    <img class="image" :src="image">
    <span class="type">{{ type }}</span>
    <span class="name">{{ name }}</span>
    <p class="description" v-show="!!description">{{ description }}</p>
    <a class="link" :href="linkUrl" target="_blank" v-show="!!linkTitle">
      {{ linkTitle }}
      <OpenInNew class="icon-open-in-new"/>
    </a>
  </div>
</template>

<script>
import OpenInNew from '~/components/Icons/OpenInNew.vue'

export default {
  components: {
    OpenInNew
  },
  props: [
    'label',
    'image',
    'type',
    'name',
    'description',
    'link-url',
    'link-title'
  ]
}
</script>

<style lang="scss" scoped>
.project-item {
  margin: 48px 60px;
  width: 320px;
  text-align: left;
}
.image,
.type,
.name,
.description,
.link {
  display: block;
}
.label {
  display: inline-block;
  margin-bottom: 2px;
  padding: 4px 16px;
  background: #000;
  font-size: 14px;
  font-weight: bold;
  color: hsla(0, 0, 100%, 0.9);
}
.image {
  width: 100%;
  height: 320px;
  background: hsla(0, 0, 70%, 0.7);
}
.type {
  margin-top: 4px;
  font-size: 14px;
  color: hsla(0, 0, 30%, 1);
}
.name {
  margin-top: 16px;
  font-size: 16px;
  line-height: 20px;
  font-weight: bold;
  color: hsla(0, 0, 30%, 1);
}
.description {
  margin-top: 4px;
  font-size: 16px;
}
.link {
  margin-top: 8px;
  color: hsla(0, 0, 30%, 1);
}
.icon-open-in-new {
  width: 16px;
  height: 16px;
  fill: hsla(0, 0, 60%, 1);
}
</style>

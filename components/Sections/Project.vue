<template>
  <section class="project-section">
    <SectionTitle en="Projects" ja="プロジェクト"/>
    <div class="project-items">
      <ProjectItem
        class="project-item"
        v-for="(project, index) in projects"
        :key="index"
        v-bind="project"
      />
    </div>
  </section>
</template>

<script>
import ProjectItem from '~/components/Parts/ProjectItem.vue'
import SectionTitle from '~/components/Parts/SectionTitle.vue'

export default {
  components: {
    SectionTitle,
    ProjectItem
  },
  data() {
    return {
      projects: [
        {
          image: require('@/assets/placeholder.png'),
          label: '品川区',
          type: 'iOS, Andoroid',
          name: '(仮) 戸越公園 Language exchange 音声アプリ',
          description: 'Coming Soon...'
        },
        {
          image: require('@/assets/placeholder.png'),
          label: '品川区',
          type: 'iOS, Andoroid',
          name: '(仮) 戸越八幡神社 英語案内音声アプリ',
          description: 'Coming Soon...'
        },
        {
          image: require('@/assets/placeholder.png'),
          label: '品川区',
          type: 'iOS, Andoroid',
          name: '(仮) 戸越銀座商店街 多言語・他宗教に優しい音声ガイド',
          description: 'Coming Soon...'
        },
        {
          image: require('@/assets/placeholder.png'),
          type: '?',
          name: '?',
          description: 'Coming Soon...',
          label: '目黒区'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.project-items {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding-top: 48px;
}
.project-item {
  flex-shrink: 0;
}
</style>

<template>
  <div class="home">
    <SectionProfile />
    <SectionIcons />
    <SectionExperience />

    <div class="construction">Em construção...</div>
  </div>
</template>

<script>
// @ is an alias to /src
import SectionProfile from '@/components/SectionProfile.vue'
import SectionIcons from '@/components/SectionIcons.vue'
import SectionExperience from '@/components/SectionExperience.vue'

export default {
  name: 'HomeView',
  components: {
    SectionProfile,
    SectionIcons,
    SectionExperience
  }
}
</script>

<style scoped>
  .construction{
    margin: 4rem auto
  }
</style>

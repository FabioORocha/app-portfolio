<template>
  <div class="home">
    <SectionProfile />
    <SectionIcons />
    <SectionExperience />
    <SectionWorks />

    <div class="construction">Em construção...</div>
  </div>
</template>

<script>
// @ is an alias to /src
import SectionProfile from '@/components/SectionProfile.vue'
import SectionIcons from '@/components/SectionIcons.vue'
import SectionExperience from '@/components/SectionExperience.vue'
import SectionWorks from '@/components/SectionWorks.vue'

export default {
  name: 'HomeView',
  components: {
    SectionProfile,
    SectionIcons,
    SectionExperience,
    SectionWorks
  }
}
</script>

<style scoped>
  .construction{
    margin: 4rem auto
  }
</style>

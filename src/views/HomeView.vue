<template>
  <div class="home">
    <SectionProfile />
    <SectionIcons />
    <SectionExperience />
    <SectionWorks />
    <SectionProjects />
  </div>
</template>

<script>
// @ is an alias to /src
import SectionProfile from '@/components/SectionProfile.vue'
import SectionIcons from '@/components/SectionIcons.vue'
import SectionExperience from '@/components/SectionExperience.vue'
//import SectionWorks from '@/components/SectionWorks.vue'
import SectionProjects from '@/components/SectionProjects.vue'

export default {
  name: 'HomeView',
  components: {
    SectionProfile,
    SectionIcons,
    SectionExperience,
    //SectionWorks,
    SectionProjects
  }
}
</script>

<style scoped>
  .construction{
    margin: 0 auto;
    padding: 4rem auto;
  }
</style>

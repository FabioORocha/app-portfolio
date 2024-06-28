<template>
  <div class="home">
    <SectionProfile />
    <SectionIcons />
  </div>
</template>

<script>
// @ is an alias to /src
import SectionProfile from '@/components/SectionProfile.vue'
import SectionIcons from '@/components/SectionIcons.vue'

export default {
  name: 'HomeView',
  components: {
    SectionProfile,
    SectionIcons
  }
}
</script>

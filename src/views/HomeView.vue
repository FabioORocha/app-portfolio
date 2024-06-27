<template>
  <div class="home">
    <SectionProfile />
  </div>
</template>

<script>
// @ is an alias to /src
import SectionProfile from '@/components/SectionProfile.vue'

export default {
  name: 'HomeView',
  components: {
    SectionProfile
  }
}
</script>

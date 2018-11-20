<template>
  <div class="WriterPage">
    <Hero
      title="About me"
      sub-title="Don't think you are, know you are." 
      banner-filename="banner-aboutme.jpg"
      background-position="100% 100%" />
  </div>
</template>

<script>
import Hero from '@/components/Hero'

export default {
  name: 'AboutMe',
  components: { Hero }
}
</script>


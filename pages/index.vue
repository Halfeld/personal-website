<template>
  <div class="IndexPage">
    <Hero
      title="Igor Halfeld."
      sub-title="Software Consultancy."
      banner-filename="banner-me.jpg" />
  </div>
</template>

<script>
import Hero from '@/components/Hero'

export default {
  name: 'Index',
  components: { Hero }
}
</script>
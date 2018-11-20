<template>
  <section
    :style="{
      backgroundImage: `url(/${bannerFilename})`,
      backgroundPosition: backgroundPosition
    }"
    class="section Hero">
    <div class="container HeroContainer">
      <h1 class="HeroTitle">{{ title }}</h1>
      <p class="HeroSubtitle">{{ subTitle }}</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Hero',
  props: {
    title: { type: String, default: 'Awesome title' },
    subTitle: { type: String, default: 'Awesome subtitle' },
    bannerFilename: { type: String, default: '' },
    backgroundPosition: { type: String, default: '' }
  }
}
</script>

<style lang="scss" scoped>
.Hero {
  height: 100vh;
  background-size: cover;
  position: relative;

  &::before {
    content: "";
    position: absolute;
    width: 100vw;
    height: 100vh;
    top: 0px;
    left: 0px;
    background-color: rgba(0, 0, 0, 0.75);
  }
  
  > .HeroContainer {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;

    .HeroTitle {
      color: #fff;
      font-size: 90px;
      font-weight: 700;
      margin-bottom: -20px;
    }
    .HeroSubtitle {
      color: #fff;
      font-size: 60px;
      font-weight: 300;

      > strong {
        color: #fff;
      }
    }
  }
}
</style>


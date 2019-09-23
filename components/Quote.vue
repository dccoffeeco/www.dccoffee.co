<template lang="pug">
  .quote.text-center
    slot
</template>

<script>
export default {}
</script>

<style lang="scss">
@import '@/assets/variables.scss';
@import '~vuetify/src/styles/settings/_variables.scss';

.quote {
  margin: 150px 0;
  font-family: 'Roboto Slab', sans-serif;
  font-size: 80px;
  font-weight: 700;
  line-height: 95px;

  @media (max-width: map_get($grid-breakpoints, 'md')) {
    font-size: 40px;
    line-height: 47px;
  }

  .quote-start {
    position: relative;

    &::before {
      content: '“';
      font-family: 'Cookie', sans-serif;
      font-size: 500px;
      position: absolute;
      font-weight: 500;
      color: $accent-color;
      margin-top: 100px;
      z-index: -1;
      margin-left: -83px;

      @media (max-width: map_get($grid-breakpoints, 'md')) {
        font-size: 250px;
        margin-top: 48px;
        margin-left: -42px;
      }
    }
  }
}

.emphasize {
  font-family: 'Kaushan Script', sans-serif;
  font-size: 150px;
  color: $accent-color;

  @media (max-width: map_get($grid-breakpoints, 'md')) {
    font-size: 75px;
  }
}
</style>

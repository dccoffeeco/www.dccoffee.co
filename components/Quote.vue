<template lang="pug">
  .quote.text-center
    slot
</template>

<script>
export default {}
</script>

<style lang="scss">
@import '@/assets/variables.scss';

.quote {
  margin: 150px 0;
  font-family: 'Roboto Slab', sans-serif;
  font-size: 80px;
  font-weight: 700;
  line-height: 95px;
}

.emphasize {
  font-family: 'Kaushan Script', sans-serif;
  font-size: 150px;
  color: $accent-color;
}
</style>

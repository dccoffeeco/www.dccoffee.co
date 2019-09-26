<template lang="pug">
  div
    .physical
      | Cnr. Forest rd. & Sunset Boulevard,
      | Pineslopes, Fourways.

    .schedule.my-4
      .schedule-line.d-flex
        .day Mon - Fri
        .hours 7.00 - 18:00
      .schedule-line.d-flex
        .day Sat
        .hours 8.00 - 13:00
      .schedule-line.closed.d-flex
        .day Sun
        .hours closed

    .email hello@dccoffee.co
</template>

<script>
export default {}
</script>

<style lang="scss">
.schedule {
  font-weight: bold;
  .closed {
    color: #ea4335;
  }
  .day {
    width: 100px;
  }
}
</style>

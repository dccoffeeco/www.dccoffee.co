<template lang="pug">
  v-app
    v-app-bar(absolute flat height="130" color="rgba(0, 0, 0, 0)")
      img(src="~/static/dc-coffee-co-logo.png" height="100" class="mx-10")
      v-spacer
      v-toolbar-items
        v-btn.basic(text color="#FFFFFF" max-height="50" class="mx-3") Coffee Shop
        v-btn.basic(text color="#FFFFFF" max-height="50" class="mx-3") Programs
        v-btn.basic(text color="#FFFFFF" max-height="50" class="mx-3") Community
        v-btn.basic(text color="#FFFFFF" max-height="50" class="mx-3") Login / Sign up
        v-btn.radius(outlined color="#FFFFFF" max-height="50" class="mx-3") Become a resident
    v-content
      nuxt
    v-footer(app absolute)
      span &copy; 2019
</template>

<script>
export default {
  data() {
    return {
      title: 'DC Coffee Co.'
    }
  }
}
</script>

<style lang="scss">
.v-content {
  padding-top: 0;
}

.v-toolbar__items {
  padding-top: 35px;

  .v-btn.basic {
    border-bottom: 2px solid transparent;
    transition: ease 0.2s;

    &:hover {
      border-bottom: 2px solid #168c8d;

      &::before {
        opacity: 0 !important;
      }
    }
  }
}
</style>

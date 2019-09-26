<template lang="pug">
  v-app
    v-app-bar(absolute flat height="130" color="rgba(0, 0, 0, 0)")
      img(src="~/static/dc-coffee-co-logo.png" height="100" class="mx-10")
      v-spacer
      v-toolbar-items.pr-9.d-none.d-md-block
        v-btn.basic.mx-3(
          v-for="item in menu"
          :key="item.title"
          :to="item.to"
          text
          color="#FFFFFF"
          max-height="50"
          exact
          ) {{ item.title }}
        v-btn.radius(outlined color="#FFFFFF" max-height="50" class="mx-3") Become a resident
      v-app-bar-nav-icon.d-block.d-md-none.mr-4(@click.stop="navigationDrawer = !navigationDrawer" color="#FFFFFF" x-large)
    v-navigation-drawer(v-model="navigationDrawer" right temporary app)
      v-list-item(
        v-for="item in menu"
        :key="item.title"
        :to="item.to"
        nuxt
        )
        v-list-item-content
          v-list-item-title {{ item.title }}
    v-content
      nuxt
    v-footer(app absolute)
      span &copy; 2019
</template>

<script>
export default {
  data() {
    return {
      title: 'DC Coffee Co.',
      navigationDrawer: false,
      menu: [
        {
          title: 'Coffee Shop',
          to: '#'
        },
        {
          title: 'Programs',
          to: '#'
        },
        {
          title: 'Community',
          to: '#'
        },
        {
          title: 'Login / Sign up',
          to: '#'
        }
      ]
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

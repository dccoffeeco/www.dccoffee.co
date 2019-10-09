<template lang="pug">
  v-app
    v-app-bar(absolute flat height="130" color="rgba(0, 0, 0, 0)")
      nuxt-link(to="/")
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
    v-footer
      v-row(no-gutters justify="center")
        v-col(cols="11")
          .d-block.py-8.d-md-flex
            .col.pr-6.d-flex-shrink
              img(src="~/static/dc-coffee-co-logo.png" height="70")
              .address.mt-6
                address-schedule
            .col.d-flex-shrink
              h4 Coffee Shop

              ul
                li
                  nuxt-link(to="#") Our Manifesto
                li
                  nuxt-link(to="#") Coffee
                li
                  nuxt-link(to="#") Menu
                li
                  nuxt-link(to="#") Team
                //li
                  nuxt-link(to="#") Financial Reports

            .col.d-flex-shrink
              h4 Programs & Trainings

              ul
                li
                  nuxt-link(to="#") Volunteers
                li
                  nuxt-link(to="#") Future Generation
                li
                  nuxt-link(to="#") Corporate Trainings

            .col.d-flex-shrink
              h4 Community & Events

              ul
                li
                  nuxt-link(to="#") Our Tenants
                li
                  nuxt-link(to="#") Event Calendar
                li
                  nuxt-link(to="#") Venue Hire
                li
                  nuxt-link(to="#") Become a Resident
                li &nbsp;
                li &nbsp;
                li.sm &copy; 2019 DC COFFEE CO NPC
                li.sm
                  nuxt-link(to="#") Terms & Conditions
                  nuxt-link(to="#") Privacy Policy
</template>

<script>
import AddressSchedule from '~/components/AddressSchedule.vue'

export default {
  components: {
    AddressSchedule
  },

  data() {
    return {
      title: 'DC Coffee Co.',
      navigationDrawer: false,
      menu: [
        {
          title: 'Coffee Shop',
          to: {
            name: 'coffee-shop'
          }
        },
        {
          title: 'Programs',
          to: {
            name: 'programs'
          }
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
@import '~vuetify/src/styles/settings/_variables.scss';

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

.v-footer {
  $color: #dcdcdc;
  background-color: #393939 !important;
  color: $color !important;
  font-size: 0.9rem;
  font-weight: 300;

  .col {
    width: 25%;

    @media (max-width: map_get($grid-breakpoints, 'md')) {
      width: 100%;
    }

    h4 {
      margin-bottom: 15px;
    }

    ul {
      padding-left: 0;
      li {
        list-style-type: none;
        padding-bottom: 8px;

        a {
          text-decoration: none;
          color: inherit;
          transition: ease 0.2s;

          &:hover {
            color: darken($color, 20%);
          }
        }

        &.sm {
          font-size: 0.7rem;

          a {
            margin-right: 20px;
            color: darken($color, 20%);

            &:hover {
              color: darken($color, 40%);
            }
          }
        }
      }
    }
  }
}
</style>

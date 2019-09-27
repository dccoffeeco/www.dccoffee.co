<template lang="pug">
  v-container(fluid pa-0)
    v-row(no-gutters)
      v-col
        v-parallax(src="dc-coffee-shop-banner.jpg" :height="$vuetify.breakpoint.mdAndUp ? 600 : 400")
          .header.text-center Coffee
            span.highlight &nbsp;Shop

    v-row.mb-12(no-gutters justify="center")
      v-col(:cols="$vuetify.breakpoint.mdAndUp ? 8 : 11")
        .manifesto
          h2.my-4 Our Manifesto
          p Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Tristique senectus et netus et malesuada fames ac. Sagittis id consectetur purus ut. Ut venenatis tellus in metus vulputate eu scelerisque felis imperdiet.
          p Ante in nibh mauris cursus mattis. Habitant morbi tristique senectus et netus et malesuada. At urna condimentum mattis pellentesque id. Sagittis orci a scelerisque purus semper eget duis at tellus. Eleifend mi in nulla posuere sollicitudin aliquam ultrices sagittis. Molestie nunc non blandit massa enim. Fermentum leo vel orci porta. Ut etiam sit amet nisl.
          .bloque We exist to empower individuals, transform societies and build leaders of the future.
          p Parturient montes nascetur ridiculus mus mauris. Risus quis varius quam quisque. Eu volutpat odio facilisis mauris sit amet massa vitae tortor. Dui nunc mattis enim ut tellus.

          p Proin fermentum leo vel orci porta. Nascetur ridiculus mus mauris vitae ultricies leo integer malesuada. Gravida neque convallis a cras semper auctor neque vitae. Volutpat sed cras ornare arcu dui. Nisl nisi scelerisque eu ultrices vitae auctor eu. Faucibus ornare suspendisse sed nisi lacus sed viverra. Donec et odio pellentesque diam volutpat commodo sed.

          p Tincidunt lobortis feugiat vivamus at augue eget arcu.

          p Nisl nunc mi ipsum faucibus vitae aliquet nec. Aliquam ut porttitor leo a. Massa tincidunt nunc pulvinar sapien et ligula ullamcorper. Id ornare arcu odio ut sem nulla pharetra. Habitasse platea dictumst vestibulum rhoncus est pellentesque.

          p Lorem ipsum dolor sit amet consectetur adipiscing elit. Quam id leo in vitae turpis. Diam quis enim lobortis scelerisque fermentum dui faucibus.

          p &ndash; The DC Coffee Co. Team

    v-row(no-gutters justify="center")
      v-col
        //.radius-map
        v-parallax(src="dc-radius.jpg" height="742")
          .d-flex.flex-row-reverse
            .charity-starts(:class="{'mr-9': $vuetify.breakpoint.mdAndUp, 'phone': $vuetify.breakpoint.mdAndDown}")
              h3.mb-4.head
                span Charity starts at home
              p We aim to be a blessing to the community we’re planted at, that’s why our current and every future DC shop has a mandate to run social projects within 2.5km radius.
              p To be a blessing to a community, we first need to be effective as individuals, that’s why we focus heavily on personal development and run leadership programs for volunteers, staff and corporates.
              p From individual to a family, from a family to a community, from a community to the world - step by step, through a ripple effect, we can positively impact our country.
              p By 2030 we aim to have 100 DC stores that operate as cogs in the big wheel of transformation for social justice.

    v-row.mt-12(no-gutters justify="center")
      v-col
        v-carousel(:height="$vuetify.breakpoint.mdAndUp ? 800 : 400")
          v-carousel-item(src="/photos/001.jpg")
          v-carousel-item(src="/photos/002.jpg")
          v-carousel-item(src="/photos/003.jpg")
          v-carousel-item(src="/photos/004.jpg")
          v-carousel-item(src="/photos/005.jpg")

    v-row.my-12(no-gutters justify="center")
      v-col(cols="11")
        h1.mb-6 Our Team

        v-row
          v-col(cols="12" md="3")
            v-card.fill-height(outlined)
              v-img(height="300" src="/team/neil.jpg")
              v-card-title Neil Golding
              v-card-text
                .subheader.mb-5 HEAD OF STRATEGY & INNOVATION
                p
                  | Neil is an unshakable optimist, futurist and innovator.
                  | He is in charge of our overarching mission and vision,
                  | making the impossible possible and pushing everyone
                  | to realize their full potential.

          v-col(cols="0" md="1")

          v-col(cols="12" md="3")
            v-card.fill-height(outlined)
              v-img(height="300" src="/team/mark.jpg")
              v-card-title Mark Karimov
              v-card-text
                .subheader.mb-5 HEAD OF TECHNOLOGY & OPERATIONS
                p
                  | Mark brings order into our operations by building technology, setting up processes and
                  | mobilizing people.
                  | He is in charge of our volunteering programs, development of the open source tech solutions
                  | and quality control of our products and offerings.

          v-col(cols="0" md="1")

          v-col(cols="12" md="3")
            v-card.fill-height(outlined)
              v-img(height="300" src="/team/lawrie.jpg")
              v-card-title Lawrie Golding
              v-card-text
                .subheader.mb-5 HEAD OF PROGRAMS & PARTNERSHIPS
                p
                  | Lawrie is a Change Warrior, focused on strategic Purpose Based
                  | interventions in Telecoms, FMCG, Customer Service Delivery and Event Management.
                  | He is passionate about connecting people, changing lives and creating possibilities.

    v-row.my-12(no-gutters justify="center")
      v-col.pr-12(cols="11" md="7")
        h1.mb-6 Our Story

        v-timeline(align-top dense)
          v-timeline-item(color="#168c8d")
            template(v-slot:icon)
              span.year 2017
            v-card
              v-card-text
                | DC Coffee Co. opened its doors on a rustic-style farm in Riversands
                | Johannesburg with a mission to serve and empower people. Home to an array of
                | outdoor activities, food and craft vendors as well as the venue to some of the
                | city's largest events.

          v-timeline-item(color="#168c8d")
            template(v-slot:icon)
              span.year 2018
            v-card
              v-card-text
                | DC Coffee moved to a Fourways area. With a space that can be morphed
                | to accommodate up to 60 guests and that has a beautiful deck
                | overlooking the new Fourways development, it’s a perfect spot for
                | a cup of great coffee.

          v-timeline-item(color="#168c8d")
            template(v-slot:icon)
              span.year 2019
            v-card
              v-card-text
                | With a bold vision in mind, DC Coffee Co. transformed into a non-profit
                | coffee-shop with a mission to empower individuals, transform societies
                | and build the leaders of the future.
      v-col(cols="11" md="4")
        v-img(src="/history.png")
</template>

<script>
export default {}
</script>

<style lang="scss">
@import '@/assets/variables.scss';
@import '~vuetify/src/styles/settings/_variables.scss';

.manifesto {
  font-family: 'Roboto Slab', sans-serif;

  p {
    font-size: 1.2rem;
    margin: 20px 0;
  }

  .bloque {
    border-left: 4px solid $accent-color;
    padding: 15px 30px;
    margin: 30px 0;
    font-size: 1.8rem;
    font-weight: 500;
  }
}

.charity-starts {
  width: 40%;
  background-color: #ffffff;
  color: rgba(0, 0, 0, 0.87);
  padding: 30px;
  box-shadow: 0 0 20px #666666;

  @media (max-width: map_get($grid-breakpoints, 'md')) {
    width: 100%;
  }

  .head {
    span {
      position: relative;
      z-index: 1;
    }

    &::before {
      content: '“';
      font-family: 'Cookie', sans-serif;
      font-size: 100px;
      position: absolute;
      font-weight: 500;
      color: $accent-color;
      margin-top: -37px;
      z-index: 0;
      margin-left: -17px;
    }
  }
}

.year {
  font-size: 11px;
  color: #ffffff;
  font-weight: 500;
}
</style>

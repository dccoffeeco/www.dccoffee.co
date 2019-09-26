<template lang="pug">
  v-container(fluid pa-0)
    v-row(no-gutters)
      v-col
        v-parallax(src="dc-coffee-shop-banner.jpg" height="600")
          .header.text-center Coffee
            span.highlight &nbsp;Shop

    v-row(no-gutters justify="center")
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
</template>

<script>
export default {}
</script>

<style lang="scss">
@import '@/assets/variables.scss';
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
</style>

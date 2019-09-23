<template lang="pug">
  v-container(fluid pa-0)
    v-row(no-gutters)
      v-col
        v-parallax(src="dc-main-banner.jpg" height="800")
          .tagline-wrapper.text-center
            .tagline Your Place. Your Moment.
            .why
              span.breakline.shop A non-profit coffee-shop
              span.breakline.empowers that empowers individuals, transforms societies
              span.breakline.builds and builds leaders of the future.

    v-row(justify="center")
      v-col(cols="11")
        .basic-info.pa-6.elevation-8.d-flex
          .manifesto.pr-10
            .mb-6
              | Located in the heart of Fourways, DC Coffee Co. aims to be
              | a blessing to a community by promoting active citizenship,
              | investing in social projects
              | and working with its customers and volunteers to build
              | a safer, healthier environment for all.

            v-btn.cta(x-large outlined color="#168c8d") Our Manifesto

          .map
            .mapouter
              .gmap_canvas
                iframe(
                  width="400"
                  height="270"
                  id="gmap_canvas"
                  src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3585.4108228159!2d28.011813314978834!3d-26.02011088352012!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1e9576b20daf0ef3%3A0x4784fdf670438a9c!2sDC%20Coffee%20Co%20Fourways!5e0!3m2!1sen!2sza!4v1569240804062!5m2!1sen!2sza"
                  frameborder="0"
                  scrolling="no"
                  marginheight="0"
                  marginwidth="0"
                  )

          .address.pl-6.flex-grow-1
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

    v-row(justify="center")
      v-col(cols="11")
        quote
          span(style="position:relative;z-index:1;")
            | The world has enough
            br
            | greatness, but not enough
            br
          span.emphasize(style="position:relative;top:8px;z-index:0;") goodness
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'
import Quote from '~/components/Quote.vue'

export default {
  components: {
    Logo,
    VuetifyLogo,
    Quote
  }
}
</script>

<style lang="scss">
.tagline-wrapper {
  margin-top: -150px;

  .tagline {
    font-family: 'Cookie';
    font-size: 90px;
    text-shadow: 0 1px 1px #666666;
  }

  .why {
    margin-top: 20px;
    font-size: 30px;
    font-family: 'Roboto Slab';
    text-shadow: 0 1px 1px #666666;

    .breakline {
      display: block;
    }
  }
}

.basic-info {
  position: relative;
  margin-top: -200px;
  background-color: #ffffff;

  .manifesto {
    width: 35%;
  }

  .address {
    font-size: 18px;
  }

  .schedule {
    font-weight: bold;
    .closed {
      color: #ea4335;
    }
    .day {
      width: 100px;
    }
  }
}

.mapouter {
  position: relative;
  text-align: right;
  height: 270px;
  width: 400px;
}

.gmap_canvas {
  overflow: hidden;
  background: none !important;
  height: 270px;
  width: 400px;
  border-radius: 5px;
  border: 1px solid #d3d3d3;
}
</style>

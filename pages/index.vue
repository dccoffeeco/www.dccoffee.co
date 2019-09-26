<template lang="pug">
  v-container(fluid pa-0)
    v-row(no-gutters)
      v-col
        v-parallax(src="dc-main-banner.jpg" height="800")
          .tagline-wrapper.text-center
            .tagline
              .d-block.d-md-inline Your Place.&nbsp;
              .d-block.d-md-inline Your Moment.
            .why
              span.breakline.shop A non-profit coffee shop
              span.breakline.empowers that empowers individuals, transforms societies
              span.breakline.builds and builds leaders of the future.

    v-row(no-gutters justify="center")
      v-col(cols="11")
        .basic-info.pa-6.elevation-8.d-block.d-md-flex
          .manifesto.pr-10.pb-10
            .mb-6
              | Located in the heart of Fourways, DC Coffee Co. aims to be
              | a blessing to a community by promoting active citizenship,
              | investing in social projects
              | and working with its customers and volunteers to build
              | a safer, healthier environment for all.

            v-btn.cta(x-large outlined color="#168c8d") Our Manifesto

          .map(:class="{'pb-5': $vuetify.breakpoint.mdAndDown, 'pr-6': $vuetify.breakpoint.mdAndUp}")
            iframe(
              :width="$vuetify.breakpoint.mdAndUp ? 400 : '100%'"
              height="270"
              id="gmap_canvas"
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3585.4108228159!2d28.011813314978834!3d-26.02011088352012!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1e9576b20daf0ef3%3A0x4784fdf670438a9c!2sDC%20Coffee%20Co%20Fourways!5e0!3m2!1sen!2sza!4v1569240804062!5m2!1sen!2sza"
              frameborder="0"
              scrolling="no"
              marginheight="0"
              marginwidth="0"
              )

          .address.flex-grow-1
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

    v-row(no-gutters justify="center")
      v-col(cols="11")
        quote
          .text(style="position:relative;z-index:2;")
            .quote-start.d-inline.d-md-block The world has enough&nbsp;
            .d-inline.d-md-block greatness, but not enough
          .emphasize(style="position:relative;top:8px;z-index:1;") goodness

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")
        .dual.d-block.d-md-flex
          .dual-pic(:class="{'mr-12': $vuetify.breakpoint.mdAndUp, 'mb-6 mr-4': $vuetify.breakpoint.mdAndDown}")
            .img-cover
              v-img(src="/coffee-cup-tag.jpg" contain max-width="600")
          .dual-info.pt-6
            h2.mb-4 Specialty coffee
            p Every cup of coffee we serve comes with a tag typed by hand on a 1946 Remington Rand typewriter.
            p Every tag contains an upliftment message and we encourage you to keep it and place it on your rearview mirror, desk at work or fridge at home.

            v-btn.cta.mt-4(x-large outlined color="#168c8d") About our coffee

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")
        h2.mb-6.mt-12 Our Products
        .product-line.d-block.d-md-flex
          .product.flex-grow-1.mr-8.mb-12
            .product-holder
              .d-block.d-md-flex
                v-img(src="/product-nutella-cheesecake.jpg" contain max-width="300")
              .d-block.d-md-flex
                .product-info.pt-4.pr-8
                  h3.mb-3 Nutella Cheesecake
                  p The all-time favourite, freshly made in-store, the one and only Nutella Cheesecake. And we’re not even stingy on Nutella. :-P
          .product.flex-grow-1.mr-8.mb-12
            .product-holder
              v-img(src="/product-chocolate-brownies.jpg" contain max-width="300")
              .product-info.pt-4.pr-8
                h3.mb-3 Chocolate Brownies
                p Made with 75% dark chocolate and slow-baked for over an hour, this chocolate brownie will not let you down. A perfect pick-me-up for your splendid day.
        .product-line.d-block.d-md-flex
          .product.flex-grow-1.mr-8.mb-12
            .product-holder
              v-img(src="/product-lunch-unboxed.jpg" contain max-width="300")
              .product-info.pt-4.pr-8
                h3.mb-3 The Lunch UnBoxed
                p Make your own sandwich, wrap or salad and enjoy your lunch with our fresh organic ingredients chopped and prepped in-store every day.
          .product.flex-grow-1.mr-8.mb-12
            .wording.pt-4
              p Fresh medium roast specialty coffee - check!
              p Organic ice teas, hot teas and fresh juices - check!
              p Freshly baked cakes and pastries - check!
              p All profit to empower the community - check!
            v-btn.cta.mt-4(x-large outlined color="#168c8d") See full menu

    v-row(no-gutters justify="center")
      v-col(cols="11")
        quote
          .text(style="position:relative;z-index:2;")
            .quote-start.d-inline.d-md-block When the power of love is&nbsp;
            .d-inline.d-md-block greater than the love of&nbsp;
            .d-inline.d-md-block  power, the world will know&nbsp;
          .emphasize(style="position:relative;top:8px;z-index:1;") peace

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")
        .dual.d-flex(:class="{'flex-column-reverse': $vuetify.breakpoint.mdAndDown}")
          .dual-info.pt-6.pr-12
            h2.mb-4 Invest in future generation
            p As a non-profit coffee shop we run multiple leadership, personal development and social projects with kids, students and underpriveleged.
            p We believe that its everyone’s responsibility to invest in future generation, to set an example of caring community and do everything we can to improve statistics on&nbsp;
              a.underline(href="#") fatherless homes
              | ,&nbsp;
              a.underline(href="#") domestic violence
              | ,&nbsp;
              a.underline(href="#") abuse of power
              | &nbsp;and many other issues that cripple our country.

            v-btn.cta.mt-4(x-large outlined color="#168c8d") Get involved

          .dual-pic(:class="{'ml-12': $vuetify.breakpoint.mdAndUp, 'mt-6 ml-4': $vuetify.breakpoint.mdAndDown}")
            .img-cover
              v-img.reverse(src="/future-leader.jpg" contain max-width="600")

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")
        .dual.d-flex(:class="{'flex-column-reverse': $vuetify.breakpoint.mdAndDown}")
          .dual-info.pt-6.pr-12
            h2.mb-4 Leadership program for volunteers
            p We invite students and community members to volunteer at our coffee shop and learn the skills of servant leadership, entrepreneurship, organizational performance as well as specialty coffee brewing.
            p
              | Program duration: 3 months
              br
              | Next intake: 21 October 2019

            v-btn.cta.mt-4(x-large outlined color="#168c8d") Enroll

          .dual-pic(:class="{'ml-12': $vuetify.breakpoint.mdAndUp, 'mt-6 ml-4': $vuetify.breakpoint.mdAndDown}")
            .img-cover
              v-img.reverse(src="/volunteers.jpg" contain max-width="600")

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")
        .dual.d-flex(:class="{'flex-column-reverse': $vuetify.breakpoint.mdAndDown}")
          .dual-info.pt-6.pr-12
            h2.mb-4 Corporate trainings & interventions
            p With 25 years of experience in Purpose Based Interventions, Transformational Change, Strategy and Culture development as well as Value and Behaviour alignment, ex- Group Executive Marketing and Head Coach of Vodacom Group&nbsp;
              a.underline(href="#") Lawrie Golding
              | &nbsp;and&nbsp;
              a.underline(href="#") his team
              | &nbsp;take a step forward in bringing executive and staff training programs and sessions to the corporate world.
            p Our country is in need of ethical, value-based, purpose-driven organizations that empower their employees, customers and society. Our trainings are engaging, direct and transformational.

            v-btn.cta.mt-4(x-large outlined color="#168c8d") Enquire

          .dual-pic(:class="{'ml-12': $vuetify.breakpoint.mdAndUp, 'mt-6 ml-4': $vuetify.breakpoint.mdAndDown}")
            .img-cover
              v-img.reverse(src="/corporate-trainings.jpg" contain max-width="600")

    v-row(no-gutters justify="center")
      v-col(cols="11")
        quote
          .text(style="position:relative;z-index:2;")
            .quote-start.d-inline.d-md-block There is no power for&nbsp;
            .d-inline.d-md-block change greater than a
          .emphasize(style="position:relative;top:8px;z-index:1;margin-bottom:30px;") community
          .text(style="position:relative;z-index:2;")
            .d-inline.d-md-block discovering what it cares
            .d-inline.d-md-block about.
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
@import '~vuetify/src/styles/settings/_variables.scss';
@import '@/assets/variables.scss';

.tagline-wrapper {
  margin-top: -150px;

  .tagline {
    font-family: 'Cookie', sans-serif;
    font-size: 90px;
    text-shadow: 0 1px 1px #666666;

    @media (max-width: map_get($grid-breakpoints, 'md')) {
      font-size: 60px;
    }
  }

  .why {
    margin-top: 20px;
    font-size: 30px;
    font-family: 'Roboto Slab', sans-serif;
    text-shadow: 0 1px 1px #666666;

    @media (max-width: map_get($grid-breakpoints, 'md')) {
      font-size: 24px;
    }

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

    @media (max-width: map_get($grid-breakpoints, 'md')) {
      width: 100%;
    }
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

.map {
  iframe {
    border-radius: 5px;
    border: 1px solid #d3d3d3;
  }
}

.dual-info {
  font-size: 18px;
}

.product-line {
  .product {
    width: 50%;

    @media (max-width: map_get($grid-breakpoints, 'md')) {
      width: 100%;
    }

    .wording {
      margin-top: 14px;

      p {
        margin-bottom: 0;
        font-size: 1.2rem;
      }
    }

    .product-holder {
      background-color: $accent-color;
      margin-top: 15px;
      min-height: 220px;
      color: #ffffff;
      box-shadow: 0 0 15px #ccc;

      .v-image {
        position: absolute;
        margin-top: -15px;
        margin-left: 15px;
      }

      .product-info {
        padding-left: 340px;

        @media (max-width: map_get($grid-breakpoints, 'md')) {
          padding-left: 15px;
          padding-top: 250px !important;
          padding-bottom: 15px;
        }

        p {
          font-size: 14px;
        }
      }
    }
  }
}
</style>

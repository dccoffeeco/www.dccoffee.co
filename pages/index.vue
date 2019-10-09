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

            v-btn.cta(:to="{name: 'coffee-shop'}" nuxt x-large outlined color="#168c8d") Our Manifesto

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
            address-schedule

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
              v-img(src="/coffee/coffee_003.jpg" contain max-width="600")
          .dual-info.pt-6
            h2.mb-4 Specialty coffee
            p
              | We work with the top "direct fair trade" micro-roasters in South Africa to bring you the best
              | specialty coffee in the country. Our current all-time favourite Tanzania/Brazil blend will
              | leave you wanting more and more.
            p
              | Every cup of coffee we serve comes with a tag typed by hand on a 1946 Remington Rand typewriter.
              | Each tag contains an upliftment message and we encourage you to keep it and place it on your rearview mirror, desk at work or fridge at home.

            v-btn.cta.mt-4(
              x-large
              outlined
              color="#168c8d"
              @click.stop="dialogAboutCoffee = true"
              ) About our coffee

            v-dialog(v-model="dialogAboutCoffee" max-width="600")
              v-card
                v-carousel(height="300" hide-delimiters)
                  v-carousel-item(src="/coffee/coffee_004.jpg")
                  v-carousel-item(src="/coffee/coffee_005.jpg")
                  v-carousel-item(src="/coffee/coffee_002.jpg")
                v-card-title About our coffee
                v-card-text
                  P
                    | Ethically sourced from the farms in Tanzania and Brazil,
                    | our current all-favourite coffee beans have been roasted to medium with love
                    | by our favourite micro-roastery in Centurion.
                  p
                    | Expect soft nutty undertones with a cocoa finish in every sip you take.
                  p
                    | We recommend it as a Flat White or Cortado, but it also goes down really
                    | well when brewed in V60 or Chemex.

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
              v-img(src="/product-panini.jpg" contain max-width="300")
              .product-info.pt-4.pr-8
                h3.mb-3 The Lunch UnBoxed
                p Make your own sandwich, wrap or salad and enjoy your lunch with our fresh organic ingredients chopped and prepped in-store every day.
          .product.flex-grow-1.mr-8.mb-12
            .wording.pt-4
              p Fresh medium roast specialty coffee - check!
              p Organic ice teas, hot teas and fresh juices - check!
              p Freshly baked cakes and pastries - check!
              p All profit to empower the community - check!
            v-btn.cta.mt-4(
              x-large
              outlined
              color="#168c8d"
              @click.stop="dialogFullMenu = true"
              ) See full menu

            v-dialog(v-model="dialogFullMenu" max-width="600")
              v-card
                v-card-title Our Menu
                v-card-text
                  v-expansion-panels(focusable)
                    v-expansion-panel
                      v-expansion-panel-header HOT DRINKS
                      v-expansion-panel-content
                        v-simple-table
                          template(v-slot:default)
                            thead
                              tr
                                th
                                th
                                th Small/Single
                                th Medium/Double
                            tbody
                              tr(v-for="item in menuHotDrinks" :key="item.name")
                                td
                                  div {{ item.name }}
                                  div.sub(v-if="item.sub") {{ item.sub }}
                                td
                                td {{ item.price1 ? 'R' + item.price1 : '' }}
                                td {{ item.price2 ? 'R' + item.price2 : '' }}

                    v-expansion-panel
                      v-expansion-panel-header FRUIT CRUSHES
                      v-expansion-panel-content
                        v-simple-table.mt-4
                          template(v-slot:default)
                            tbody
                              tr(v-for="item in menuFruitCrushes" :key="item.name")
                                td
                                  div {{ item.name }}
                                  div.sub(v-if="item.sub") {{ item.sub }}
                                td
                                td R{{ item.price }}

                    v-expansion-panel
                      v-expansion-panel-header CRAFT ICE TEAS
                      v-expansion-panel-content
                        v-simple-table.mt-4
                          template(v-slot:default)
                            tbody
                              tr(v-for="item in menuCraftIceTeas" :key="item.name")
                                td
                                  div {{ item.name }}
                                  div.sub(v-if="item.sub") {{ item.sub }}
                                td
                                td R{{ item.price }}

                    v-expansion-panel
                      v-expansion-panel-header FREEZOS
                      v-expansion-panel-content
                        v-simple-table.mt-4
                          template(v-slot:default)
                            tbody
                              tr(v-for="item in menuFreezos" :key="item.name")
                                td
                                  div {{ item.name }}
                                  div.sub(v-if="item.sub") {{ item.sub }}
                                td
                                td R{{ item.price }}

                    v-expansion-panel
                      v-expansion-panel-header MILKSHAKES
                      v-expansion-panel-content
                        v-simple-table.mt-4
                          template(v-slot:default)
                            tbody
                              tr(v-for="item in menuMilkshakes" :key="item.name")
                                td
                                  div {{ item.name }}
                                  div.sub(v-if="item.sub") {{ item.sub }}
                                td
                                td R{{ item.price }}

                    v-expansion-panel
                      v-expansion-panel-header EATS
                      v-expansion-panel-content
                        v-simple-table.mt-4
                          template(v-slot:default)
                            tbody
                              tr(v-for="item in menuEats" :key="item.name")
                                td
                                  div {{ item.name }}
                                  div.sub(v-if="item.sub") {{ item.sub }}
                                td
                                td R{{ item.price }}

                    v-expansion-panel
                      v-expansion-panel-header DESSERTS
                      v-expansion-panel-content
                        v-simple-table.mt-4
                          template(v-slot:default)
                            tbody
                              tr(v-for="item in menuDesserts" :key="item.name")
                                td
                                  div {{ item.name }}
                                  div.sub(v-if="item.sub") {{ item.sub }}
                                td
                                td R{{ item.price }}

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
import Quote from '~/components/Quote.vue'
import AddressSchedule from '~/components/AddressSchedule.vue'

export default {
  components: {
    Quote,
    AddressSchedule
  },

  data() {
    return {
      dialogAboutCoffee: false,
      dialogFullMenu: false,
      menuHotDrinks: [
        {
          name: 'Espresso',
          price1: 17,
          price2: 20
        },
        {
          name: 'Flat White',
          price1: 25,
          price2: null
        },
        {
          name: 'Cappuccino',
          price1: 23,
          price2: 27
        },
        {
          name: 'Americano',
          price1: 20,
          price2: 23
        },
        {
          name: 'Latte',
          price1: 24,
          price2: 28
        },
        {
          name: 'Cortado',
          price1: 19,
          price2: 22
        },
        {
          name: 'Macchiato',
          price1: 18,
          price2: 21
        },
        {
          name: 'Mocha',
          price1: 28,
          price2: 32
        },
        {
          name: 'Hot Chocolate',
          price1: 25,
          price2: 29
        },
        {
          name: 'Chai Latte',
          price1: 27,
          price2: 30
        },
        {
          name: 'Red Cappuccino',
          price1: 25,
          price2: 29
        },
        {
          name: 'Babyccino',
          price1: 5,
          price2: null
        },
        {
          name: 'Tea',
          sub: 'Five Roses, Rooibos, Green, Earl Grey',
          price1: null,
          price2: 20
        }
      ],
      menuFruitCrushes: [
        {
          name: 'Mixed Berry',
          price: 30
        },
        {
          name: 'Mango',
          price: 30
        },
        {
          name: 'Passion Fruit',
          price: 28
        },
        {
          name: 'Lemonade',
          price: 28
        }
      ],
      menuCraftIceTeas: [
        {
          name: 'Berry',
          price: 25
        },
        {
          name: 'Peach',
          price: 25
        },
        {
          name: 'Lemon',
          price: 25
        }
      ],
      menuFreezos: [
        {
          name: 'Freezoccino',
          price: 35
        },
        {
          name: 'Chocolate Freezo',
          price: 32
        },
        {
          name: 'Chai Freezo',
          price: 35
        },
        {
          name: 'Mocha Freezo',
          price: 37
        }
      ],
      menuMilkshakes: [
        {
          name: 'Chocolate',
          price: 35
        },
        {
          name: 'Salted Caramel',
          price: 35
        },
        {
          name: 'Vanilla',
          price: 35
        },
        {
          name: 'Strawberry',
          price: 35
        },
        {
          name: 'Lime',
          price: 35
        }
      ],
      menuEats: [
        {
          name: 'Jaffle',
          sub: 'Mince / Chicken / Cheese',
          price: 30
        },
        {
          name: 'Toasted Sandwich',
          sub: 'Cheese & Tomato / Chicken Mayo / Ham, Cheese & Tomato',
          price: 30
        },
        {
          name: 'Wrap',
          sub: 'Roasted chicken mayo / BBQ pulled pork, slaw, sesame',
          price: 45
        },
        {
          name: 'Panini',
          sub: 'Fajita chicken / Basil pesto chicken',
          price: 55
        },
        {
          name: 'Salad',
          sub: 'Thai chicken noodle / Pesto chicken pasta',
          price: 45
        }
      ],
      menuDesserts: [
        {
          name: 'Nutella Cheesecake',
          price: 30
        },
        {
          name: 'Chocolate brownie',
          price: 20
        },
        {
          name: 'Vanilla Fudge',
          price: 15
        },
        {
          name: 'Caramel Nut Fudge',
          price: 20
        },
        {
          name: 'Chocolate Cake',
          price: 25
        },
        {
          name: 'Carrot Cake',
          price: 30
        },
        {
          name: 'Lemon Meringue',
          price: 20
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
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

.dots {
  border-bottom: 1px dotted #999999;
}

.sub {
  font-size: 12px;
  line-height: 14px;
  color: #666666;
}
</style>

<template lang="pug">
  v-container(fluid pa-0)
    v-row(no-gutters)
      v-col
        v-parallax(src="dc-programs-banner.jpg" :height="$vuetify.breakpoint.mdAndUp ? 600 : 400")
          .header.text-center Programs
            span.highlight &nbsp;&&nbsp;
            span Events

    v-row.my-12(no-gutters justify="center")
      v-col(cols="11")
        v-row
          v-col(cols="7")
            .intro
              | Here at DC we love investing in a local community. There are several programs
              | that are available free of charge, while others require a participation fee.
              | Fear not &mdash; if you're a volunteer at our coffee shop, all of the below programs
              | are free for you. Pick what rocks your boat and we'll make sure you have
              | the time of your life.

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")
        .dual.d-flex(:class="{'flex-column-reverse': $vuetify.breakpoint.mdAndDown}")
          .dual-pic(:class="{'mr-12': $vuetify.breakpoint.mdAndUp, 'mt-6 mr-4': $vuetify.breakpoint.mdAndDown}")
            .img-cover
              v-img.reverse(src="/program-begin.jpg" contain max-width="450")

          .dual-info.pt-6.pr-12
            h2.mb-4 INDUCTION
            p
              | Induction is an event where we share our philosophy, reason for existence, our motivation and purpose
              | with everyone who comes into a contact with DC on a professional or volunteering basis.
              | All volunteers, new staff and contractors are required to participate as they begin their journey
              | with us, however our doors are open to anyone who just wants to learn more about DC and see how we do things,
              | learn about our values, how we started and what are our plans for the future.
            .d-flex.mb-4
              .flex-shrink-1.pr-6
                v-icon.mr-1 mdi-calendar
                span.icon-text First Monday of every month, 6pm
              .flex-shrink-1
                v-icon mdi-currency-usd
                span.icon-text Free

            v-btn.typeform-share.button.cta.mt-4(
              x-large
              outlined
              color="#168c8d"
              href="https://dccoffee.typeform.com/to/Rn7bCn"
              data-mode="popup"
              target="_blank"
              ) Participate

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")
        .dual.d-flex(:class="{'flex-column-reverse': $vuetify.breakpoint.mdAndDown}")
          .dual-pic(:class="{'mr-12': $vuetify.breakpoint.mdAndUp, 'mt-6 mr-4': $vuetify.breakpoint.mdAndDown}")
            .img-cover
              v-img.reverse(src="/program-volunteer.jpg" contain max-width="450")

          .dual-info.pt-6.pr-12
            h2.mb-4 VOLUNTEER
            p
              | As a non-profit coffee shop, volunteers are the backbone and the spirit of our organization.
              | If you want to learn servant leadership skills, communication skills and teamwork,
              | if you want to experience what it means to touch people's lives and empower them, to be an active citizen
              | and an advocate for change, there is no better place to be than shoulder to shoulder with
              | us behind the bar.
            p
              | You'll learn everything there is to know about specialty coffee (although it's a never-ending journey),
              | while all along meeting some amazing people, building relationships and having fun.
            .d-flex.mb-4
              .flex-shrink-1.pr-6
                v-icon.mr-1 mdi-calendar
                span.icon-text Custom
              .flex-shrink-1
                v-icon mdi-currency-usd
                span.icon-text Free

            v-btn.typeform-share.button.cta.mt-4(
              x-large
              outlined
              color="#168c8d"
              href="https://dccoffee.typeform.com/to/Rn7bCn"
              data-mode="popup"
              target="_blank"
              ) Participate

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")
        .dual.d-flex(:class="{'flex-column-reverse': $vuetify.breakpoint.mdAndDown}")
          .dual-pic(:class="{'mr-12': $vuetify.breakpoint.mdAndUp, 'mt-6 mr-4': $vuetify.breakpoint.mdAndDown}")
            .img-cover
              v-img.reverse(src="/program-coffee-making.jpg" contain max-width="450")

          .dual-info.pt-6.pr-12
            h2.mb-4 COFFEE MAKING & TASTING EVENT
            p
              | As a non-profit coffee shop, volunteers are the backbone and the spirit of our organization.
              | If you want to learn servant leadership skills, communication skills and teamwork,
              | if you want to experience what it means to touch people's lives and empower them, to be an active citizen
              | and an advocate for change, there is no better place to be than shoulder to shoulder with
              | us behind the bar.
            p
              | You'll learn everything there is to know about specialty coffee (although it's a never-ending journey),
              | while all along meeting some amazing people, building relationships and having fun.
            .d-flex.mb-4
              .flex-shrink-1.pr-6
                v-icon.mr-1 mdi-calendar
                span.icon-text Last Thursday of every month, 6.30pm
              .flex-shrink-1
                v-icon mdi-currency-usd
                span.icon-text R200 pp

            v-btn.typeform-share.button.cta.mt-4(
              x-large
              outlined
              color="#168c8d"
              href="https://dccoffee.typeform.com/to/Rn7bCn"
              data-mode="popup"
              target="_blank"
            ) Participate

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")
        .dual.d-flex(:class="{'flex-column-reverse': $vuetify.breakpoint.mdAndDown}")
          .dual-pic(:class="{'mr-12': $vuetify.breakpoint.mdAndUp, 'mt-6 mr-4': $vuetify.breakpoint.mdAndDown}")
            .img-cover
              v-img.reverse(src="/program-1-on-1.jpg" contain max-width="450")

          .dual-info.pt-6.pr-12
            h2.mb-4 1-ON-1 SOUL SEARCHING
            p
              | As a non-profit coffee shop, volunteers are the backbone and the spirit of our organization.
              | If you want to learn servant leadership skills, communication skills and teamwork,
              | if you want to experience what it means to touch people's lives and empower them, to be an active citizen
              | and an advocate for change, there is no better place to be than shoulder to shoulder with
              | us behind the bar.
            p
              | You'll learn everything there is to know about specialty coffee (although it's a never-ending journey),
              | while all along meeting some amazing people, building relationships and having fun.
            .d-flex.mb-4
              .flex-shrink-1.pr-6
                v-icon.mr-1 mdi-calendar
                span.icon-text Last Thursday of every month, 6.30pm
              .flex-shrink-1
                v-icon mdi-currency-usd
                span.icon-text R200 pp

            v-btn.typeform-share.button.cta.mt-4(
              x-large
              outlined
              color="#168c8d"
              href="https://dccoffee.typeform.com/to/Rn7bCn"
              data-mode="popup"
              target="_blank"
            ) Participate

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")
        .dual.d-flex(:class="{'flex-column-reverse': $vuetify.breakpoint.mdAndDown}")
          .dual-pic(:class="{'mr-12': $vuetify.breakpoint.mdAndUp, 'mt-6 mr-4': $vuetify.breakpoint.mdAndDown}")
            .img-cover
              v-img.reverse(src="/program-upliftment.jpg" contain max-width="450")

          .dual-info.pt-6.pr-12
            h2.mb-4 COMMUNITY UPLIFTMENT PROJECTS
            p
              | As a non-profit coffee shop, volunteers are the backbone and the spirit of our organization.
              | If you want to learn servant leadership skills, communication skills and teamwork,
              | if you want to experience what it means to touch people's lives and empower them, to be an active citizen
              | and an advocate for change, there is no better place to be than shoulder to shoulder with
              | us behind the bar.
            p
              | You'll learn everything there is to know about specialty coffee (although it's a never-ending journey),
              | while all along meeting some amazing people, building relationships and having fun.
            .d-flex.mb-4
              .flex-shrink-1.pr-6
                v-icon.mr-1 mdi-calendar
                span.icon-text Ad-hoc ongoing
              .flex-shrink-1
                v-icon mdi-currency-usd
                span.icon-text Free

            v-btn.typeform-share.button.cta.mt-4(
              x-large
              outlined
              color="#168c8d"
              href="https://dccoffee.typeform.com/to/Rn7bCn"
              data-mode="popup"
              target="_blank"
            ) Participate

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")
        .dual.d-flex(:class="{'flex-column-reverse': $vuetify.breakpoint.mdAndDown}")
          .dual-pic(:class="{'mr-12': $vuetify.breakpoint.mdAndUp, 'mt-6 mr-4': $vuetify.breakpoint.mdAndDown}")
            .img-cover
              v-img.reverse(src="/program-corporate-training.jpg" contain max-width="450")

          .dual-info.pt-6.pr-12
            h2.mb-4 CORPORATE TRAININGS
            p
              | As a non-profit coffee shop, volunteers are the backbone and the spirit of our organization.
              | If you want to learn servant leadership skills, communication skills and teamwork,
              | if you want to experience what it means to touch people's lives and empower them, to be an active citizen
              | and an advocate for change, there is no better place to be than shoulder to shoulder with
              | us behind the bar.
            p
              | You'll learn everything there is to know about specialty coffee (although it's a never-ending journey),
              | while all along meeting some amazing people, building relationships and having fun.
            .d-flex.mb-4
              .flex-shrink-1.pr-6
                v-icon.mr-1 mdi-calendar
                span.icon-text Custom
              .flex-shrink-1
                v-icon mdi-currency-usd
                span.icon-text Custom

            v-btn.typeform-share.button.cta.mt-4(
              x-large
              outlined
              color="#168c8d"
              href="https://dccoffee.typeform.com/to/Rn7bCn"
              data-mode="popup"
              target="_blank"
            ) Enquire

    v-row(no-gutters justify="center").mb-10
      v-col(cols="11")
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.intro {
  font-size: 20px;
  font-family: 'Roboto Slab', sans-serif;
}

.icon-text {
  position: relative;
  top: 1px;
  color: #666666;
  font-size: 14px;
}
</style>

<template>
  <section
    id="faq"
    class="overflow-hidden"
  >
    <v-row
      class="accent"
      no-gutters
    >
      <v-col
        class="hidden-sm-and-down"
        md="6"
      >
        <v-img
          :src="require('@/static/faq.jpg')"
          height="100%"
        />
      </v-col>

      <v-col
        class="text-center pa-5"
        cols="12"
        md="6"
      >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
          <v-col cols="12">
            <base-bubble-2
              style="transform: translateX(55%)"
            />
            <base-heading class="info--text">
              {{ localText.faqHeader }}
            </base-heading>

            <base-text class="mb-5">
              {{ localText.faqText }}
            </base-text>
          </v-col>

          <v-col
            v-for="(service, i) in services"
            :key="i"
            class="text-center mb-3"
            md="6"
          >
            <v-avatar
              class="elevation-6 mb-2"
              color="#69A1BB"
              size="64"
              tile
            >
              <v-icon
                dark
                size="52"
                v-text="service.icon"
              />
            </v-avatar>

            <base-text>
              <div
                class="mb-2"
                v-text="service.name"
              />
              <div v-html="service.blurb" />
            </base-text>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </section>
</template>

<script>
import text from '../text.json'

export default {
  name: 'FAQ',

  data: () => ({
    localText: text,
    services: [
      {
        name: 'Maternity Care',
        icon: 'mdi-Baby-Carriage',
        blurb: 'Take the time you want when you grow your family.'
      },
      {
        name: 'Vacation',
        icon: 'mdi-beach',
        blurb: 'Enjoy a worry free vacation while your business keeps earning.'
      },
      {
        name: 'Medical Leave',
        icon: 'mdi-settings',
        blurb: 'Take care of yourself or your family without a worry.'
      },
      {
        name: 'Emergency Care',
        icon: 'mdi-account',
        blurb: 'Life happens- I am here to help.'
      }
    ]
  })
}
</script>

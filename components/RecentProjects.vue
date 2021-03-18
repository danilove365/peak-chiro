<template>
  <section
    id="recent-projects"
    class="overflow-hidden"
  >
    <v-row no-gutters>
      <v-col
        class="primary text-center pa-5 white--text"
        cols="12"
        md="6"
      >
        <base-bubble-1
          style="transform: rotate(180deg) translateX(25%)"
        />

        <base-heading>
          {{ localText.reviewHeading }}
        </base-heading>

        <base-text class="mb-5">
          {{ localText.reviewText }}
        </base-text>

        <v-carousel
          cycle
        >
          <v-carousel-item
            v-for="project in projects"
            :key="project"
          >
            <testimonial
              :test="project"
            />
          </v-carousel-item>
        </v-carousel>
      </v-col>

      <v-col
        class="hidden-sm-and-down"
        md="6"
      >
        <v-img
          :src="require('@/static/adjustment.jpg')"
          height="100%"
        />
      </v-col>
    </v-row>
  </section>
</template>

<script>
import text from '../text.json'
import Testimonial from './Testimonial'

export default {
  name: 'RecentProjects',
  components: {
    Testimonial
  },
  data: () => ({
    localText: text,
    projects: text.testimonials,
    items: [
      {
        src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg'
      },
      {
        src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg'
      },
      {
        src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg'
      },
      {
        src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg'
      }
    ]
  })
}
</script>

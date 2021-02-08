<template>
  <section
    id="welcome"
    class="overflow-hidden"
  >
    <v-row no-gutters>
      <v-col
        class="hidden-sm-and-down"
        md="6"
      >
        <v-img
          :src="require('@/static/spine.jpg')"
          height="100vh"
        />
      </v-col>

      <v-col
        class="align-content-space-between layout wrap"
        cols="12"
        md="6"
      >
        <base-bubble-1
          style="transform: rotate(180deg) translateY(25%)"
        />

        <v-row
          align="left"
          justify="center"
        >
          <v-col
            cols="10"
            md="6"
          >
            <base-heading>{{ localText.welcomeHeading }}</base-heading>
            <base-text>
              {{ localText.welcomeBody }}
            </base-text>
          </v-col>
        </v-row>

        <base-bubble-2
          style="transform: rotate(180deg) translate(-200px, -15%)"
        />
      </v-col>
    </v-row>
  </section>
</template>
<script>
import text from '../text.json'
export default {
  data: () => ({
    localText: text
  })
}
</script>

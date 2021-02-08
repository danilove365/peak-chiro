<template>
  <section
    id="about"
    class="overflow-hidden"
  >
    <a name="aboutMe" />
    <v-row
      class="white"
      no-gutters
    >
      <v-col
        class="pa-5"
        cols="12"
        md="6"
      >
        <base-bubble-1 style="transform: translate(5%, -5%)" />

        <base-heading class="info--text">
          About Me
        </base-heading>

        <base-text class="mb-5">
          {{ localText.aboutMe }}
        </base-text>

        <!-- <base-subheading class="info--text">
          Skills
        </base-subheading>

        <base-text class="mb-5">
          Lorem ipsum dolor sit amet, consecte tur adipi scin e<br>
          lit. Etiam vulputate augu e vel felis gravida porta.
        </base-text>

        <v-alert
          outlined
          color="info"
        >
          <v-row
            v-for="(skill, i) in skills"
            :key="i"
            style="color: #69A1BB;"
          >
            <v-col
              class="text-uppercase"
              cols="6"
              v-text="skill.name"
            />

            <v-col
              class="text-right"
              cols="6"
              v-text="`${skill.value}%`"
            />

            <v-progress-linear
              :value="skill.value"
              color="info"
              height="8"
            />
          </v-row>
        </v-alert>
      </v-col> -->
      </v-col>
      <v-col
        class="hidden-sm-and-down"
        md="6"
        cols="12"
      >
        <v-img
          :src="require('@/static/Theresa.jpg')"
          height="100%"
        />
      </v-col>
      </v-col>
    </v-row>
  </section>
</template>

<script>
import text from '../text.json'

export default {
  data: () => ({
    localText: text,
    skills: [
      {
        name: 'Web Design',
        value: 100
      },
      {
        name: 'Web Development',
        value: 75
      },
      {
        name: 'Web Support',
        value: 90
      }
    ]
  })
}
</script>

<template>
  <v-app-bar
    v-scroll="onScroll"
    :color="!isScrolling ? 'transparent' : 'black'"
    fixed
    flat
  >
    <v-slide-x-transition>
      <v-img
        v-if="showLogo"
        :src="require('@/static/logo.png')"
        class="shrink"
        contain
        height="50"
      />
    </v-slide-x-transition>

    <v-spacer />

    <base-btn
      class="ml-3"
      small
      @click="goToSection('services')"
    >
      Services
    </base-btn>

    <base-btn
      class="ml-3"
      small
      @click="goToSection('about')"
    >
      About
    </base-btn>

    <base-btn
      class="ml-3"
      small
      @click="goToSection('recent-projects')"
    >
      Reviews
    </base-btn>

    <base-btn
      class="ml-3"
      small
      @click="goToSection('faq')"
    >
      FAQ
    </base-btn>

    <base-btn
      class="ml-3"
      small
      @click="goToSection('get-in-touch')"
    >
      Contact Me
    </base-btn>
  </v-app-bar>
</template>

<script>
export default {
  name: 'CoreAppBar',

  components: {

  },

  data: () => ({
    showLogo: false,
    isScrolling: false
  }),

  methods: {
    onScroll () {
      const offset = window.pageYOffset
      this.isScrolling = offset > 50
      this.showLogo = offset > 200
    },
    goToSection (sectionName) {
      const el = document.getElementById(sectionName)
      el.scrollIntoView()
    }
  }
}
</script>

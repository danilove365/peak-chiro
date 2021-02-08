<template>
  <v-app>
    <core-app-bar />
    <v-main>
      <nuxt />
    </v-main>
    <core-footer />
  </v-app>
</template>

<script>
import CoreAppBar from '~/components/core/AppBar'
import CoreFooter from '~/components/core/Footer'

export default {
  components: {
    CoreAppBar,
    CoreFooter
  }
}
</script>

<template>
  <div v-html="displayText" />
</template>

<script>
import marked from 'marked'
export default {
  name: 'Testimonial',
  props: {
    test: {
      type: String,
      required: true
    }
  },
  data () {
    return {
      localTest: this.test
    }
  },
  computed: {
    displayText () {
      return marked(this.localTest)
    }
  }
}
</script>

<style lang="sass" scoped>

</style>

<template>
  <div>
    <welcome />

    <services />

    <about-me />

    <recent-projects />

    <FAQ />

    <get-in-touch />
  </div>
</template>

<script>
export default {
  name: 'CoreView',

  components: {
    AboutMe: () => import('@/components/AboutMe'),
    GetInTouch: () => import('@/components/GetInTouch'),
    RecentProjects: () => import('@/components/RecentProjects'),
    Services: () => import('@/components/Services'),
    Welcome: () => import('@/components/Welcome'),
    FAQ: () => import('@/components/faq')
  }
}
</script>

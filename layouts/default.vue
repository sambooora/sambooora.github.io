<script setup lang="ts">
useHead({
  link: [{ rel: 'icon', href: '/images/icon.png' }],
  viewport:
    'width=device-width, initial-scale=1, maximum-scale=1, minimum-scale=1, user-scalable=no, viewport-fit=cover'
})

const route = useRoute()
</script>

<template>
  <div id="main-container" class="safe-area transition-colors" :class="route.meta.bg || 'bg-base-100'">
    <div>
      <Header v-if="$route.path !== '/checkout'" />
      <slot />
      <BacktoTop />
    </div>
    <Footer />
  </div>
</template>
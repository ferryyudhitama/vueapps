<template>
  <div>
    <TheHeader /> ini body
    <div class="main-content">
      <nuxt />
    </div>
    <TheFooter />
  </div>
</template>

<script>
  import TheHeader from '@/components/TheHeader/TheHeader'
  import TheFooter from '@/components/TheFooter/TheFooter'

  export default {
    components: {
      TheHeader,
      TheFooter
    }
  }
</script>
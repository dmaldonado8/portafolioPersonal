<template>
    <div class="container">
    <Front/>
      <div class="body--page">
        <Portafolio></Portafolio>
      </div>
    </div>
</template>

<script>
import Front from '~/components/FrontDescription.vue';
import Portafolio from '~/components/Portafolio.vue';
export default {
  components: {
    Front,
    Portafolio
  }
}
</script>

<style lang="scss">
  @import '../assets/variables';
  .body--page {
    background-color: $black;
  }
</style>

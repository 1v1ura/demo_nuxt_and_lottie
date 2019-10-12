<template>
  <div class="container">
    <Lottie :options="lottieOptions" />
  </div>
</template>

<script>
import Lottie from '~/components/Lottie.vue';

export default {
  components: {
    Lottie
  },
  asyncData() {
    return {
      lottieOptions: {
        animationData: require(`~/assets/SaCSS.json`)
      }
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: center / cover no-repeat url("~assets/sapporo.jpg");
  overflow: hidden;
}
</style>

<template>
  <div class="container">
    <lottie :options="defaultOptions" v-on:animCreated="handleAnimation"/>
  </div>
</template>

<script>
import Lottie from '~/components/lottie.vue';
import * as animationData from '~/assets/SaCSS.json';

export default {
  components: { Lottie },
  data() {
    return {
      defaultOptions: { animationData },
    }
  },
  methods: {
    handleAnimation: function(anim) {
      this.anim = anim;
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

<template>
  <div ref="animationConatainer"></div>
</template>

<script>
  import lottie from 'lottie-web';

  export default {
    props: {
      options: {
        type: Object,
        required: true
      }
    },
    mounted () {
      lottie.loadAnimation({
        container: this.$refs.animationConatainer,
        renderer: 'svg',
        loop: true,
        autoplay: true,
        animationData: this.options.animationData
      });
    }
  }
</script>

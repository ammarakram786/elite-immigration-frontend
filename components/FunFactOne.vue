<template>
  <section class="fact-one" v-observe-visibility="onVisibilityChange">
    <div class="container text-center">
      <img src="/assets/images/resources/decor-star-1-1.png" class="fact-one__star-1" alt="">
      <h3 class="fact-one__title counter"><countTo :startVal='0' :endVal='startCounter ? 468980 : 0' :duration='3000'></countTo></h3>
      <p class="fact-one__text">People have joined the campaigns</p>
      <img src="/assets/images/resources/decor-star-1-1.png" class="fact-one__star-2" alt="">
    </div><!-- /.container -->
  </section>
</template>

<script>

  import countTo from 'vue-count-to';
  import { ObserveVisibility } from 'vue-observe-visibility'

  export default {
    name: "FunFactOne",
    components: { countTo },
    directives: {
      ObserveVisibility
    },
    data() {
      return{
        startCounter: false
      }
    },
    methods: {
      onVisibilityChange (isVisible) {
        if (isVisible){
          this.startCounter = true;
        }
      },
    },

  }
</script>

<style scoped>

</style>

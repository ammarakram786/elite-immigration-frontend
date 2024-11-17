<template>
  <section class="static-banner-one">
    <div class="static-banner-one__bg">
      <div class="static-banner-one__bg-inner" style="background-image: url(assets/images/background/banner-bg-1-2.jpg);"></div><!-- /.static-banner-one__bg-inner -->
    </div><!-- /.static-banner-one__bg -->
    <div class="container">
      <vue-typed-js :loop="true" :strings="['Forward', 'Powerful']">
        <h2 class="static-banner-one__title">
          Let's Move <br />
          America <span class="typed-effect typing"></span>
        </h2>
      </vue-typed-js>
      <p class="static-banner-one__text">Become a part of our campaign, sign up for updates.</p>
      <form class="static-banner-one__form mc-form" data-url="https://xyz.us18.list-manage.com/subscribe/post?u=20e91746ef818cd941998c598&amp;id=cc0ee8140e">
        <div class="row">
          <div class="col-lg-6">
            <div class="static-banner-one__form-fields ">
              <input placeholder="Email Address" type="email" required="required" class="formInput">
              <input type="text" name="zip" placeholder="Zip Code">
            </div><!-- /.static-banner-one__form-fields -->
            <button type="submit" class="thm-btn static-banner-one__form-btn">Sign Up</button>
          </div><!-- /.col-lg-6 -->
        </div><!-- /.row -->
      </form>
      <div class="mc-form__response"></div><!-- /.mc-form__response -->
    </div><!-- /.container -->
  </section>
</template>

<script>
    export default {
        name: "SliderOne"
    }
</script>

<style scoped>

</style>

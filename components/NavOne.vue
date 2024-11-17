<template>
  <div>
    <div class="topbar-one">
      <div class="container">
        <div class="inner-container">
          <div class="topbar-one__left">
            <a href="mailto:needhelp@potisen.com">needhelp@potisen.com</a>
            <a href="tel:666-888-0000">666 888 0000</a>
          </div><!-- /.topbar-one__left -->
          <div class="topbar-one__right">
            <nuxt-link to="/donation"><i class="fa fa-money"></i> Donate Now</nuxt-link>
            <nuxt-link to="/volunteer"><i class="fa fa-user-o"></i>Join Us</nuxt-link>
          </div><!-- /.topbar-one__right -->
        </div><!-- /.inner-container -->
      </div><!-- /.container -->
    </div><!-- /.topbar-one -->
    <header class="site-header site-header__header-one ">
      <nav :class="`navbar navbar-expand-lg navbar-light header-navigation stricky ${sticky ? 'stricked-menu stricky-fixed' : ''}`">
        <div class="container clearfix">
          <!-- Brand and toggle get grouped for better mobile display -->
          <div class="logo-box clearfix">
            <nuxt-link class="navbar-brand" to="/">
              <img src="/assets/images/logo-dark.png" class="main-logo" width="177" alt="Awesome Image"/>
            </nuxt-link>
            <button @click="mobileToggle = !mobileToggle" class="menu-toggler" data-target=".main-navigation">
              <span class="fa fa-bars"></span>
            </button>
          </div><!-- /.logo-box -->
          <!-- Collect the nav links, forms, and other content for toggling -->
          <div :class="`main-navigation ${mobileToggle ? 'showen' : ''}`" :style="`display: ${mobileToggle ? 'block' : 'none'}`">
            <ul class=" navigation-box">
              <li class="current">
                <nuxt-link to="/">Home</nuxt-link>
                <ul class="sub-menu">
                  <li>
                    <nuxt-link to="/">Home 01</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="/index-2">Home 02</nuxt-link>
                  </li>
                  <li><a href="#">Header Versions</a>
                    <ul class="sub-menu">
                      <li>
                        <nuxt-link to="/">Header 01</nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="/index-2">Header 02</nuxt-link>
                      </li>
                    </ul><!-- /.sub-menu -->
                  </li>
                </ul><!-- /.sub-menu -->
              </li>
              <li>
                <nuxt-link to="/about">About</nuxt-link>
                <ul class="sub-menu">
                  <li>
                    <nuxt-link to="/about">About Us</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="/history">History</nuxt-link>
                  </li>
                </ul><!-- /.sub-menu -->
              </li>
              <li>
                <nuxt-link to="/donation">Contribute</nuxt-link>
                <ul class="sub-menu">
                  <li>
                    <nuxt-link to="/donation">Donations</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="/volunteer">Volunteer</nuxt-link>
                  </li>
                </ul><!-- /.sub-menu -->
              </li>
              <li>
                <a href="#">Pages</a>
                <ul class="sub-menu">
                  <li>
                    <nuxt-link to="/event">Events</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="/event-details">Event Details</nuxt-link>
                  </li>
                </ul><!-- /.sub-menu -->
              </li>

              <li>
                <a href="#news">News</a>
                <ul class="sub-menu">
                  <li>
                    <nuxt-link to="/news">News Page</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="/news-details">News Details</nuxt-link>
                  </li>
                </ul><!-- /.sub-menu -->
              </li>
              <li>
                <nuxt-link to="/contact">Contact</nuxt-link>
              </li>
            </ul>
          </div><!-- /.navbar-collapse -->
          <div class="right-side-box">
            <div class="header-social">
              <a href="#" class="fa fa-twitter"></a>
              <a href="#" class="fa fa-facebook-square"></a>
              <a href="#" class="fa fa-pinterest-p"></a>
              <a href="#" class="fa fa-instagram"></a>
            </div><!-- /.header-social -->
          </div><!-- /.right-side-box -->
        </div>
        <!-- /.container -->
      </nav>
    </header>
  </div>
</template>

<script>
  export default {
    name: "NavOne",
    data() {
      return {
        sticky: false,
        mobileToggle: false
      }
    },
    mounted() {
      window.addEventListener('scroll', this.handleScroll);
    },
    methods: {

      handleScroll() {
        if (window.scrollY > 70) {
          this.sticky = true
        } else if (window.scrollY < 70) {
          this.sticky = false
        }
      },
    }
  }
</script>

<style>
  .header-navigation .navigation-box > li > .sub-menu, .header-navigation .navigation-box > li > .sub-menu > li > .sub-menu {
    display: block;
  }
</style>

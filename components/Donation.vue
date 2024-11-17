<template>
  <section class="contact-form-one donation-page">
    <div class="container">
      <form class="contact-form-one__form contact-form-validated">
        <div class="row">
          <div class="col-lg-9">
            <h3 class="donation-page__title">Payment Info</h3>
            <div class="donation-page__amount">
              <div class="dropdown bootstrap-select">
                <div class="btn dropdown-toggle btn-light" data-toggle="dropdown" role="button" title="$">
                  <div class="filter-option">
                    <div class="filter-option-inner">
                      <div class="filter-option-inner-inner">$</div>
                    </div>
                  </div>
                </div>
                <div class="dropdown-menu">
                  <div class="inner show">
                    <ul class="dropdown-menu inner show"></ul>
                  </div>
                </div>
              </div>
              <input type="text" name="donation-money" value=".00">
            </div>
          </div><!-- /.col-lg-9 -->
        </div><!-- /.row -->
        <div class="row">
          <div class="col-lg-5">
            <h3 class="donation-page__title">Payment Info</h3>

            <div class="donation-page__payment-time">
              <p>
                <input type="radio" id="test1" name="radio-group" checked>
                <label for="test1">Online Payment</label>
              </p>
              <p>
                <input type="radio" id="test2" name="radio-group">
                <label for="test2">Offline Payment</label>
              </p>
            </div><!-- /.donation-page__payment-time -->
          </div><!-- /.col-lg-5 -->
        </div><!-- /.row -->
        <div class="row">
          <div class="col-lg-9">
            <h3 class="donation-page__title">Personal Info</h3>
            <div class="row low-gutters">
              <div class="col-lg-6">
                <input type="text" name="fname" placeholder="First Name">
              </div><!-- /.col-lg-6 -->
              <div class="col-lg-6">
                <input type="text" name="lname" placeholder="Last Name">
              </div><!-- /.col-lg-6 -->
              <div class="col-lg-6">
                <input type="text" name="email" placeholder="Email Address">
              </div><!-- /.col-lg-6 -->
              <div class="col-lg-6">
                <input type="text" name="phone" placeholder="Phone">
              </div><!-- /.col-lg-6 -->
              <div class="col-lg-6">
                <input type="text" name="address" placeholder="Address">
              </div><!-- /.col-lg-6 -->
              <div class="col-lg-6">
                <input type="text" name="address" placeholder="City">
              </div><!-- /.col-lg-6 -->
              <div class="col-lg-12">
                <textarea name="message" placeholder="Describe Yourself"></textarea>
                <div class="text-left">
                  <button type="submit" class="thm-btn contact-form-one__btn">Submit Donation</button>
                </div><!-- /.text-center -->
              </div><!-- /.col-lg-12 -->
            </div><!-- /.row -->
          </div><!-- /.col-lg-9 -->
        </div><!-- /.row -->
      </form><!-- /.contact-form-one__form -->
      <div class="result"></div><!-- /.result -->
    </div><!-- /.container -->
  </section>
</template>

<script>
  export default {
    name: "Donation"
  }
</script>

<style scoped>

</style>

<template>
  <div class="latest-project">
    <div class="latest-project__left">
      <div class="latest-project__header">
        <h3>Latest <b>Projects</b></h3>
        <p>These are my Latest Projects, Projects from office or any collegues others</p>
      </div>
      <div class="latest-project__img">
        <div class="latest-project__img--single" style="margin-bottom: 20px;">
          <img src="~assets/images/topup.png" alt="" style="width: -webkit-fill-available;">
        </div>
        <div class="latest-project__img--double">
          <div class="left">
            <img src="https://buttoncreative.agency/html/diffusal/images/project-05.jpg" alt="">
          </div>
          <div class="right">
            <img src="https://buttoncreative.agency/html/diffusal/images/project-06.jpg" alt="">
          </div>
        </div>
      </div>
    </div>
    <div class="latest-project__right">
      <div class="uk-navbar-center">
        <ul class="uk-navbar-nav latest-project__header">
          <li class="uk-active"><a href="#">All Projects</a></li>
          <li class="uk-active"><a href="#">BLANJA.com</a></li>
          <li class="uk-active"><a href="#">IQRA</a></li>
        </ul>
        <div class="latest-project__img">
          <div class="latest-project__img--double" style="margin-bottom: 20px;">
            <div class="left">
              <img src="https://buttoncreative.agency/html/diffusal/images/project-02.jpg" alt="">
            </div>
            <div class="right">
              <img src="https://buttoncreative.agency/html/diffusal/images/project-03.jpg" alt="">
            </div>
          </div>
          <div class="latest-project__img--single">
           <img src="https://buttoncreative.agency/html/diffusal/images/project-04.jpg" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.latest-project {
  display: flex;
  margin-top: 30px;
  a {
    text-transform: unset !important;
  }
  &__left {
    width: 50%;
    padding-right: 10px;
  }
  &__right {
    // margin-left: auto;
    width: 50%;
    padding-left: 10px;
  }
  &__header {
    min-height: 130px;
  }
  &__img {
    &--double {
      display: flex;
    }
  }
}
.uk-navbar-nav {
  margin-left: auto !important;
}
.left {
  width: 50%;
  padding-right: 10px;
}
.right {
  width: 50%;
  padding-left: 10px;
}
</style>
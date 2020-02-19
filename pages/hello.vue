<template>
  <div>
    <Header/>
    <div class="content">
      <div>
        <Carousel/> 
      </div>
      <div class="latest-project">
        <LatestProject/>
      </div>
    </div>
  </div>
</template>

<script>
import Header from '~/components/Header.vue'
import Carousel from '~/components/Carousel.vue'
import LatestProject from '~/components/LatestProject.vue'
export default {
  components: {
    Header,
    Carousel,
    LatestProject
  }
}
</script>

<style>
.content {
  margin-top: 70px;
  padding: 0px 80px;
}
.latest-project {
  padding: 0px 50px;
}
</style>
<template>
  <div class="carousel">
    <div id="slider">
      <transition-group tag="div" :name="transitionName" class="slides-group">
        <div v-if="show" :key="current" class="slide carousel-img" :class="slides[current].className">
          <p class="carousel-text">{{ contentText[current].text }}</p>
        </div>
      </transition-group>
      <div class="btn btn-prev" aria-label="Previous slide" @click="slide(-1)">
        &#10094;
      </div>
      <div class="btn btn-next" aria-label="Next slide" @click="slide(1)">
        &#10095;
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      current: 0,
      direction: 1,
      transitionName: "fade",
      show: false,
      slides: [
        { className: "first" },
        { className: "second" },
        { className: "third" }
      ],
      contentText: [
        { text: 'Hi, nice to meet you!' },
        { text: "I'm a Software Engineer"},
        { text: 'This web is my Portfolio'}
      ]
    }
  },
  computed: {
    backImages() {

    }
  },
  mounted() {
    this.show = true;
    this.autoSlide()
  },
  methods: {
    slide(dir) {
      this.direction = dir;
      dir === 1
        ? (this.transitionName = "slide-next")
        : (this.transitionName = "slide-prev");
      var len = this.slides.length;
      this.current = (this.current + dir % len + len) % len;
    },
    autoSlide() {
      setInterval(() => {
        this.slide(1)
      }, 5000);
    }
  }
}
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css?family=Crimson+Text");

.carousel {
  &-text {
    font-size: 60px;
    font-weight: 700;
  }
}

.first {
  background-image: url('~assets/images/carousel-1.jpg') !important;
  background-size: 100% auto;
}
.second {
  background-image: url('~assets/images/carousel-1.jpg') !important;
}
.third {
  background-image: url('~assets/images/carousel-1.jpg') !important;
  background-size: 182% auto;
}

/* FADE IN */
.fade-enter-active {
  transition: opacity 1s;
}
.fade-enter {
  opacity: 0;
}

/* GO TO NEXT SLIDE */
.slide-next-enter-active,
.slide-next-leave-active {
  transition: transform 0.5s ease-in-out;
}
.slide-next-enter {
  transform: translate(100%);
}
.slide-next-leave-to {
  transform: translate(-100%);
}

/* GO TO PREVIOUS SLIDE */
.slide-prev-enter-active,
.slide-prev-leave-active {
  transition: transform 0.5s ease-in-out;
}
.slide-prev-enter {
  transform: translate(-100%);
}
.slide-prev-leave-to {
  transform: translate(100%);
}

/* SLIDES CLASSES */

.blue {
  background: #4a69bd;
}

.red {
  background: #e55039;
}

.yellow {
  background: #f6b93b;
}

/* SLIDER STYLES */
body {
  overflow: hidden;
  margin: 0;
  font-size: 50px;
  font-family: "Crimson Text", sans-serif;
  color: #fff;
}

#slider {
  width: 100%;
  height: 62vh;
  position: relative;
}

.slide {
  width: 100%;
  height: 62vh;
  position: absolute;
  top: 0;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  p {
    color: white;
  }
}

.btn {
  z-index: 10;
  cursor: pointer;
  border: 3px solid #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 70px;
  height: 70px;
  position: absolute;
  top: calc(50% - 35px);
  left: 1%;
  transition: transform 0.3s ease-in-out;
  user-select: none;
}

.btn-next {
  left: auto;
  right: 1%;
}

.btn:hover {
  transform: scale(1.1);
}

</style>

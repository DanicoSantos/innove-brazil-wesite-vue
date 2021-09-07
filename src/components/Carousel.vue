<template>
  <div class="carousel">
    <section class="hero carousel__hero is-fullheight">
      <img :src="currentImage" style="height: 100%" alt="Some image" />
      <div class="actions">
        <span @click="prevImage" class="prev">
          <i class="fas fa-chevron-left"></i>
        </span>
        <span @click="nextImage" class="next">
          <i class="fas fa-chevron-right"></i>
        </span>
      </div>
      <div class="dots">
        <div
          v-for="(image, index) in images"
          :key="image.id"
          :class="['thumbnail-image', activeImage == index ? 'active' : '']"
          @click="activateImage(index)"
        >
          <span class="dot"></span>
        </div>
      </div>
    </section>
  </div>
</template>

<style lang="scss" scoped>
@import "../assets/scss/variables.scss";

.carousel {
  background-size: cover;
  position: relative;
}

.carousel__hero .title,
.subtitle {
  text-shadow: $baseShadow;
}

.carousel__hero {
  background: rgba($color: #000, $alpha: 0.4);
  height: 645px;
}

/* Next & previous buttons */
.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  margin-top: -22px;
  color: #fff;
  padding: 16px;
  font-weight: bold;
  font-size: 18px;
  transition: 0.6s ease;
}

/* Position the "next button" to the right */
.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}

/* On hover, add a black background color with a little bit see-through */
.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.8);
}

.dot {
  cursor: pointer;
  height: 15px;
  width: 15px;
  margin: 0 2px;
  background-color: rgba($color: #000, $alpha: 0.4);
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}

.active .dot, .dot:hover {
  background-color: #fff;
}

.dots {
  position: absolute;
  right: 5rem;
  top: 50%;
  padding: 3rem;
  background: rgba($color: #fff, $alpha: 0.20);
  border-radius: 0.5rem;
  z-index: 10001;
}

/* Fading animation */
.fade {
  -webkit-animation-name: fade;
  -webkit-animation-duration: 1.5s;
  animation-name: fade;
  animation-duration: 1.5s;
}

@-webkit-keyframes fade {
  from {opacity: .4}
  to {opacity: 1}
}

@keyframes fade {
  from {opacity: .4}
  to {opacity: 1}
}
</style>

<script>
export default {
  name: "Carousel",
  data() {
    return {
      heroSize: "",
      images: [
        {
          id: 1,
          src: "/img/banner-home.jpg",
        },
        {
          id: 2,
          src: "/img/banner-about.jpg",
        },
      ],
      activeImage: 0,
    };
  },
  computed: {
    // currentImage gets called whenever activeImage changes
    // and is the reason why we don't have to worry about the
    // big image getting updated
    currentImage() {
      return this.images[this.activeImage].src;
    },
  },
  methods: {
    // Go forward on the images array
    // or go at the first image if you can't go forward :/
    nextImage() {
      var active = this.activeImage + 1;
      if (active >= this.images.length) {
        active = 0;
      }
      this.activateImage(active);
    },
    // Go backwards on the images array
    // or go at the last image
    prevImage() {
      var active = this.activeImage - 1;
      if (active < 0) {
        active = this.images.length - 1;
      }
      this.activateImage(active);
    },
    activateImage(imageIndex) {
      this.activeImage = imageIndex;
    },
  },
};
</script>

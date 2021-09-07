<template>
  <div class="carousel">
    <section class="hero carousel__hero is-fullheight">
      <img
        :src="currentImage"
        style="height: 100%"
        alt="Some image"
      />
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
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}
</style>

<script>
export default {
  name: "Carousel",
  data() {
    return {
      heroSize: "",
      items: [],
    };
  },
};
</script>

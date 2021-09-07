<template>
  <div class="carousel">
    <section class="hero carousel__hero is-fullheight">
      <div class="overlay overlay--filter-black"></div>
      <div class="carousel-container">
        <figure :class="{ fade: hasChange }">
          <img @load="onImageLoad" :src="currentImage" style="height: 100%" alt="Some image" />
        </figure>
      </div>
      <div class="hero-body">
        <div class="container">
          <div class="columns">
            <div class="column is-7">
              <h1 class="title is-size-2">{{ currentImageTitle }}</h1>
            </div>
          </div>
        </div>
      </div>
      <div class="dots">
        <div
          v-for="(image, index) in images"
          :key="image.id"
          :class="[activeImage == index ? 'active' : '']"
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

.carousel-container {
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: 9998;
}

.carousel-container figure {
  width: 100%;
  height: 100%;
}

.carousel__hero .title,
.subtitle {
  text-shadow: $baseShadow;
}

.carousel__hero {
  background: rgba($color: #000, $alpha: 0.4);
  height: 645px;
}

.hero-body {
  position: relative;
  z-index: 9999;
}

.hero-body .title,
.subtitle {
  color: #fff;
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

.active .dot,
.dot:hover {
  background-color: #fff;
}

.dots {
  position: absolute;
  right: 10rem;
  top: 50%;
  padding: 3rem;
  background: rgba($color: #fff, $alpha: 0.4);
  border-radius: 0.5rem;
  z-index: 10000;
}

/* Fading animation */
.fade {
  -webkit-animation-name: fade;
  -webkit-animation-duration: 4s;
  animation-name: fade;
  animation-duration: 4s;
}

@-webkit-keyframes fade {
  from {
    opacity: 0.4;
  }
  to {
    opacity: 1;
  }
}

@keyframes fade {
  from {
    opacity: 0.4;
  }
  to {
    opacity: 1;
  }
}

.overlay {
  position: absolute;
  height: 100%;
  width: 100%;
  z-index: 9999;
}

.overlay--filter-black {
  background: rgba($color: #000, $alpha: 0.4);
}
</style>

<script>
export default {
  name: "Carousel",
  data() {
    return {
      heroSize: "",
      hasChange: false,
      images: [
        {
          id: 1,
          src: "/img/banner-home.jpg",
          title: "Title 1",
          subtitle: "Subtitle 1",
        },
        {
          id: 2,
          src: "/img/banner-about.jpg",
          title: "Title 2",
          subtitle: "Subtitle 2",
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

    currentImageTitle() {
      return this.images[this.activeImage].title;
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
      this.hasChange = false;
    },
    activateImage(imageIndex) {
      this.activeImage = imageIndex;
      this.hasChange = this.hasChange ? false : true;      
    },    

    onImageLoad() {
      this.hasChange = this.hasChange ? false : true;
    }
  },
};
</script>

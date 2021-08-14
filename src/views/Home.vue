<template>
  <div class="home">
    <Carousel />
    <Partners />
  </div>
</template>

<script>
// @ is an alias to /src
import Carousel from "@/components/Carousel";
import Partners from "@/components/Partners";

export default {
  name: "Home",
  components: {
    Carousel,
    Partners,
  },
};
</script>

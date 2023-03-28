<template>
  <div>
    <vue-carousel :per-page="1">
      <vue-carousel-slide v-for="(slide, index) in slides" :key="index">
        <div
          class="slide"
          :style="{ 'background-image': 'url(' + slide.image + ')' }"
        >
          <h2>{{ slide.title }}</h2>
          <p>{{ slide.text }}</p>
        </div>
      </vue-carousel-slide>
    </vue-carousel>
  </div>
</template>

<script>
import VueCarousel from "vue-carousel";

export default {
  name: "AppSlider",
  components: {
    VueCarousel,
  },
  data() {
    return {
      slides: [
        {
          image: "../assets/images/bg-1.jpg",
          title: "Slide 1",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
        },
        {
          image: "/path/to/image2.jpg",
          title: "Slide 2",
          text: "Praesent euismod, augue quis bibendum pharetra, nisi turpis consectetur justo.",
        },
        {
          image: "/path/to/image3.jpg",
          title: "Slide 3",
          text: "Sed in aliquet nulla. Nulla vel quam vitae velit euismod lobortis.",
        },
      ],
    };
  },
};
</script>

<style scoped>
.slide {
  height: 500px;
  background-size: cover;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: white;
  text-align: center;
}

.slide h2 {
  font-size: 36px;
  margin-bottom: 20px;
}

.slide p {
  font-size: 24px;
}
</style>

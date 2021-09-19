<template>
<section>
  <main class="container p-3">
    <div class="text-center">
      <h2 class="p-3">RECENT CAUSES</h2>
      <div class="b-line "></div>
      <p>We run projects in over 30 countries in 5 continent</p>
    </div>
    <div class="row text-center">
      <div class="col ">
        <img
          v-for="image in images"
          :key="image.img"
          :src="image.img"
          class="p-2 img-fluid mt-3"
        />
      </div>    
    </div>
  </main>
    <ArticlesSection/>
    </section>
</template>

<script>
import ArticlesSection from '@/components/ArticlesSection.vue';
export default {
  name: "ThirdMainSection",
  data() {
    return {
      images: [
        {
          img: require("@/assets/avada-charity-fair-trade-featured-200x150.jpg"),
        },
        {
          img: require("@/assets/avada-charity-shelter-featured-200x150.jpg"),
        },
        {
          img: require("@/assets/avada-charity-farming-featured-200x150.jpg"),
        },
        {
          img: require("@/assets/avada-charity-vaccines-featured-200x150.jpg"),
        },
      ],
    };
  },

  components:{
      ArticlesSection,
  }
};
</script>

<style lang="scss" scoped></style>

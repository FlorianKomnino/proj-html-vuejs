<script>
import StatsCard from '../CardsComponents/StatsCard.vue';

export default {
  name: 'FooterCarousel',

  components: {
    StatsCard,
  },

  data() {
    return {
      imgPaths: [
        '../../assets/instagram_img1.jpg',
        '../../assets/instagram_img2.jpg',
        '../../assets/instagram_img3.jpg',
        '../../assets/instagram_img4.jpg',
        '../../assets/instagram_img5.jpg',
        '../../assets/instagram_img6.jpg',
        '../../assets/instagram_img7.jpg',
        '../../assets/instagram_img8.jpg',
        '../../assets/instagram_img9.jpg',
        '../../assets/instagram_img10.jpg',
      ]
    }
  },

  methods: {
    getImagePath: function (imgPath) {
      return new URL(imgPath, import.meta.url).href;
    },
  }
}
</script>

<template>
  <div class="col-12">

    <figure>
      <img v-for="imagePath, index in imgPaths" :src="getImagePath(imgPaths[index])" class="img-fluid"
        alt="instrument on background image">
    </figure>
  </div>
</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables" as *;
@use "../../../node_modules/bootstrap" as *;

figure {
  width: 100vw;
  height: 250px;
  display: flex;
  margin: 0;
  overflow: hidden;

  img {
    height: 100%;
  }

}
</style>

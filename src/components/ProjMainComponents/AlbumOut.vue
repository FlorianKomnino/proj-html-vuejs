<script>
import ProjButton from '../ProjButton.vue';

export default {
  name: 'AlbumOut',

  components: {
    ProjButton,
  },

  data() {
    return {

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

  <div class="col">
    <figure>
      <img :src="getImagePath('../../assets/cms_parallax.jpg')" class="img-fluid" alt="">
      <div class="albumOutText col-9">
        <h3>
          instrumental rock
        </h3>
        <h1>
          album out now
        </h1>
        <ProjButton :textOnTheButton="`read more`" class="text-uppercase customButton" />
      </div>
    </figure>
  </div>



</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables" as *;
@use "../../../node_modules/bootstrap" as *;

figure {
  width: 100vw;
  height: 680px;
  position: relative;
  margin: 0;
  overflow: hidden;

  div.albumOutText {
    position: absolute;
    top: 45%;
    left: 50%;
    transform: translate(-50%, -50%);

    h3 {
      color: $brandOrange;
      text-transform: uppercase;
      margin-bottom: 20px;
      font-size: 1.1rem;
      font-weight: 700;
    }

    h1 {
      color: $brandWhite;
      text-transform: uppercase;
      font-size: 4.25rem;
      font-weight: 700;
      margin-bottom: 30px;
      transform: scaleY(1.3);
    }
  }

  .customButton {
    font-size: 0.8rem;
  }
}
</style>

<script>
import { store } from '../store.js';
import FirstSense from './ProjMainComponents/FirstSense.vue';
import MainJumbo from './ProjMainComponents/MainJumbo.vue';
import MainVideo from './ProjMainComponents/MainVideo.vue';
import SecondSense from './ProjMainComponents/SecondSense.vue';
import AlbumOut from './ProjMainComponents/AlbumOut.vue';
import MainStats from './ProjMainComponents/MainStats.vue';
import ProjFooter from './ProjFooter.vue';

export default {
  name: 'ProjMain',

  components: {
    FirstSense,
    MainJumbo,
    MainVideo,
    SecondSense,
    AlbumOut,
    MainStats,
    ProjFooter,
  },

  data() {
    return {
      store,
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
    <MainJumbo />
    <FirstSense :senseContentText="store.senseSectionText" />
    <MainVideo />
    <SecondSense />
    <AlbumOut />
    <MainStats />
    <ProjFooter />
  </div>



</template>

<style lang="scss" scoped>
@use "../../styles/partials/variables" as *;
@use "../../node_modules/bootstrap" as *;

figure {
  width: 100vw;
  height: 700px;
  position: relative;
  margin: 0;
  overflow: hidden;

  div.jumboText {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;

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
      font-size: 4.5rem;
      font-weight: 700;
      margin-bottom: 30px;
      transform: scaleY(1.25);
    }
  }

  .customButton {
    font-size: 0.8rem;
  }
}

.frontViewCards {
  margin-top: 0;
  position: absolute;
  top: 780px;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;

  article {
    height: 330px;
    padding: 0.75rem;
  }
}
</style>

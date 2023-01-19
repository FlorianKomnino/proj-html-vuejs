<script>
import ProjButton from './ProjButton.vue';
import ProjCard from './ProjCard.vue';

export default {
  name: 'ProjMain',

  components: {
    ProjButton,
    ProjCard,
  },

  data() {
    return {
      topCardsProps: {
        titleOriginalIdeas: 'original ideas',
        titleMusicStudio: 'music stuidio',
        titleAcousticCovers: 'acoustic covers',
      },
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
  <figure>
    <img :src="getImagePath('../assets/jumbotronA.png')" class="img-fluid" alt="">
    <div class="jumboText">
      <h3>
        instrumental rock
      </h3>
      <h1>
        music in this video
      </h1>
      <div>
        <!-- component still to be created -->
      </div>
      <ProjButton :textOnTheButton="`read more`" />
    </div>
  </figure>
  <div class="frontViewCards col-9 d-flex">
    <article>
      <!-- iconClass set momentarily to different icon because given speaker icon was not found -->
      <ProjCard :titleText="topCardsProps.titleOriginalIdeas" iconClass="fa-regular fa-lightbulb" />
    </article>
    <article>
      <ProjCard :titleText="topCardsProps.titleMusicStudio" iconClass="fa-solid fa-record-vinyl" />
    </article>
    <article>
      <ProjCard :titleText="topCardsProps.titleAcousticCovers" iconClass="fa-solid fa-headset" />
    </article>
  </div>
</template>

<style lang="scss" scoped>
@use "../../styles/partials/variables" as *;
@use "../../node_modules/bootstrap" as *;

figure {
  height: calc(100vh - 100px);
  position: relative;
  margin-bottom: 0;
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
}

.frontViewCards {
  margin-top: 0;
  position: absolute;
  top: 100vh;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;

  article {
    height: 340px;
    padding: 0.75rem;
  }
}
</style>

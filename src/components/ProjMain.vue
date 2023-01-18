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
      frontViewCardsTitles: {
        contentTitleOriginalIdeas: 'original ideas',
        contentTitleMusicStudio: 'music stuidio',
        contentTitleAcousticCovers: 'acoustic covers',
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
    <img src="../assets/jumbotronA.png" alt="">
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
    <div class="frontViewCards">
      <article>
        <ProjCard :titleText="frontViewCardsTitles.contentTitleOriginalIdeas" />
      </article>
      <article>
        <ProjCard :titleText="frontViewCardsTitles.contentTitleMusicStudio" />
      </article>
      <article>
        <ProjCard :titleText="frontViewCardsTitles.contentTitleAcousticCovers" />
      </article>
    </div>
  </figure>
</template>

<style lang="scss" scoped>
@use "../../styles/partials/variables" as *;

figure {
  height: calc(100vh - 80px);
  position: relative;
  margin-bottom: 0;

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
}
</style>

<script>
import { store } from '../../store.js';
import ProjButton from '../ProjButton.vue';
import ProjCard from '../ProjCard.vue';

export default {
  name: 'MainJumbo',

  components: {
    ProjButton,
    ProjCard,
  },

  data() {
    return {
      store,
      topCardsProps: {
        titleOriginalIdeas: 'original ideas',
        titleMusicStudio: 'music studio',
        titleAcousticCovers: 'acoustic covers',
      },
      cardsTextProps: "contrary popular belief, lorem ipsum not simply ipsum random text",
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
      <img :src="getImagePath('../../assets/jumbotronA.png')" class="img-fluid" alt="jumbo image">
      <div class="jumboText">
        <h3>
          instrumental rock
        </h3>
        <h1>
          music in this video
        </h1>
        <ProjButton :textOnTheButton="`read more`" class="text-uppercase customButton" />
      </div>
    </figure>
    <div class="frontViewCards col-10 d-flex">
      <article>
        <ProjCard :titleText="topCardsProps.titleOriginalIdeas" class="customBgColor"
          iconClass="fa-regular fa-lightbulb" :textContent="cardsTextProps" />
      </article>
      <article>
        <ProjCard :titleText="topCardsProps.titleMusicStudio" class="customBgColor" iconClass="fa-solid fa-record-vinyl"
          :textContent="cardsTextProps" />
      </article>
      <article>
        <ProjCard :titleText="topCardsProps.titleAcousticCovers" class="customBgColor" iconClass="fa-solid fa-headset"
          :textContent="cardsTextProps" />
      </article>
    </div>
  </div>



</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables" as *;
@use "../../../node_modules/bootstrap" as *;

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

    .customBgColor {
      background-color: $alternativeBlack;
    }
  }
}
</style>

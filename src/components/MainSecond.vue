<script>
import ProjButton from './ProjButton.vue';
import ProjCard from './ProjCard.vue';

export default {
  name: 'MainSecond',

  props: {
    senseContentText: String,
  },

  components: {
    ProjButton,
    ProjCard,
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
  <section class="senseSection">
    <div class="container">
      <div class="row">
        <div class="col-9 m-auto">

          <h3>
            who we are
          </h3>
          <h1>
            sense the jazz
          </h1>
          <p>
            {{ senseContentText }}
          </p>
          <ProjButton :textOnTheButton="`read more`" class="text-uppercase customButton" />
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "../../styles/partials/variables" as *;
@use "../../node_modules/bootstrap" as *;

section.senseSection {
  background-color: $brandBlack;
  width: 100vw;
  padding: 280px 280px 90px 280px;
  text-align: center;

  h3 {
    font-size: 0.7rem;
    color: $brandOrange;
    text-transform: uppercase;
    transform: scaleX(1.25);

  }

  h1 {
    color: $brandWhite;
    text-transform: uppercase;
    padding-top: 0.5rem;
    font-weight: 600;
    transform: scaleY(1.4);
  }

  p {
    padding: 1.75rem 3rem;
    font-size: 0.75rem;
    font-weight: 300;
    line-height: 1.5rem;
    text-transform: capitalize;
    color: $brandWhite;
  }

  .customButton {
    font-size: 0.8rem;
  }
}
</style>

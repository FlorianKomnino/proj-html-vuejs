<script>
import ProjButton from './ProjButton.vue';
import ProjCard from './ProjCard.vue';

export default {
  name: 'MainSecond',

  components: {
    ProjButton,
    ProjCard,
  },

  data() {
    return {
      topCardsProps: {

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
  <div class="jumboText">
    <h3>
      who we are
    </h3>
    <h1>
      sense the jazz
    </h1>
    <ProjButton :textOnTheButton="`read more`" />
  </div>
</template>

<style lang="scss" scoped>
@use "../../styles/partials/variables" as *;
@use "../../node_modules/bootstrap" as *;

div.jumboText {
  background-color: $alternativeBlack;
  width: 100vw;

  h3 {
    font-size: 1.2rem;
    color: $brandOrange;
  }

  h1 {
    color: $brandWhite;
  }
}
</style>

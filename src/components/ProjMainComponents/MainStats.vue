<script>
import StatsCard from '../StatsCard.vue';

export default {
  name: 'MainStats',

  components: {
    StatsCard,
  },

  data() {
    return {
      statsNumbersProps: {
        concerts: "163",
        happyClients: "145",
        musicAwards: "72",
        totalSongs: "182",
      },
      cardsTextPropsArray: [
        "concerts",
        "happy clients",
        "music awards",
        "total songs",
      ],
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
      <img :src="getImagePath('../../assets/counter_parallax.jpg')" class="img-fluid"
        alt="instrument on background image">
      <div class="statsCards d-flex">
        <article>
          <!-- iconClass set momentarily to different icon because given speaker icon was not found -->
          <StatsCard :titleText="statsNumbersProps.concerts" :textContent="cardsTextPropsArray[0]"
            iconClass="fa-solid fa-child-reaching" />
        </article>
        <article>
          <StatsCard :titleText="statsNumbersProps.happyClients" :textContent="cardsTextPropsArray[1]"
            iconClass="fa-solid fa-rocket" />
        </article>
        <article>
          <StatsCard :titleText="statsNumbersProps.musicAwards" :textContent="cardsTextPropsArray[2]"
            iconClass="fa-solid fa-trophy" />
        </article>
        <article>
          <StatsCard :titleText="statsNumbersProps.totalSongs" :textContent="cardsTextPropsArray[3]"
            iconClass="fa-solid fa-music" />
        </article>
      </div>
    </figure>
  </div>
</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables" as *;
@use "../../../node_modules/bootstrap" as *;

figure {
  width: 100vw;
  height: 350px;
  position: relative;
  margin: 0;
  overflow: hidden;

  .statsCards {
    position: absolute;
    width: 100%;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    justify-content: center;

    article {
      height: 300px;
      width: 250px;
      color: $brandWhite;
      margin: 0 20px;

    }
  }
}
</style>

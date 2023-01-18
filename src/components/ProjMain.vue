<script>

export default {
  name: 'ProjMain',

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
    </div>

  </figure>
</template>

<style lang="scss" scoped>
@use "../../styles/partials/variables" as *;

figure {
  height: calc(100vh - 80px);
  position: relative;

  div.jumboText {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: white;
    text-align: center;
  }
}
</style>

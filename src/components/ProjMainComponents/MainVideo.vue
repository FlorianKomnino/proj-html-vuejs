<script>

export default {
  name: 'MainVideo',

  props: {
  },

  components: {
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
    <figure>
      <img :src="getImagePath('../../assets/Video-1536x541.jpg')" class="img-fluid" alt="">
      <div class="MusicVideoTitles">
        <h3>
          <i class="fa-regular fa-circle-play"></i>
        </h3>
        <h1>
          new music video
        </h1>
      </div>
    </figure>
  </section>
</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables" as *;
@use "../../../node_modules/bootstrap" as *;

section.senseSection {
  text-align: center;

  figure {
    position: relative;
    margin-bottom: 0;
  }

  h3 {
    font-size: 0.7rem;
    color: $brandOrange;
  }

  h1 {
    color: $brandWhite;
    text-transform: uppercase;
    padding-top: 1rem;
    font-weight: 700;
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

  div.MusicVideoTitles {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);

    i {
      font-size: 6rem;
    }
  }

  .customButton {
    font-size: 0.8rem;
  }
}
</style>

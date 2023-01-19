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
    <div class="container-fluid">
      <div class="row">
        <div class="col-12 m-auto">


          <figure>
            <img :src="getImagePath('../../assets/Video-1024x361.jpg')" class="img-fluid" alt="">
            <div class="jumboText">
              <h3>
                play button
              </h3>
              <h1>
                new music video
              </h1>
            </div>
          </figure>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables" as *;
@use "../../../node_modules/bootstrap" as *;

section.senseSection {
  text-align: center;

  h3 {
    font-size: 0.7rem;
    color: $brandOrange;
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

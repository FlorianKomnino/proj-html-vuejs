<script>

export default {
  name: 'BlogCard',

  props: {
    titleText: String,
    imgPath: String,
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
  <div class="cardWrapper">
    <figure>
      <img :src="getImagePath(imgPath)" class="img-fluid" alt="stream image">
    </figure>
    <h4>
      {{ titleText }}
    </h4>
    <p>
      stream on : <i class="fa-brands fa-spotify"></i> <i class="fa-brands fa-youtube"></i> <i
        class="fa-brands fa-itunes-note"></i> <i class="fa-brands fa-soundcloud"></i> <i
        class="fa-brands fa-safari"></i>
    </p>
  </div>
</template>

<style lang="scss" scoped>
@use "../../styles/partials/variables" as *;
@use "../../node_modules/bootstrap" as *;

.cardWrapper {
  color: $brandWhite;
  height: 100%;
  width: 100%;

  h4 {
    font-size: 1rem;
    font-weight: 700;
    margin-top: 10px;
    text-transform: uppercase;
    transform: scaleY(1.25);
  }

  p {
    font-size: 0.75rem;
    font-weight: 300;
    text-transform: capitalize;
  }

  i {
    font-size: 0.75rem;
    font-weight: 300;
    margin: 0 0.3rem;
  }
}
</style>

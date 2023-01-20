<script>

export default {
  name: 'ProjCard',

  props: {
    titleText: String,
    textContent: String,
    iconImgUrl: String,
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
      <img :src="getImagePath(iconImgUrl)" alt="theme icon">
    </figure>
    <h4>
      {{ titleText }}
    </h4>
    <p>
      {{ textContent }}
    </p>
  </div>
</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables" as *;

.cardWrapper {
  color: $brandWhite;
  height: 100%;
  width: 100%;
  padding: 3rem;
  text-align: center;

  figure {
    width: 90px;
    height: 90px;
    filter: invert(100%) sepia(53%) saturate(689%) hue-rotate(240deg) brightness(108%) contrast(106%);
    font-size: 5rem;
    margin-top: 15px;
    margin: auto;

    img {
      height: 100%;
    }
  }

  h4 {
    margin-top: 35px;
    text-transform: uppercase;
    transform: scaleY(1.25);
  }

  p {
    margin-top: 10px;
    font-size: 0.75rem;
    line-height: 1.2rem;
    font-weight: 300;
    text-transform: capitalize;
  }
}
</style>

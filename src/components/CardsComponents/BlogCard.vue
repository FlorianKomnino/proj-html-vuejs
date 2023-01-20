<script>

export default {
  name: 'BlogCard',

  props: {
    imgPath: String,
    titleText: String,
    postDate: String,
    postTeaser: String,
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
    <time>
      <i class="fa-solid fa-calendar-days"></i>
      {{ postDate }}
    </time>
    <p>
      {{ postTeaser }}
    </p>
  </div>
</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables" as *;
@use "../../../node_modules/bootstrap" as *;

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

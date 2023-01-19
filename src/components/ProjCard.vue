<script>

export default {
  name: 'ProjCard',

  props: {
    titleText: String,
    iconClass: String,
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
    <i :class="iconClass"></i>
    <h4>
      {{ titleText }}
    </h4>
    <p>
      contrary popular belief, lorem ipsum not simply ipsum random text
    </p>
  </div>
</template>

<style lang="scss" scoped>
@use "../../styles/partials/variables" as *;

.cardWrapper {
  color: $brandWhite;
  height: 100%;
  width: 100%;
  background-color: $alternativeBlack;
  padding: 3rem;

  i {
    font-size: 5rem;
    margin-top: 15px;
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

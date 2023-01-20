<script>

export default {
  name: 'StatsCard',

  props: {
    titleText: String,
    textContent: String,
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
      {{ textContent }}
    </p>
  </div>
</template>

<style lang="scss" scoped>
@use "../../styles/partials/variables" as *;

.cardWrapper {
  color: $brandWhite;
  height: 100%;
  width: 100%;
  margin-left: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;

  i {
    font-size: 3.5rem;
    margin-top: 15px;
  }

  h4 {
    font-size: 2.5rem;
    margin-top: 35px;
    text-transform: uppercase;
    transform: scaleY(1.25);
  }

  p {
    margin-top: 10px;
    font-size: 1rem;
    line-height: 1.2rem;
    font-weight: 600;
    text-transform: uppercase;
  }
}
</style>

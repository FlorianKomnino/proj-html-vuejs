<script>

export default {
  name: 'ProjButton',

  props: {
    textOnTheButton: String,
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
  <button>
    {{ textOnTheButton }}
  </button>
</template>

<style lang="scss" scoped>
@use "../../styles/partials/variables" as *;

button {
  width: 150px;
  height: 40px;
  color: $brandWhite;
  background-color: transparent;
  border: 0.25px solid $brandOrange;
  font-weight: 600;
  transform: scaleY(1.1);
}
</style>

<script>

export default {
  name: 'ProjCard',

  props: {
    titleText: String,
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
    <i class="fa-solid fa-compact-disc"></i>
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
  background-color: green;
}
</style>

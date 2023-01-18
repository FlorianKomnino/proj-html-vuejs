<script>
import ProjMain from './ProjMain.vue';

export default {
  name: 'ProjHeader',

  components: {
    ProjMain,
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
  <div id="topBar">
    <figure>
      <img :src="getImagePath('../assets/logo.png')" alt="">
    </figure>

    <ul>
      <li>
        <!-- this will be a v-for -->
        Example text
      </li>
    </ul>
  </div>

  <ProjMain />
</template>

<style lang="scss" scoped>
@use "../../styles/partials/variables" as *;

#topBar {
  margin: 0 !important;
  padding: 0 !important;
  background-color: $brandBlack;
  height: 82.5px;
  width: 100vw;
  display: flex;
  justify-content: space-between;

  ul {
    padding: 0 3rem;

    li {
      color: $brandWhite;
    }
  }
}
</style>

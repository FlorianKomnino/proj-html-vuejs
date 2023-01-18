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

<template class="row">
  <div class="col-12" id="topBar">
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
</template>

<style lang="scss" scoped>
@use "../../styles/partials/variables" as *;

#topBar {
  background-color: $blackMetal;
  height: 82.5px;
  width: 100vw;
  display: flex;
  justify-content: space-between;

  li {
    color: white;
  }
}
</style>

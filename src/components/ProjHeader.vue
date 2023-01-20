<script>
import ProjMain from './ProjMain.vue';

export default {
  name: 'ProjHeader',

  components: {
    ProjMain,
  },

  data() {
    return {
      menuList: [
        "home",
        "blog",
        "events",
        "gallery",
        "about us",
        "shop",
      ],
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
  <div class="row">
    <div class="col">
      <div id="topBar">
        <figure>
          <img :src="getImagePath('../assets/logo.png')" alt="">
        </figure>

        <ul class="d-flex">
          <li v-for="menuItem in menuList">
            {{ menuItem }}
            <i v-if="menuItem === 'events' || menuItem === 'shop'" class="fa-solid fa-angle-down"></i>
          </li>
          <li>
            <i class="fa-sharp fa-solid fa-magnifying-glass"></i>
          </li>
        </ul>
      </div>

    </div>
  </div>

  <ProjMain />

</template>

<style lang="scss" scoped>
@use "../../styles/partials/variables" as *;
@use "../../node_modules/bootstrap" as *;

#topBar {
  background-color: $brandBlack;
  height: 82.5px;
  width: 100vw;
  display: flex;
  justify-content: space-between;

  figure {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-left: 1.5rem;
    margin-bottom: 0;
  }

  ul {
    list-style-type: none;
    margin-bottom: 0;
    padding: 0 3rem;

    li {
      color: $brandWhite;
      list-style-type: none;
      margin: auto 1.4rem;
      font-size: 0.75rem;
      text-transform: uppercase;
      font-weight: 700;
    }
  }
}
</style>

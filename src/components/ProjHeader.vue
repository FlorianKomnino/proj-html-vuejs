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

      isEventsDropdownMenuvisible: false,
      isShopDropdownMenuvisible: false,
    }
  },

  methods: {
    getImagePath: function (imgPath) {
      return new URL(imgPath, import.meta.url).href;
    },

    dropdownToggler(menuItem) {
      let myThis = this;
      if (menuItem = "events") {
        if (this.isDropdownMenuvisible) {
          myThis.isEventsDropdownMenuvisible = false;
        } else {
          myThis.isEventsDropdownMenuvisible = true;
        }
      }
      if (menuItem = "shop") {
        if (this.isDropdownMenuvisible) {
          myThis.isShopDropdownMenuvisible = false;
        } else {
          myThis.isShopDropdownMenuvisible = true;
        }
      }
    }
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

          <li v-for="menuItem, index in menuList"
            @click="(menuItem === 'events' || menuItem === 'shop') ? dropdownToggler(menuItem) : ''">
            {{ menuItem }}

            <i v-if="menuItem === 'events' || menuItem === 'shop'" class="fa-solid fa-angle-down"></i>

            <div v-if="menuItem === 'events'" class="customDropdownMenu"
              :class="isEventsDropdownMenuvisible === true ? 'customShower' : 'd-none'" :key="index">
              <ul>
                <li>Customizable Content</li>
                <li>Customizable Content</li>
              </ul>
            </div>
            <div v-if="menuItem === 'shop'" class="customDropdownMenu"
              :class="isShopDropdownMenuvisible === true ? 'customShower' : 'd-none'" :key="index">
              <ul>
                <li>Customizable Content</li>
                <li>Customizable Content</li>
              </ul>
            </div>
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
      position: relative;

      &:hover {
        color: $brandOrange;
      }
    }
  }

  div.customDropdownMenu {
    position: absolute;
    border-radius: 1rem;
    top: 45px;
    right: 0;
    z-index: 3;
    background-color: $brandBlack;
    color: $brandWhite;

    li {
      margin: 0.5rem 0;
    }

    .customShower {
      display: block !important;
    }
  }
}
</style>

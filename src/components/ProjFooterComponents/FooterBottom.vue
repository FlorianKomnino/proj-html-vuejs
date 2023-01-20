<script>
import ListCard from '../CardsComponents/ListCard.vue';

export default {
  name: 'FooterBottom',

  props: {
  },

  components: {
    ListCard,
  },

  data() {
    return {
      listsProps: [
        {
          listTitle: "bookings",
          listItemsArray: ["502 new design str, melbbourne, san francisco, CA 94110, united states of america australia", "t:1123-456-789", "email:"],
        },
        {
          listTitle: "music business worldwide",
          listItemsArray: ["502 new design str, melbbourne, san francisco, CA 94110, united states of america australia"],
        },
        {
          listTitle: "giveaways rock to all",
          listItemsArray: ["502 new design str, melbbourne, san francisco, CA 94110, united states of america australia"],
        },
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
  <section>
    <div class="listsCards col-10 d-flex flex-wrap">
      <article>
        <ListCard :listTitle="listsProps[0].listTitle" :listItemsArray="listsProps[0].listItemsArray" />
      </article>
      <article>
        <ListCard :listTitle="listsProps[1].listTitle" :listItemsArray="listsProps[1].listItemsArray" />
      </article>
      <article>
        <ListCard :listTitle="listsProps[2].listTitle" :listItemsArray="listsProps[2].listItemsArray" />
      </article>
    </div>
  </section>


</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables" as *;
@use "../../../node_modules/bootstrap" as *;

section {
  background-color: $brandBlack;
  width: 100vw;
  text-align: center;
  padding: 90px;
}

.listsCards {
  text-align: center;
  justify-content: space-between;
  margin: 0 auto;

  article {
    height: 330px;
    width: calc((100% / 3) - 1.5rem);
    margin: 1rem 0 4rem 0;
    text-align: left;
    color: $brandWhite;
  }
}
</style>

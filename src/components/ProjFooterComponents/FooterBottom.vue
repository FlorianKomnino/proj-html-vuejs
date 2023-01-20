<script>
import ListCard from '../CardsComponents/ListCard.vue';
import ProjButton from '../ProjButton.vue';
import FormCard from '../CardsComponents/FormCard.vue';

export default {
  name: 'FooterBottom',

  props: {
  },

  components: {
    ListCard,
    ProjButton,
    FormCard,
  },

  data() {
    return {
      listsProps: [
        {
          listTitle: "bookings",
          listItemsArray: ["502 new design str, melbbourne, san francisco, CA 94110, united states of america australia", "t:1123-456-789", "email:"],
        },
        {
          listTitle: "information",
          listItemsArray: ["product support", "checkout", "report abuse", "redeem voucher", "order status"],
        },
        {
          listTitle: "support",
          listItemsArray: ["policies & rules", "privacy policy", "license policy", "my account", "locality"],
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
      <article>
        <FormCard />
      </article>
    </div>

  </section>


</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables" as *;
@use "../../../node_modules/bootstrap" as *;

section {
  text-transform: capitalize;
  background-color: $brandBlack;
  width: 100vw;
  text-align: center;
  padding: 40px 40px 20px 40px;
}

.listsCards {
  text-align: center;
  justify-content: space-between;
  margin: 0 auto;

  article {
    height: 330px;
    width: calc((100% / 4) - 1.5rem);
    margin: 1rem 0;
    text-align: left;
    color: $brandWhite;

  }
}
</style>

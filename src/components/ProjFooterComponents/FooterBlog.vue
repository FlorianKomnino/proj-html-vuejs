<script>
import StreamCard from '../CardsComponents/StreamCard.vue';

export default {
  name: 'FooterBlog',

  props: {
  },

  components: {
    StreamCard,
  },

  data() {
    return {
      cardsTitles: [
        "a roll and bang the floor",
        "your melody to our music",
        "touching heaven on frequency",
        "misic makes stronge beats",
        "sound is the spark of time",
        "make your night groovy",
      ],
      cardsImgsList: [
        "../assets/gallery1.jpg",
        "../assets/gallery2.jpg",
        "../assets/gallery3.jpg",
        "../assets/gallery4.jpg",
        "../assets/gallery5.jpg",
        "../assets/gallery6.jpg",
      ]
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
    <h3>
      who we are
    </h3>
    <h1>
      sense the jazz
    </h1>

    <div class="streamsCards col-10 d-flex flex-wrap">
      <article>
        <StreamCard :titleText="cardsTitles[0]" :imgPath="cardsImgsList[0]" />
      </article>
      <article>
        <StreamCard :titleText="cardsTitles[1]" :imgPath="cardsImgsList[1]" />
      </article>
      <article>
        <StreamCard :titleText="cardsTitles[2]" :imgPath="cardsImgsList[2]" />
      </article>
      <article>
        <StreamCard :titleText="cardsTitles[3]" :imgPath="cardsImgsList[3]" />
      </article>
      <article>
        <StreamCard :titleText="cardsTitles[4]" :imgPath="cardsImgsList[4]" />
      </article>
      <article>
        <StreamCard :titleText="cardsTitles[5]" :imgPath="cardsImgsList[5]" />
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

  h3 {
    font-size: 0.7rem;
    color: $brandOrange;
    text-transform: uppercase;
    transform: scaleX(1.25);

  }

  h1 {
    color: $brandWhite;
    text-transform: uppercase;
    font-weight: 600;
    transform: scaleY(1.4);
  }
}

.streamsCards {
  text-align: center;
  justify-content: space-between;
  margin: 0 auto;

  article {
    height: 330px;
    width: calc((100% / 3) - 1.5rem);
    margin: 1rem 0 4rem 0;
  }
}
</style>

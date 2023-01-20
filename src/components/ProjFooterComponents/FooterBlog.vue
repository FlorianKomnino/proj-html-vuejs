<script>
import BlogCard from '../CardsComponents/BlogCard.vue';

export default {
  name: 'FooterBlog',

  props: {
  },

  components: {
    BlogCard,
  },

  data() {
    return {
      postsProps: [
        {
          postImgPath: "../../assets/hip_hop_wired_to_dance_make.jpg",
          postTitle: "hip hop wired to dance make",
          postDate: "06 november 2021",
          postTeaserContent: "Driving short distances music is a music genre that includes traditional folk music and the contemporary genre that evolved from the former"
        },
        {
          postImgPath: "../../assets/music_business-worldwide.jpg",
          postTitle: "music business worldwide",
          postDate: "27 may 2022",
          postTeaserContent: "accelerate work and drive productivity the beatles' experimentation and creative freedom led other bands to experiment in various ways as well."
        },
        {
          postImgPath: "../../assets/giveaways_rock.jpg",
          postTitle: "giveaways rock to all",
          postDate: "07 may 2022",
          postTeaserContent: "signs your car battery has to be replaced when the dashboard lights start flashing, this is a sign the battery is dying. several issues arise and"
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
    <h3>
      music blog
    </h3>
    <h1>
      best music blog
    </h1>

    <div class="streamsCards col-10 d-flex flex-wrap">
      <article>
        <BlogCard :titleText="postsProps[0].postTitle" :imgPath="postsProps[0].postImgPath"
          :postDate="postsProps[0].postDate" :postTeaser="postsProps[0].postTeaserContent" />
      </article>
      <article>
        <BlogCard :titleText="postsProps[1].postTitle" :imgPath="postsProps[1].postImgPath"
          :postDate="postsProps[1].postDate" :postTeaser="postsProps[1].postTeaserContent" />
      </article>
      <article>
        <BlogCard :titleText="postsProps[2].postTitle" :imgPath="postsProps[2].postImgPath"
          :postDate="postsProps[2].postDate" :postTeaser="postsProps[2].postTeaserContent" />
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

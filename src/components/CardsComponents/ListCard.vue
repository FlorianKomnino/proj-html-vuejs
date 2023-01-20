<script>

export default {
    name: 'ListCard',

    props: {
        listItemsArray: Array,
        listTitle: String,
        socialIcons: Boolean,
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

        <h4>
            {{ listTitle }}
        </h4>
        <ul>
            <li v-for="listItem in listItemsArray">{{ listItem }}</li>
            <li v-if="socialIcons">
                <i class="fa-brands fa-instagram"></i>
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-twitter"></i>
                <i class="fa-brands fa-youtube"></i>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables" as *;

.cardWrapper {
    color: $brandWhite;
    height: 100%;
    width: 100%;
    padding: 3rem;

    h4 {
        margin-top: 20px;
        padding-bottom: 1rem;
        text-transform: uppercase;
        transform: scaleY(1.25);
    }

    p {
        margin-top: 10px;
        font-size: 0.75rem;
        line-height: 1.2rem;
        font-weight: 300;
        text-transform: capitalize;
    }

    li {
        list-style-type: none;
        padding: 0.5rem 0;
    }
}
</style>

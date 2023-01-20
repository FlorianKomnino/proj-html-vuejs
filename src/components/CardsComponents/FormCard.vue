<script>
import ProjButton from '../ProjButton.vue';

export default {
    name: 'FormCard',

    components: {
        ProjButton,
    },

    props: {
        listTitle: String,
    },

    data() {
        return {

        }
    },

    methods: {

    }
}
</script>

<template>
    <div class="cardWrapper">
        <h4>
            {{ listTitle }}
        </h4>
        <article>
            <h4>
                newsletter
            </h4>
            <input type="text" class="eMailField" placeholder="Email">
            <input type="text" class="messageField" placeholder="Message">
            <ProjButton :textOnTheButton="`send message`" class="customFormButton" />
        </article>
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
        padding-bottom: 1rem;
        text-transform: uppercase;
        transform: scaleY(1.25);
    }

    input {
        margin: 1rem 0;
        padding: 0.4rem;
        width: 220px;
        background-color: $brandBlack;
        border: 3px solid $alternativeBlack;
    }

    input.messageField {
        height: 75px;
    }
}

.customFormButton {
    text-transform: uppercase;
}
</style>

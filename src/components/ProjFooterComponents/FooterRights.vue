<script>
export default {
  name: 'FooterRights',

  props: {
  },

  components: {
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
  <section>
    <p>
      &copy; 2023 all rights reserved. developed by TemplateMela
    </p>

  </section>


</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables" as *;
@use "../../../node_modules/bootstrap" as *;

section {
  border-top: 4px solid $alternativeBlack;
  text-transform: capitalize;
  background-color: $brandBlack;
  color: $brandWhite;
  font-size: 0.8rem;
  width: 100vw;
  text-align: center;
  padding: 20px 0;
}
</style>

<script>
import ProjHeader from './components/ProjHeader.vue';

export default {

  components: {
    ProjHeader,
  }
}
</script>

<template>
  <div id="projHeaderWrapper">
    <ProjHeader />
  </div>
</template>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#projHeaderWrapper {
  max-width: 100vw !important;
  overflow-x: hidden;
}
</style>

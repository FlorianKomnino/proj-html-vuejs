<script>
import ProjHeader from './components/ProjHeader.vue';

export default {

  components: {
    ProjHeader,
  }
}
</script>

<template>
  <div class="projHeaderWrapper">
    <ProjHeader />
  </div>
</template>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.projHeaderWrapper {
  width: 100vw;
  overflow-x: hidden;
}
</style>

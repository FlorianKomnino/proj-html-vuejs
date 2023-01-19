<script>
import ProjHeader from './components/ProjHeader.vue';

export default {

  components: {
    ProjHeader,
  }
}
</script>

<template>
  <div id="projHeaderWrapper" class="container-fluid">
    <div class="row">
      <div class="col">
        <ProjHeader />
      </div>
    </div>
  </div>
</template>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#projHeaderWrapper {
  overflow-x: hidden;
}
</style>

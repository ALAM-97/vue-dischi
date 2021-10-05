<template>
  <div id="app">
    <Header  @filter="albumsFiltered"/>
    <Albums :filt="genreSelected"/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Albums from './components/Albums.vue'

export default {
  name: 'App',
  data() {
    return {
      genreSelected: "",
    }
  },
  components: {
    Header,
    Albums
  },
  methods: {
    albumsFiltered(genre) {
          this.genreSelected = genre;
        }
  }
}
</script>

<style lang="scss">
    @import './style/common.scss';

    #app {
      background-color: $bodyBg;
    }
</style>

<script>
export default {
  name: "ComicItem",

  data() {
    return {

    }
  },

  props: {
    thumb: String,
    title: String,
  }
}
</script>

<template>
  <div class="comic">
    <img class="comic-cover" :src="thumb" alt="comic cover">
    <div class="comic-title">{{ title }}</div>
  </div>
</template>

<style lang="scss" scoped>
  .comic {
    width: calc(100% / 6 - 10px / 6 * 5);


    .comic-cover {
      width: 100%;

      // questa proprietà permette di dare la dimensione ad un elemento in base al rapporto che indichiamo
      // il rapporto 1/1 rappresenta un quadrato
      aspect-ratio: 1/1;

      object-fit: cover;
      object-position: top;
      
    }

    .comic-title {
      text-transform: uppercase;
    }

  }
</style>
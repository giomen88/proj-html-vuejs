<template>
  <div class="card border-0 rounded-0 m-3">
    <BaseImage :imageSrc="imageSrc" :imageAlt="imageAlt" />
    <div class="text p-3">
      <h3>{{ cardTitle }}</h3>
      <time>{{ cardTime }}</time>
    </div>
  </div>
</template>

<script>
import BaseImage from "./BaseImage.vue";

export default {
  name: "BaseCard",

  components: { BaseImage },

  props: {
    imageSrc: String,
    imageAlt: String,
    cardTitle: String,
    cardTime: String,
  },
};
</script>

<style lang="scss" scoped>
</style>

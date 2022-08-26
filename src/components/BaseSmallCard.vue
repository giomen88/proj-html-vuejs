<template>
  <div class="card small-card border-0">
    <BaseImage :imageSrc="imageSrc" :imageAlt="imageAlt" />
    <button class="bg-white border-0 text-dark pb-3">{{ textButton }}</button>
  </div>
</template>

<script>
import BaseImage from "./BaseImage.vue";
export default {
  name: "BaseSmallCard",

  components: {
    BaseImage,
  },

  props: {
    imageSrc: String,
    imageAlt: String,
    textButton: String,
  },
};
</script>

<style lang="scss" scoped>
.small-card:hover button {
  background-color: var(--primarycolor);
}
</style>
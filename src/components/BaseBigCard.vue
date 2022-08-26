<template>
  <div class="card border-0">
    <BaseImage :imageSrc="imageSrc" :imageAlt="imageAlt" />
    <div class="text d-flex flex-column justify-content-between p-3">
      <h3>{{ cardTitle }}</h3>
      <p class="subtitle">{{ cardSubtitle }}</p>
      <div class="line my-3"></div>
      <p class="description">{{ cardDescription }}</p>
      <a class="button">{{ textButton }}</a>
    </div>
  </div>
</template>

<script>
import BaseImage from "./BaseImage.vue";
export default {
  name: "BaseBigCard",

  components: { BaseImage },

  props: {
    imageSrc: String,
    imageAlt: String,
    cardTitle: String,
    cardSubtitle: String,
    cardDescription: String,
    textButton: String,
  },
};
</script>

<style lang="scss" scoped>
.subtitle {
  font-size: 0.8rem;
  color: var(--primary-textcolor);
}
.description {
  color: var(--primary-textcolor);
}
.button {
  background-color: var(--primarycolor);
  color: #fff;
  padding: 10px 10px;
}
</style>

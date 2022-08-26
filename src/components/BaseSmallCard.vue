<template>
  <div
    class="
      card
      small-card
      border-0
      rounded-0
      d-flex
      flex-column
      align-items-center
    "
  >
    <img :src="imageSrc" :alt="imageAlt" class="img-fluid w-50" role="button" />
    <button class="bg-white border-0 text-dark pb-3">{{ textButton }}</button>
  </div>
</template>

<script>
export default {
  name: "BaseSmallCard",

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
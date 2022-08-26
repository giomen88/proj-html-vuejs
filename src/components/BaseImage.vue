<template>
  <figure class="position-relative text-center">
    <img :src="imageSrc" :alt="imageAlt" class="img-fluid" role="button" />
    <div class="hover"><i class="fa-solid fa-link"></i></div>
  </figure>
</template>

<script>
export default {
  name: "BaseImage",

  props: {
    imageSrc: String,
    imageAlt: String,
  },
};
</script>

<style lang="scss" scoped>
.hover {
  display: none;
}
img:hover .hover {
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-image: linear-gradient(#147464 #20ad96);
  opacity: 0.5;
}
</style>
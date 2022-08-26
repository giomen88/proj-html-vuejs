<template>
  <div id="app">
    <div class="container-fluid">
      <TheHeader />

      <main>
        <TheBanner />

        <section id="popular-recipes" class="mt-5">
          <div class="container">
            <div class="row">
              <div class="col-6 offset-3 title text-center my-5">
                <h2 class="fs-5 mb-3">POPULAR RECIPES</h2>
                <p>
                  Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                  Atque, nostrum animi dolorem nisi sequi eos at nam
                  voluptatibus esse.
                </p>
              </div>
              <div class="col-6 current-recipe">
                <BaseBigCard
                  :imageSrc="
                    require('./assets/img/recipes/Yogurt-Nan-1200x790.jpg')
                  "
                  cardTitle="Launch Favourite with Salad, Naan and Beans"
                  cardSubtitle="Bakery, Featured, Healty, Latest Recipes, Staff Picks"
                  cardDescription="Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis molestias aspernatur similique, illum, voluptate impedit pariatur atque dolor quidem quis incidunt asperiores, molestiae necessitatibus tenetur suscipit nemo at nesciunt. Esse."
                  textButton="LEARN MORE"
                />
              </div>
              <div
                class="
                  col-6
                  recipes-list
                  d-flex
                  justify-content-between
                  flex-wrap
                "
              >
                <BaseImage
                  v-for="recipe in recipes"
                  :key="recipe.id"
                  class="recipe-img"
                  :imageSrc="recipe.img"
                />
              </div>
            </div>
          </div>
        </section>
      </main>

      <TheFooter />
    </div>
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import TheBanner from "./components/TheBanner.vue";
import TheFooter from "./components/TheFooter.vue";
import BaseImage from "./components/BaseImage.vue";
import BaseBigCard from "./components/BaseBigCard.vue";

export default {
  name: "App",
  components: { TheHeader, TheBanner, TheFooter, BaseImage, BaseBigCard },

  data() {
    return {
      recipes: [
        {
          img: require("./assets/img/recipes/Mixed-fruits.jpg"),
          title: "",
          text: "",
          id: "1",
        },
        {
          img: require("./assets/img/recipes/r-rachel-park-366508-unsplash-min.jpg"),
          title: "",
          text: "",
          id: "2",
        },
        {
          img: require("./assets/img/recipes/r-michelle-tsang-500721-unsplash-min.jpg"),
          title: "",
          text: "",
          id: "3",
        },
        {
          img: require("./assets/img/recipes/quick-summer-drink-460x295.jpg"),
          title: "",
          text: "",
          id: "4",
        },
        {
          img: require("./assets/img/recipes/r-maarten-van-den-heuvel-400626-unsplash-min-460x295.jpg"),
          title: "",
          text: "",
          id: "5",
        },
        {
          img: require("./assets/img/recipes/perfect-cosmopolitan-460x295.jpg"),
          title: "",
          text: "",
          id: "6",
        },
        {
          img: require("./assets/img/recipes/fi2x-6-460x295.jpg"),
          title: "",
          text: "",
          id: "7",
        },
        {
          img: require("./assets/img/recipes/r-brooke-lark-96398-unsplash-min-460x295.jpg"),
          title: "",
          text: "",
          id: "8",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./assets/sass/style.scss";
#app {
  background-color: var(--bgcolor);
}
#popular-recipes .title p {
  color: var(--primary-textcolor);
}
.recipes-list {
  margin-top: -10px;
  .recipe-img {
    flex-basis: calc(50% - 20px);
    margin: 10px;
  }
}
</style>

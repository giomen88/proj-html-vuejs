<template>
  <div id="app">
    <div class="container-fluid">
      <TheHeader />

      <main>
        <!-- banner -->
        <TheBanner />

        <!-- popular-recipes section -->
        <section id="popular-recipes" class="mt-5">
          <div class="container">
            <div class="row">
              <div class="col-6 offset-3 text-center my-5">
                <h2 class="fs-5 mb-3">POPULAR RECIPES</h2>
                <p class="subtitle">
                  Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                  Atque, nostrum animi dolorem nisi sequi eos at nam
                  voluptatibus esse.
                </p>
              </div>
              <!-- current-recipe -->
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
              <!-- recipes-list -->
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

        <!-- culinary-collection section -->
        <section id="culinary-collection" class="mt-5">
          <div class="container">
            <div class="row">
              <div class="col-6 offset-3 text-center my-5">
                <h2 class="fs-5 mb-3">CULINARY COLLECTION</h2>
                <p class="subtitle">
                  Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                  Atque, nostrum animi dolorem nisi sequi eos at nam
                  voluptatibus esse.
                </p>
              </div>
              <div class="col-12 d-flex justify-content-between flex-wrap">
                <!-- cards -->
                <BaseSmallCard
                  class="collection-img"
                  v-for="item in collection"
                  :key="item.id"
                  :imageSrc="item.img"
                  :imageAlt="item.label"
                  :textButton="item.label"
                />
              </div>
            </div>
          </div>
        </section>

        <!-- subscribe section -->
        <section id="subscribe" class="mt-5 p-5">
          <div class="container">
            <div class="row">
              <div
                class="
                  col-6
                  offset-3
                  d-flex
                  flex-column
                  justify-content-center
                  align-items-center
                "
              >
                <h2>Subscribe & Receive a free book</h2>
                <p class="subtitle">
                  Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                </p>
                <div class="form d-flex mb-3">
                  <input
                    type="email"
                    class="form-control me-3"
                    placeholder="Inserisci la tua email"
                  />

                  <a
                    class="
                      button
                      w-50
                      rounded-1
                      text-center text-white
                      py-2
                      px-2
                    "
                    role="button"
                    >SUBSCRIBE</a
                  >
                </div>
                <span
                  >Lorem ipsum dolor, sit amet consectetur adipisicing
                  elit.</span
                >
              </div>
            </div>
          </div>
        </section>
      </main>

      <!-- footer -->
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
import BaseSmallCard from "./components/BaseSmallCard.vue";

export default {
  name: "App",
  components: {
    TheHeader,
    TheBanner,
    TheFooter,
    BaseImage,
    BaseBigCard,
    BaseSmallCard,
  },

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

      collection: [
        {
          img: require("./assets/img/collection/drinks-recipes.png"),
          label: "DRINKS",
          id: "1",
        },
        {
          img: require("./assets/img/collection/soups-recipes.png"),
          label: "SOUPS",
          id: "2",
        },
        {
          img: require("./assets/img/collection/baking-recipes.png"),
          label: "BAKERY",
          id: "3",
        },
        {
          img: require("./assets/img/collection/dinner-recipes.png"),
          label: "DINNER",
          id: "4",
        },
        {
          img: require("./assets/img/collection/healthy-recipes.png"),
          label: "HEALTY",
          id: "5",
        },
        {
          img: require("./assets/img/collection/staff-picks.png"),
          label: "STAFF PICKS",
          id: "6",
        },
        {
          img: require("./assets/img/collection/premium-recipes.png"),
          label: "APPETISERS",
          id: "7",
        },
        {
          img: require("./assets/img/collection/quick-easy-recipes.png"),
          label: "QUICK & EASY",
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
// popular recipes
.recipes-list {
  margin-top: -10px;

  .recipe-img {
    flex-basis: calc(50% - 20px);
    margin: 10px;
    box-shadow: 0 5px 10px lightgray;
  }

  // culinary collection
}
.collection-img {
  flex-basis: calc(25% - 40px);
  margin: 20px;
}

// subscribe
#subscribe {
  height: 300px;
  background-image: url(./assets/img/subscribe-sec-bg.png);
  background-size: cover;

  h2 {
    font-family: "Domine", serif;
  }

  span {
    color: var(--primary-textcolor);
    font-size: 0.8rem;
  }
}
</style>

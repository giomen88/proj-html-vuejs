<template>
  <div id="app">
    <div class="container-fluid">
      <TheHeader />

      <div class="jumbotron">
        <div class="container h-100">
          <div class="row h-100 justify-content-center align-items-center">
            <div
              class="
                col-6
                pick
                d-flex
                flex-column
                justify-content-center
                align-items-center
                text-center
                position-relative
              "
            >
              <h1>Food Corner: Top Japanese Restaurant for Sushi</h1>
              <time>March 25, 2019</time>
              <label>TODAY'S PICK</label>
            </div>
          </div>
        </div>
      </div>

      <main class="position-relative">
        <div class="container">
          <banner id="foodie-journal">
            <div class="title">
              <div></div>
              <h2>FOODIE JOURNAL</h2>
              <div></div>
            </div>
            <div class="row">
              <div class="col-4"><SmallBaseCard /></div>
              <div class="col-4"><SmallBaseCard /></div>
              <div class="col-4"><SmallBaseCard /></div>
            </div>
          </banner>
        </div>
      </main>

      <TheFooter />
    </div>
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";

export default {
  name: "App",
  components: { TheHeader, TheFooter },
};
</script>

<style lang="scss">
@import "./assets/sass/style.scss";
#app {
  background-color: #f6f7f1;

  .jumbotron {
    height: 500px;
    background-image: url(./assets/img/single-post-img3.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center center;

    .pick {
      height: 200px;
      background-color: #fff;
      border-radius: 10px;

      label {
        padding: 5px 10px;
        background-color: #fc7525;
        color: #fff;
        font-size: 0.8rem;
        border-radius: 5px;
        position: absolute;
        top: 0;
        right: 50%;
        transform: translate(50%, -50%);
      }
    }
  }

  #foodie-journal {
    background-color: #fff;
    position: absolute;
    top: -10%;
    right: 50%;
  }
}
</style>

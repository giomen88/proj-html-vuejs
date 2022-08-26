<template>
  <header>
    <div class="container">
      <!-- header-top -->
      <div class="header-top py-2">
        <div class="row">
          <div class="col-6 text-start">
            <ul>
              <li>
                <a href="">Dowload App <label role="button">iOS</label></a>
              </li>
              <li><a href="">Advertise with us</a></li>
            </ul>
          </div>
          <div class="col-6">
            <ul class="justify-content-end">
              <li>
                <a href=""><i class="fa-brands fa-instagram"></i></a>
              </li>
              <li>
                <a href=""><i class="fa-brands fa-twitter"></i></a>
              </li>
              <li>
                <a href=""><i class="fa-brands fa-youtube"></i></a>
              </li>
              <li>
                <a href=""><i class="fa-brands fa-facebook-f"></i></a>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <!-- header-bottom -->
      <div class="header-bottom py-3">
        <div class="row justify-content-center">
          <div class="col-12 text-center">
            <img
              src="../assets/img/logo/avada-food-logo.png"
              alt="avada-food-logo"
              class="logo img-fluid"
            />
          </div>
          <div class="col-6 links pt-4 text-center">
            <ul class="justify-content-between p-0">
              <li><a href="">Home</a></li>
              <li><a href="">Recipes</a></li>
              <li><a href="">Places</a></li>
              <li><a href="">Blog</a></li>
              <li><a href="">About</a></li>
              <li><a href="">Contact</a></li>
              <li>
                <a href=""><i class="fa-solid fa-magnifying-glass"></i></a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>

    <!-- jumbotron -->
    <div id="jumbotron">
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
  </header>
</template>

<script>
export default {
  name: "TheHeader",
  components: {},
};
</script>

<style lang="scss" scoped>
header {
  background-color: #fff;

  a {
    color: var(--secondary-textcolor);
    margin: 0 10px;
  }
  .header-top label {
    background-color: var(--primarycolor);
    color: #fff;
    border-radius: 5px;
    padding: 0 10px;
    font-size: 0.8rem;
  }

  .header-bottom a {
    color: #000;

    &:hover {
      color: var(--primarycolor);
    }
  }

  #jumbotron {
    height: 550px;
    background-image: url(../assets/img/images/single-post-img3.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center center;

    h1 {
      font-family: "Domine", serif;
    }

    .pick {
      height: 200px;
      background-color: #fff;
      border-radius: 10px;

      label {
        padding: 5px 10px;
        background-color: var(--primarycolor);
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
}
</style>

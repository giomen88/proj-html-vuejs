<template>
  <footer class="mt-0">
    <!-- footer-top -->
    <div class="footer-top d-flex">
      <img src="../assets/img/recipes/Yogurt-Nan-1200x790.jpg" alt="" />
      <img src="../assets/img/recipes/Mixed-fruits.jpg" alt="" />
      <img
        src="../assets/img/recipes/r-rachel-park-366508-unsplash-min.jpg"
        alt=""
      />
      <img
        src="../assets/img/recipes/r-michelle-tsang-500721-unsplash-min.jpg"
        alt=""
      />
    </div>
    <!-- footer-nav -->
    <div class="footer-nav p-5 position-relative">
      <div class="container">
        <div class="row">
          <div class="col-6 offset-3">
            <div class="row">
              <div class="col-3 d-flex flex-column justify-content-between">
                <a href="" class="mb-4"
                  ><img
                    src="../assets/img/logo/avada-food-logo-mob.png"
                    alt=""
                    class="img-fluid"
                /></a>
                <ul class="social-links">
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
              <div class="col-3">
                <ul class="links d-flex flex-column justify-content-start">
                  <li><a href="">Home</a></li>
                  <li><a href="">Recipes</a></li>
                  <li><a href="">Places</a></li>
                  <li><a href="">Blog</a></li>
                  <li><a href="">About</a></li>
                  <li><a href="">Contact</a></li>
                </ul>
              </div>
              <div
                class="col-3 contact d-flex flex-column justify-content-start"
              >
                <h6>CONTACT</h6>
                <a href="" class="address"
                  ><i class="fa-solid fa-location-dot">
                    775 New York Ave, Brooklyn, Kings, New York 11203</i
                  ></a
                >
                <a href="" class="phone-number"
                  ><i class="fa-solid fa-phone-flip"> + 0100-505-0000</i></a
                >
                <a href="" class="email"
                  ><i class="fa-solid fa-envelope"> info@your-domain.com</i></a
                >
              </div>
              <div
                class="
                  col-3
                  get-app
                  d-flex
                  flex-column
                  justify-content-between
                  border-0
                "
              >
                <h6>GET OUR APP!</h6>
                <a href=""
                  ><img
                    src="../assets/img/download-android.png"
                    alt=""
                    class="img-fluid"
                /></a>
                <a href=""
                  ><img
                    src="../assets/img/download-app-store.png"
                    alt=""
                    class="img-fluid"
                /></a>
              </div>
            </div>
          </div>
        </div>
        <div class="go-up position-absolute">
          <a class="text-dark" href="#jumbotron"
            ><i class="fa-solid fa-circle-chevron-up fa-3x"></i
          ></a>
        </div>
      </div>
    </div>
    <!-- footer-bottom -->
    <div class="footer-bottom p-4 text-center">
      <i class="fa-solid fa-copyright"></i>Copyright 2012 - 2020 | Avada Theme
      by ThemeFusion | All Rights Reserved | Powered by WordPress
    </div>
  </footer>
</template>

<script>
export default {
  name: "TheFooter",
  components: {},
};
</script>

<style lang="scss" scoped>
footer {
  background-color: #fff;
  font-size: 0.8rem;

  .footer-top {
    height: 250px;
    & img {
      flex-basis: 25%;
    }
  }

  .footer-nav div[class*="col"] {
    border-right: 0.5px dashed var(--secondary-textcolor);
  }

  .links a {
    color: #000;
  }

  .contact a {
    color: var(--secondary-textcolor);
  }

  .social-links a {
    color: var(--secondary-textcolor);
    margin: 0 5px;
  }

  .footer-nav h6 {
    color: var(--primarycolor);
  }

  .footer-bottom {
    background-color: var(--bgcolor);
    color: var(--primary-textcolor);
    font-size: 0.6rem;
  }

  .go-up {
    bottom: 20px;
    left: 20px;
    text-shadow: 0 3px 5px gray;
  }
}
</style>

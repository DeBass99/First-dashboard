<template>
  <div>
    <div class="app fixed-top">
      <b-navbar toggleable="lg" type="dark" variant="info" class="nav">
        <b-navbar-brand to="/" class="brand">
          <img src="~/assets/logo.png" alt="logo"
        /></b-navbar-brand>

        <b-navbar-toggle target="nav-collapse">
          <img src="~/assets/menu toggle.png" alt="" />
        </b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-col md="12">
            <div class="nav-one">
              <div class="pages">
                <b-nav-item
                  ><nuxt-link to="/" class="data">
                    <span class="link" @click="first">
                      <svg
                        class="one"
                        width="19"
                        height="25"
                        viewBox="0 0 19 25"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M9.09091 3.40909V0L4.54546 4.54545L9.09091 9.09091V5.68182C12.858 5.68182 15.9091 8.73295 15.9091 12.5C15.9091 13.6534 15.6193 14.733 15.1193 15.6875L16.7784 17.3466C17.6591 15.9375 18.1818 14.2841 18.1818 12.5C18.1818 7.47727 14.1136 3.40909 9.09091 3.40909ZM9.09091 19.3182C5.32386 19.3182 2.27273 16.267 2.27273 12.5C2.27273 11.3466 2.5625 10.267 3.0625 9.3125L1.40341 7.65341C0.522728 9.0625 0 10.7159 0 12.5C0 17.5227 4.06818 21.5909 9.09091 21.5909V25L13.6364 20.4545L9.09091 15.9091V19.3182Z"
                          fill="#000AFF"
                        />
                      </svg>
                      Data Analysis
                    </span>
                  </nuxt-link></b-nav-item
                >

                <b-nav-item>
                  <nuxt-link to="/transactions" class="transactions">
                    <span class="link" @click="second">
                      <svg
                        class="two"
                        width="25"
                        height="27"
                        viewBox="0 0 25 27"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M24.21 20.5855V18.1636H7.263V3.63273H9.684L6.0525 0L2.421 3.63273H4.842V6.05454H0V8.47636H4.842V18.1636C4.842 19.4956 5.93145 20.5855 7.263 20.5855H16.947V23.0073H14.526L18.1575 26.64L21.789 23.0073H19.368V20.5855H24.21ZM9.684 8.47636H16.947V15.7418H19.368V8.47636C19.368 7.14436 18.2785 6.05454 16.947 6.05454H9.684V8.47636Z"
                          fill="#000AFF"
                        />
                      </svg>
                      Transactions
                    </span>
                  </nuxt-link></b-nav-item
                >

                <b-nav-item>
                  <nuxt-link to="/settings" class="settings">
                    <span class="link move" @click="third">
                      <svg
                        class="three"
                        width="22"
                        height="22"
                        viewBox="0 0 22 22"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M0 16.9478V19.3689H7.26333V16.9478H0ZM0 2.42111V4.84222H12.1056V2.42111H0ZM12.1056 21.79V19.3689H21.79V16.9478H12.1056V14.5267H9.68444V21.79H12.1056ZM4.84222 7.26333V9.68444H0V12.1056H4.84222V14.5267H7.26333V7.26333H4.84222ZM21.79 12.1056V9.68444H9.68444V12.1056H21.79ZM14.5267 7.26333H16.9478V4.84222H21.79V2.42111H16.9478V0H14.5267V7.26333Z"
                          fill="#000AFF"
                        />
                      </svg>
                      Settings
                    </span>
                  </nuxt-link></b-nav-item
                >
              </div>

              <div class="buttons">
                <button class="week">week 1</button>
                <p>to</p>
                <button class="week">week 4</button>

                <button class="arrow">
                  <img src="~/assets/arrow left.png" alt="" />
                </button>
                <button class="arrow">
                  <img src="~/assets/arrow right.png" alt="" />
                </button>
              </div>

              <div class="profile">
                <div class="name">
                  <p>Destine Okono</p>
                </div>

                <div class="image">
                  <img src="~/assets/profile picture.png" alt="" />
                </div>
              </div>
            </div>
          </b-col>
        </b-collapse>
      </b-navbar>
    </div>
  </div>
</template>

<script>
import $ from "jquery";

export default {
  data() {
    return {};
  },

  mounted() {
    $(".one").removeClass("one-path");
    $(".two").addClass("two-path");
    $(".three").addClass("three-path");
  },

  methods: {
    first() {
      $(".one-path").removeClass("one-path");
      $(".two").addClass("two-path");
      $(".three").addClass("three-path");
    },

    second() {
      $(".two").removeClass("two-path");
      $(".one").addClass("one-path");
      $(".three").addClass("three-path");
    },

    third() {
      $(".three").removeClass("three-path");
      $(".one").addClass("one-path");
      $(".two").addClass("two-path");
    },
  },
};
</script>

<style scoped>
.nav {
  padding-top: 15px;
  background-color: #fff !important;
}

.nav-one {
  display: flex;
  justify-content: space-between;
}

a {
  font-style: normal;
  font-weight: 500;
  font-size: 13px;
  color: #3f404a;
  text-decoration: none;
}
a.nav-link {
  padding: 0px;
}

a.nuxt-link-exact-active {
  font-style: normal;
  font-weight: 700;
  font-size: 13px;
  padding-bottom: 10px;
}

span:nth-child(-n + 2) {
  margin-right: 50px;
}

.move::after {
  margin-left: -80px;
}

.one-path {
  filter: grayscale(1) invert(0.7);
}

.two-path {
  filter: grayscale(1) invert(0.7);
}

.three-path {
  filter: grayscale(1) invert(0.7);
}

.buttons {
  display: flex;
  margin-left: 386px;
}

.buttons button {
  width: 80px;
  height: 39px;
  background: #f3f4f9;
  border-radius: 4px;
  font-style: normal;
  font-weight: 500;
  font-size: 13px;
  border: none;
  margin-top: -5px;
}

.buttons p {
  margin: 0px 18px;
}

button.arrow {
  width: 30px;
  height: 39px;
  background: #f3f4f9;
  border-radius: 4px;
  margin-left: 5px;
}

.profile {
  display: flex;
  margin-left: 88px;
}

.profile p {
  font-style: normal;
  font-weight: 500;
  font-size: 13px;
}

.profile img {
  margin-left: 15px;
  margin-top: -5px;
}

.pages {
  margin-left: 80px;
  display: flex;
}

@media only screen and (max-width: 600px) {
  .app {
    background-color: #fff;
    list-style: none;
  }

  .nav-one {
    flex-direction: column;
  }
  .pages {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    padding: 0px;
    margin: 0px;
  }

  a {
    border: none;
    margin: 10px 0px;
  }

  a:hover {
    border: none;
  }

  .buttons {
    display: none;
  }

  .profile {
    margin-top: 30px;
    display: flex;
    text-align: left;
    flex-direction: column-reverse;
    margin-left: 0px;
  }

  .profile img {
    width: 25px;
    height: 25px;
    margin-left: 0px;
  }
}
</style>

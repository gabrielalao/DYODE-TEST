<template>
  <div>
    <div class="container">
      <b-card overlay img-src="img/img/home1.jpg" img-alt="Card Image" text-variant="white">
        <div class="container-text" style="margin-top:15%; line-height:2cm;">
          <h1 style="color:white; font-family:Pacifico">Title Goes Here</h1>
          <h2 style="color:white; font-family:Lato-Light">Tagline will go right here</h2>
          <b-button squared variant="dark">Shop Now</b-button>
        </div>
      </b-card>
    </div>
    <div class="container" style="font-family:Pacifico; padding-top: 30px;">
      <b-row>
        <b-col>
          <b-card
            no-body
            img-src="img/img/Womens.jpg"
            img-alt="Image"
            img-top
            tag="article"
            class="mb-2"
          >
            <b-card-body style="background: #10504F; color: white; padding: 5px;">
              <b-card-text class="text-center" style="font-size: 30px;">Womens</b-card-text>
            </b-card-body>
          </b-card>
        </b-col>
        <b-col>
          <b-card
            no-body
            img-src="img/img/Mens.jpg"
            img-alt="Image"
            img-top
            tag="article"
            class="mb-2"
          >
            <b-card-body style="background: #10504F; color: white; padding: 5px;">
              <b-card-text class="text-center" style="font-size: 30px;">Mens</b-card-text>
            </b-card-body>
          </b-card>
        </b-col>
        <b-col md="4">
          <b-card
            no-body
            v-bind:img-src="accessory_img"
            img-alt="Image"
            img-top
            tag="article"
            class="mb-2"
          >
            <b-card-body style="background: #10504F; color: white; padding: 5px;">
              <b-card-text class="text-center" style="font-size: 30px;">Accessories</b-card-text>
            </b-card-body>
          </b-card>
        </b-col>
      </b-row>
    </div>

    <div class="container" style="padding-top: 30px;">
      <h1
        style="color: black; font-family:Pacifico; text-align: center;  padding-bottom: 30px;"
      >New Arrivals</h1>
      <b-row>
        <b-col cols="1" style="align-self: center; padding: 0px;">
          <b-img right src="img/img/Arrow Left.png" alt="Left image"></b-img>
        </b-col>
        <b-col cols="10">
          <carousel :per-page="product_show_cnt" :scrollPerPage="false" :paginationEnabled="false">
            <slide data-index="0" data-name="MySlideName" @slideclick="handleSlideClick">
              <b-card
                img-src="img/img/product1.jpg"
                img-alt="Image"
                img-top
                tag="article"
                class="mb-2 no-border"
                style="border:0px;"
              >
                <b-card-text class="text-center">
                  <p style="line-height:0; font-family: Lato-Regular;">Product Title</p>
                  <p style="line-height:0; font-family: Lato-Light; ">Women's T-Shirt</p>
                  <p style="font-family: Pacifico;">$19.99</p>
                </b-card-text>
              </b-card>
            </slide>
            <slide data-index="1" data-name="MySlideName" @slideclick="handleSlideClick">
              <b-card
                img-src="img/img/product1.jpg"
                img-alt="Image"
                img-top
                tag="article"
                class="mb-2"
                style="border:0px;"
              >
                <b-card-text class="text-center">
                  <p style="line-height:0; font-family: Lato-Regular;">Product Title</p>
                  <p style="line-height:0; font-family: Lato-Light; ">Women's T-Shirt</p>
                  <p style="font-family: Pacifico;">$19.99</p>
                </b-card-text>
              </b-card>
            </slide>
            <slide data-index="2" data-name="MySlideName" @slideclick="handleSlideClick">
              <b-card
                img-src="img/img/product1.jpg"
                img-alt="Image"
                img-top
                tag="article"
                class="mb-2"
                style="border:0px;"
              >
                <b-card-text class="text-center">
                  <p style="line-height:0; font-family: Lato-Regular;">Product Title</p>
                  <p style="line-height:0; font-family: Lato-Light; ">Women's T-Shirt</p>
                  <p style="font-family: Pacifico;">$19.99</p>
                </b-card-text>
              </b-card>
            </slide>
            <slide data-index="3" data-name="MySlideName" @slideclick="handleSlideClick">
              <b-card
                img-src="img/img/product1.jpg"
                img-alt="Image"
                img-top
                tag="article"
                class="mb-2"
                style="border:0px;"
              >
                <b-card-text class="text-center">
                  <p style="line-height:0; font-family: Lato-Regular;">Product Title</p>
                  <p style="line-height:0; font-family: Lato-Light; ">Women's T-Shirt</p>
                  <p style="font-family: Pacifico;">$19.99</p>
                </b-card-text>
              </b-card>
            </slide>
            <slide data-index="4" data-name="MySlideName" @slideclick="handleSlideClick">
              <b-card
                img-src="img/img/product1.jpg"
                img-alt="Image"
                img-top
                tag="article"
                class="mb-2"
                style="border:0px;"
              >
                <b-card-text class="text-center">
                  <p style="line-height:0; font-family: Lato-Regular;">Product Title</p>
                  <p style="line-height:0; font-family: Lato-Light; ">Women's T-Shirt</p>
                  <p style="font-family: Pacifico;">$19.99</p>
                </b-card-text>
              </b-card>
            </slide>
            <slide data-index="5" data-name="MySlideName" @slideclick="handleSlideClick">
              <b-card
                img-src="img/img/product1.jpg"
                img-alt="Image"
                img-top
                tag="article"
                class="mb-2"
                style="border:0px;"
              >
                <b-card-text class="text-center">
                  <p style="line-height:0; font-family: Lato-Regular;">Product Title</p>
                  <p style="line-height:0; font-family: Lato-Light; ">Women's T-Shirt</p>
                  <p style="font-family: Pacifico;">$19.99</p>
                </b-card-text>
              </b-card>
            </slide>
          </carousel>
        </b-col>
        <b-col cols="1" style="align-self: center; padding: 0px;">
          <b-img left src="img/img/Arrow Right.png" alt="Right image"></b-img>
        </b-col>
      </b-row>
    </div>

    <div class="container">
      <b-card overlay img-src="img/img/home2.jpg" img-alt="Card Image" text-variant="white">
        <div
          class="container-text"
          style="float: right; margin-top:15%; margin-right: 50px; line-height:2cm;"
        >
          <p style="color:white; font-family:Pacifico; font-size: 30px;">Title Goes Here</p>
          <p style="color:white; font-family:Lato; font-size: 30px;">Tagline will go right here</p>
          <b-button squared variant="dark">Shop Now</b-button>
        </div>
      </b-card>
    </div>

    <div class="container" style="padding-top: 30px;">
      <h1
        style="color: black; font-family:Pacifico; text-align: center; padding-bottom: 30px;"
      >Follow us on Instagram!</h1>
      <b-row>
        <b-col>
          <b-card
            no-body
            img-src="img/img/Social1.jpg"
            img-alt="Image"
            img-top
            tag="article"
            class="mb-2"
          ></b-card>
        </b-col>
        <b-col>
          <b-card
            no-body
            img-src="img/img/Social2.jpg"
            img-alt="Image"
            img-top
            tag="article"
            class="mb-2"
          ></b-card>
        </b-col>
        <b-col>
          <b-card
            no-body
            img-src="img/img/Social3.jpg"
            img-alt="Image"
            img-top
            tag="article"
            class="mb-2"
          ></b-card>
        </b-col>
        <b-col v-if="!mobile">
          <b-card
            no-body
            img-src="img/img/Social4.jpg"
            img-alt="Image"
            img-top
            tag="article"
            class="mb-2"
          ></b-card>
        </b-col>
        <b-col v-if="!mobile">
          <b-card
            no-body
            img-src="img/img/Social5.jpg"
            img-alt="Image"
            img-top
            tag="article"
            class="mb-2"
          ></b-card>
        </b-col>
      </b-row>
    </div>

    <!-- Contact us -->
    <div class="container" style="padding-top: 30px; background: #10504F; color:white;">
      <div class="center-top" style="text-align: center;">
        <span style="font-family:Pacifico; font-size:30px;">
          <b-img src="img/img/Email_Icon.png" alt="Email Icon"></b-img>Signup & stay connected.
        </span>
      </div>
      <div class="center-bottom" style="width:96%; margin-top:1%; padding:1% 5% 2%;">
        <b-row>
          <b-col md="6">
            <p
              style="font-size:12px;line-height:0.5cm; font-weight:600; font-family:Lato;padding:0 5%;"
            >Sign up for the newsletter and get 20% off! Gain access to exclusive offers and be the first to know when new stuff drops!</p>
          </b-col>
          <b-col md="6">
            <b-row>
              <b-col cols="8">
                <b-form-input
                  v-model="text"
                  placeholder="Enter your name"
                  style="font-size:11px;height:38px;border-radius:0 !important;"
                ></b-form-input>
              </b-col>
              <b-col cols="4">
                <b-button
                  variant="primary"
                  style="font-family: Pacifico !important; font-size:9px;border-radius:0 !important;border:solid 3px white;background:rgb(14 59 58);"
                >Subscribe</b-button>
              </b-col>
            </b-row>
          </b-col>
        </b-row>
      </div>
    </div>
  </div>
</template>
<script>
import { Carousel, Slide } from "vue-carousel";

export default {
  name: "components",
  components: {
    Carousel,
    Slide,
  },
  data: () => ({
    windowWidth: 0,
    slides: [
      {
        title: "Slide #1",
        content: "Slide content.",
      },
    ],
    mobile: false,
    product_show_cnt: 4,
    accessory_img: "",
  }),
  created() {
    this.detectOrientationChange(); // when instance is created
  },
  mounted() {
    this.$nextTick(function () {
      window.addEventListener("resize", this.detectOrientationChange);
    });
    window.onresize = () => {
      this.detectOrientationChange();
    };
  },
  methods: {
    handleSlideClick(dataset) {
      console.log(dataset.index, dataset.name);
    },
    detectOrientationChange() {
      this.windowWidth = window.innerWidth;
      if (this.windowWidth > 780) {
        //desktop
        this.accessory_img = "img/img/Accessories.jpg";
        this.product_show_cnt = 4;
        this.mobile = false;
      } else if (this.windowWidth > 400) {
        //mobile
        this.accessory_img = "img/img/Accessories Image Mobile.jpg";
        this.product_show_cnt = 2;
        this.mobile = true;
      } else {
        this.accessory_img = "img/img/Accessories Image Mobile.jpg";
        this.mobile = true;
        this.product_show_cnt = 1;
      }
      console.log(this.product_show_cnt);
      console.log(this.mobile);
      //   switch (window.orientation) {
      //     case -90 || 90:
      //       // landscape
      //       this.product_show_cnt = 4;
      //       this.mobile = false;
      //       break;
      //     default:
      //       // portrait
      //       this.product_show_cnt = 2;
      //       this.mobile = true;
      //       break;
      //   }
    },
  },
};
</script>

<template>
  <v-app>
    <v-main style="background:#010933" class="hidden-md-and-down">
      <div style="margin:0px -20px 30px 200px">
        <v-row no-gutters style="color:white">
          <v-col class="mt-9" style="margin-right:300px" md="1" lg="1" sm="1">
            <v-img src="../assets/NIMC logo.png" width="100px" height="50px" />
          </v-col>
          <v-col style="margin-right:-4000px;float:right" class="mt-12" md="10" lg="10" sm="10">
            <a style="color:white;margin-right:25px"> Recurring Payment</a>
            <a style="color:white;margin-right:25px"> Pricing</a>
            <a style="color:white;margin-right:25px"> Documentation</a>
            <a style="color:white;margin-right:25px"> About us</a>
            <v-btn
              large
              style="border-radius:12px"
              outlined
              class="mr-5"
              color="white"
            >
              Login</v-btn
            >
            <v-btn
              large
              style="border-radius:12px"
              color="#d2ffd7"
              class="black--text"
            >
              Signup</v-btn
            >
          </v-col>
        </v-row>
      </div>

      <v-container>
        <v-row>
          <v-col>
            <h2
              style="width:90%;text-align:start;margin:90px 0px 0px 0px;color:white;font-size:56px"
            >
              Lorem ipsum dolor sit amet, consectetur
            </h2>
            <div style="margin-top:20px;text-align:start">
              <v-btn style="border-radius:12px" href="#developers" x-large color="#d2ffd7">
                Start for free
              </v-btn>
            </div>
          </v-col>
          <v-col>
            <v-card
              color="#d5e7fe"
              height="500px"
              width="500px"
              style="padding:90px; border-radius:30px 50px 30px 40px"
            >
              <v-img
                width="120%"
                height="100%"
                src="https://www.collect.africa/images/home/hero.png"
              />
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>

    <v-main style="background:#010933" class="hidden-lg-and-up">
      <div style="margin:0px 50px 30px 50px">
        <v-row style="color:white">
          <v-col class="mt-9" md="2" lg="2" sm="2">
            <v-img src="../assets/NIMC logo.png" height="70px" width="120px" />
          </v-col>
          <v-col style="float:right" class="mt-12" md="10" lg="10" sm="10">
            <v-btn @click="openNav()" style="float:right" color="white" x-large icon>
              <v-icon>
                mdi-menu
              </v-icon>
            </v-btn>
          </v-col>
        </v-row>

        <v-container>
          <v-row>
            <v-col cols="12" lg="12" sm="4" md="1">
              <h2
                style="width:90%;text-align:start;margin:90px 0px 0px 0px;color:white;font-size:40px"
              >
                Lorem ipsum dolor sit
              </h2>
              <div style="margin-top:20px;text-align:start">
                <v-btn style="border-radius:12px" href="#developers" x-large color="#d2ffd7">
                  Start for free
                </v-btn>
              </div>
            </v-col>
            <v-col cols="12" lg="12" sm="8" md="10">
              <v-card
                color="#d5e7fe"
                style="padding:10%; border-radius:30px 50px 30px 40px"
              >
                <v-img src="https://www.collect.africa/images/home/hero.png" />
              </v-card>
            </v-col>
          </v-row>
        </v-container>
      </div>
    </v-main>

    <div id="myNav" class="overlay">
      <a href="javascript:void(0)" class="closebtn" @click="closeNav()"
        >&times;</a
      >
      <div class="overlay-content">
          <a class="menuLink" style="font-size:23px;color:white"> Recurring Payment</a>
            <a class="menuLink" style="font-size:23px;color:white"> Pricing</a>
            <a class="menuLink" style="font-size:23px;color:white"> Documentation</a>
            <a  class="menuLink" style="font-size:23px;color:white"> About us</a>
      </div>
    </div>
  </v-app>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    openNav() {
      document.getElementById("myNav").style.width = "100%";
    },

    closeNav() {
      document.getElementById("myNav").style.width = "0%";
    }
  }
};
</script>

<style>
.v-btn {
  text-transform: none !important;
}

body {
  font-family: "Lato", sans-serif;
}

.overlay {
  height: 100%;
  width: 0;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  background-color: rgb(0, 0, 0);
  background-color: rgba(0, 0, 0, 0.9);
  overflow-x: hidden;
  transition: 0.5s;
}

.overlay-content {
  position: relative;
  top: 25%;
  width: 100%;
  text-align: center;
  margin-top: 30px;
}

.overlay a {
  padding: 8px;
  text-decoration: none;
  font-size: 36px;
  color: #818181;
  display: block;
  transition: 0.3s;
}

.overlay a:hover,
.overlay a:focus {
  color: #f1f1f1;
}

.overlay .closebtn {
  position: absolute;
  top: 20px;
  right: 45px;
  font-size: 60px;
}

@media screen and (max-height: 450px) {
  .overlay a {
    font-size: 20px;
  }
  .overlay .closebtn {
    font-size: 40px;
    top: 15px;
    right: 35px;
  }
}

.menuLink {
  text-decoration: none;
  color: white !important;
  margin-left: 59px;
}

.menuLink:hover {
  border-bottom: solid 2px #d5e7fe;
  color: #d5e7fe !important;
}

.active {
  border-bottom: solid 2px #d5e7fe;
  color: #d5e7fe !important;
}
</style>

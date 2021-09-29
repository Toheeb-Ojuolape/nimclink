<template>
<div>
  <div class="hidden-md-and-down">
    <v-container>
      <v-row>
        <v-col>
          <h2 style="margin-top:20px;font-size:45px;width:40%">
            Ready to launch across Africa?
          </h2>
          <v-btn
            class="mt-5"
            x-large
            style="color:#4e5042;border-radius:10px"
            color="#d2ffd7"
            >Start for free</v-btn
          >
        </v-col>
      </v-row>
    </v-container>

    <v-card flat tile color="#d5e7fe" class="mt-7" height="60%" width="100%">
      <div style="margin:auto;width:500px;padding:50px 150px 40px 150px">
        <v-img src="../assets/NIMC logo.png" width="100px" height="70px" />
      </div>
      <div style="text-align:center">
        <a style="color:black;margin-right:25px"> Recurring Payment</a>
        <a style="color:black;margin-right:25px"> Pricing</a>
        <a style="color:black;margin-right:25px"> Documentation</a>
        <a style="color:black;margin-right:25px"> About us</a>
        <a style="color:black;margin-right:25px"> Terms and Conditions</a>
        <a style="color:black;margin-right:25px"> Privacy Policy</a>
      </div>
      <hr style="width:80%;margin:40px auto auto auto" />
      <div style="width:80%;margin:40px auto auto auto">
        <p>
          © 2021 NIMCLink. All rights reserved
          <v-btn depressed x-small style="float:right" fab
            ><v-icon color="black">mdi-linkedin</v-icon></v-btn
          >
        </p>
      </div>
    </v-card>
  </div>

  <div class="hidden-lg-and-up">
    <v-container>
      <v-row>
        <v-col style="padding:70px 20px 70px 20px">
          <h2>
            Ready to launch across Africa?
          </h2>
          <v-btn
            class="mt-5"
            x-large
            style="color:#4e5042;border-radius:10px"
            color="#d2ffd7"
            >Start for free</v-btn
          >
        </v-col>
      </v-row>
    </v-container>
    <v-card flat tile color="#d5e7fe" class="text-center mt-7 pb-6" height="100%">
      <div style="margin:auto;padding:50px 150px 40px 150px">
        <v-img src="../assets/NIMC logo.png"  />
      </div>
      <div style="text-align:center">
        <a style="color:black;margin-right:25px"> Recurring Payment</a>
        <a style="color:black;margin-right:25px"> Pricing</a>
        <a style="color:black;margin-right:25px"> Documentation</a>
        <a style="color:black;margin-right:25px"> About us</a>
        <a style="color:black;margin-right:25px"> Terms and Conditions</a>
        <a style="color:black;margin-right:25px"> Privacy Policy</a>
      </div>
      <hr style="width:80%;margin:40px auto auto auto" />
      <div style="width:80%;margin:40px auto auto auto">
        <p>
          © 2021 NIMCLink. All rights reserved
        </p>
        <v-btn depressed x-small style="text-align:center" fab
            ><v-icon color="black">mdi-linkedin</v-icon></v-btn
          >
      </div>
    </v-card>
  </div>

  </div>
</template>

<script>
export default {};
</script>

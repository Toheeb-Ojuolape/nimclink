<template>
  <v-app>
  <Banner />
  <Summary />
  <Accept />
  <Steps />
  <Developers @showLoading="showLoading" />
  <Ready />
  <v-overlay
      style="text-align:center"
      :absolute="absolute"
   
      v-model="loadingDialog"
    >
      <v-progress-circular
        :size="30"
        :width="5"
        color="#000000"
        class="text-center"
        indeterminate
      ></v-progress-circular>
    </v-overlay>
  </v-app>
</template>



<script>
import Banner from "../components/Banner.vue"
import Summary from "../components/Summary.vue"
import Accept from "../components/Accept.vue"
import Steps from "../components/Steps.vue"
import Developers from "../components/Developers.vue"
import Ready from '../components/Ready.vue'

export default {
  name: 'Home',
  data(){
    return{
      loadingDialog:false
    }
  },
  components: {
    Banner,
    Summary,
    Accept,
    Steps,
    Developers,
    Ready
  },
  methods:{
    showLoading(){
      this.loadingDialog = true
      setTimeout(()=>{
        this.loadingDialog = false
      },2000)
    }
  }
}
</script>

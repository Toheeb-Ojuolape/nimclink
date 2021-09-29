<template>
  <v-app>
    <v-main class="hidden-md-and-down">
         <h2 style="margin-top:50px;text-align:center;font-size:45px">Made for Developers</h2>
        <v-row class="pa-7">
         <v-col>
           <div id="developers" style="width:90%;margin:40px auto auto auto">
      <v-card style="margin:auto;border-radius:12px;padding:120px 90px 0px 90px" height="350px" class="mt-4 text-center" color="#010933">
    <h2 class="white--text">Tap the button below to get started </h2>
       <v-btn @click="showLoading()" large class="mt-5">Click here to run</v-btn>
     </v-card>
     </div>  
         </v-col>
         <v-col>
             <div style="margin-left:70px;width:70%">
             <h2 style="font-size:40px;margin:50px 20px 0px 20px">
        Hit the ground running with a few lines of code
      </h2>
      <p style="color:grey;margin:20px 20px 0px 20px">
        We’ve battle-tested our platform with hundreds of use cases and pulled
        through everything you need to integrate seamlessly and start accepting
        payment sooner
      </p>

      <h2 style="font-size:40px;margin:50px 20px 0px 20px">
        Documentation
      </h2>
      <p style="color:grey;margin:20px 20px 0px 20px">
        Your team will have everything covered with our comprehensive documentation
      </p>

      <h2 style="font-size:40px;margin:50px 20px 0px 20px">
        Webhooks & APIs
      </h2>
      <p style="color:grey;margin:20px 20px 0px 20px">
        Listen for events and create custom workflows on your end using our powerful APIs
      </p>
      </div>
        </v-col>
        </v-row>
        
    </v-main>

    <v-main class="pt-12 hidden-lg-and-up">
      <h2 style="text-align:center;font-size:30px">Made for Developers</h2>
      <h2 style="margin:50px 20px 0px 20px">
        Hit the ground running with a few lines of code
      </h2>
      <p style="color:grey;margin:20px 20px 0px 20px">
        We’ve battle-tested our platform with hundreds of use cases and pulled
        through everything you need to integrate seamlessly and start accepting
        payment sooner
      </p>

      <h2 style="margin:50px 20px 0px 20px">
        Documentation
      </h2>
      <p style="color:grey;margin:20px 20px 0px 20px">
        Your team will have everything covered with our comprehensive documentation
      </p>

      <h2 style="margin:50px 20px 0px 20px">
        Webhooks & APIs
      </h2>
      <p style="color:grey;margin:20px 20px 0px 20px">
        Listen for events and create custom workflows on your end using our powerful APIs
      </p>

    <div id="developers" style="width:90%;margin:40px auto auto auto">
      <v-card style="margin:auto;border-radius:12px" class="mt-4 text-center pa-8" color="#010933">
    <h2 class="white--text">Tap the button below to get started </h2>
       <v-btn @click="showLoading()" large class="mt-5">Click here to run</v-btn>
     </v-card>
     </div>


     <v-dialog width="400px" persistent v-model="showDialog">
    <QRdialog @closeModal="closeModal"/>
    <v-btn outlined color="white" class="mt-3 mx-auto"> <v-icon class="mr-3">mdi-lock</v-icon>SECURED BY SWIFTEND</v-btn>
    </v-dialog>



    </v-main>
  </v-app>
</template>


<script>
import QRdialog from '../components/QRdialog.vue'


export default {
    data(){
        return{
            showDialog:false,
            loadingDialog:false,
            absolute:true
        }

    },

    components:{
        QRdialog
    },
    methods:{
        closeModal(){
            this.showDialog = false
        },
        showLoading(){
            this.$emit("showLoading")
            setTimeout(()=>{
                this.showDialog = true
                this.loadingDialog  = false
            },2000)
        }
    }
}
</script>


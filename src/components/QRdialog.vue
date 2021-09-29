<template>

<v-card width="400px" height="395px" class="pa-8" style="border-radius:15px">
    <v-window v-model="step">
        <v-window-item :value=1>
    <v-btn small depressed fab @click="closeModal()"><v-icon>mdi-close</v-icon></v-btn>
    <h2 style="padding:10px;text-align:center;margin-bottom:10px">Please select an option:</h2>
    <div>
    <v-btn @click="step=2" x-large outlined color="#010933" block>
       <v-icon class="mr-3">mdi-account-circle</v-icon> User ID
    </v-btn>
    </div>

    <div style="margin-top:20px">
    <v-btn @click="step = 5" x-large class="mb-3" outlined color="#010933" block>
      <v-icon class="mr-3">mdi-bank</v-icon>  Virtual ID
    </v-btn>
    </div>

        </v-window-item>

        <!--For User ID -->
        <v-window-item :value="2">
          <v-btn small depressed fab @click="step--"><v-icon>mdi-arrow-left</v-icon></v-btn>
          <v-img :loading="loading" height="150px" width="150px" style="margin:auto" :lazy-src="`https://api.qrserver.com/v1/create-qr-code/?size=70x70&data=${pin}`" :src="`https://api.qrserver.com/v1/create-qr-code/?size=70x70&data=${pin}`" />
        <p style="margin:10px 0px 0px 0px;font-size:10px;text-align:center">Your randomly generated 6-digit pin is:</p>
        <h2 class="text-center">{{pin}}</h2>
        <v-btn @click="step++" color="#010933" style="border-radius:12px" class="mt-3 white--text" block large>
            Continue
        </v-btn>

          <v-btn  @click="closeModal()" text style="border-radius:12px" block class="text-center mb-3 mt-3 black--text">
            Cancel
        </v-btn>
        </v-window-item>
        
        <v-window-item :value="3">
          <v-btn small depressed fab @click="step--"><v-icon>mdi-arrow-left</v-icon></v-btn>
        <p class="mt-8 text-center">Enter your Virtual NIN </p>
        <v-text-field @keyup="stopDisabled()" outlined type="Number" color="#010933" style="border-radius:12px" label="Virtual NIN" v-model="vNIN"/>
         <v-btn :disabled="disabled" @click="step++" color="#010933" style="border-radius:12px" class="mt-3 white--text" block large>
            Continue
        </v-btn>
        <v-btn  @click="closeModal()" text style="border-radius:12px" block class="text-center mb-3 mt-3 black--text">
            Cancel
        </v-btn>
        </v-window-item>


         <v-window-item :value="4">
          <v-btn small depressed fab @click="step--"><v-icon>mdi-arrow-left</v-icon></v-btn>
          <div style="margin:auto;width:90%">
        <div style="margin:auto;width:50%">
          <v-btn fab depressed style="text-align:center;margin:auto" width="100px" height="100px" color="green">
              <v-icon size="50px" color="white">mdi-check </v-icon>
          </v-btn>
          </div>
          <p class="mt-3 text-center">Transaction Approved </p>
           </div>
          <v-btn @click="closeModal()" color="#010933" style="border-radius:12px" class="mt-3 white--text" block large>
            Complete
        </v-btn>
        </v-window-item>


        <v-window-item :value="5">
          <v-btn small depressed fab @click="step=1"><v-icon>mdi-arrow-left</v-icon></v-btn>
        <p class="mt-8 text-center">Enter your Virtual NIN </p>
        <v-text-field @keyup="stopDisabled()" outlined type="Number" color="#010933" style="border-radius:12px" label="Virtual NIN" v-model="vNIN"/>
         <v-btn :disabled="disabled" @click="step++" color="#010933" style="border-radius:12px" class="mt-3 white--text" block large>
            Continue
        </v-btn>
        <v-btn  @click="closeModal()" text style="border-radius:12px" block class="text-center mb-3 mt-3 black--text">
            Cancel
        </v-btn>
        </v-window-item>

         <v-window-item :value="6">
          <v-btn small depressed fab @click="step--"><v-icon>mdi-arrow-left</v-icon></v-btn>
          <div style="margin:auto;width:90%">
        <div style="margin:auto;width:50%">
          <v-btn fab depressed style="text-align:center;margin:auto" width="100px" height="100px" color="green">
              <v-icon size="50px" color="white">mdi-check </v-icon>
          </v-btn>
          </div>
          <p class="mt-3 text-center">Transaction Approved </p>
           </div>
          <v-btn @click="closeModal()" color="#010933" style="border-radius:12px" class="mt-3 white--text" block large>
            Complete
        </v-btn>
        </v-window-item>

    </v-window>
</v-card>
    
</template>




<script>

export default{
    data(){
        return{
            step:1,
            value: 'https://example.com',
            size: 300,
            pin:123254,
            vNIN:"",
            loading:true,
            disabled:true
        }
    },

    components:{
    
    },

    created(){
    this.pin = Math.floor(100000 + Math.random() * 900000)
    },
    methods:{
        closeModal(){
            this.step = 1
            this.$emit('closeModal')
        },

        stopDisabled(){
            if(this.vNIN != ""){
                this.disabled = false
            }else{
                this.disabled = true
            }
        }
    }
}


</script>
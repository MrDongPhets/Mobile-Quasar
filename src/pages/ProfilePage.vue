<template>
    <q-page style=" position: relative;
    min-height: 770px;
    padding: 2px;
    gap: 1px;
    box-shadow: 0 1px 10px rgba(0, 0, 0, 0.3);
    border-radius: 30px;
    z-index: 2;">
  
      <!-- <div class="wrap">
        <div class="circle"> 
      </div>
      </div> -->
     
      <div class="search q-shadow-lg">
       <div class="searchbar flex justify-center ">
       <q-icon name="menu" class="q-m-lg" style="font-size: 34px;
       margin-right: 20px;" />
       <q-input
       v-model="searchTerm"
       borderless
       dense
       placeholder="Search..."
  
       style="width: 66%; height: 30px; "
      
     />
     <q-icon name="search" style="font-size: 34px;"/>
     </div>
   
     </div>
  
     <div class="flex justify-center" style="margin-top: 30px;">
      <div style="height: 40px; padding: 1px;">
         <p style="font-size: 30px; color: #018a88;">911 Call Emergency</p>
         
      </div>
      
     </div>
  
     <div class="flex justify-center" style="margin-top: 10px;">
         <div class="text-center" style="width: 350px; align-items: center;  margin-top: 10px;">
         <p style="">Call emergency on the City Hotline or report crime and 
           emergency situations in Realtime response.</p>
        </div>
      </div>
  
      
     <div class="flex justify-center" style="margin-top: 10px; ">
         <div class="text-center" style="width: 300px; align-items: center;  margin-top: 10px; height: 20px;">
         <p style="color: #018a88;">Profile Completion</p>
        </div>
      </div>
  
      <div class="">
        <div class="q-pa-md q-gutter-md">
      <q-linear-progress
        v-for="size in ['xs']"
        :key="size"
        :size="size"
        :value="progress"
        color="primary"
        @click="randomize"
      />
    </div>
      </div>
  
      <div class="flex justify-center" style="margin-top: 1px; margin-bottom: 10px;">
         <div class="text-center" style="width: 300px; align-items: center; height: 20px;">
         <p style="font-size: 10px;">Complete your profile to access all Verified Citizen Privilleges</p>
        </div>
      </div>
       
       
    </q-page>
  
  </template>
  
  <script>
  import { ref } from 'vue'
  
  export default {
    setup () {
      const progress = ref(0.15)
  
      return {
        progress,
        randomize () {
          progress.value = Math.random()
        }
      }
    }
  }
  </script>
  <style scoped>
   @import 'src/css/style.css';
  
  
  </style>
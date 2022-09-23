<script setup lang="ts">
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";


import { onMounted } from 'vue';
import { RouterLink, RouterView } from 'vue-router'
import ItsMe from './components/ItsMe.vue'
gsap.registerPlugin(ScrollTrigger);
onMounted(() => {
  gsap.to("#imgdiv", {
    duration: 1.5,
    right:300,
    top:200,
    width:720,
    height:452,
    scrollTrigger:{
      trigger:'#section2',
      start:"center bottom",
      end : "bottom bottom",
      scrub:true,
      markers:true
    }
  });
  gsap.to("#imgdiv2", {
    duration: 1.5,
    left:300,
    top:200,
    width:720,
    height:452,
    scrollTrigger:{
      trigger:'#section3',
      start:"center bottom",
      end : "bottom bottom",
      scrub:true,
      markers:true
    }
  });
});
</script>

<template>
  <div  class=" bg-neutral-900  min-h-screen text-white">
    <div class="max-w-7xl m-auto p-8  border-x  min-h-screen">
     
      <div class="py-4  w-full space-x-4">
        
        <ItsMe class="text-5xl"  msg="Hi,i'm Amin Bakhti"></ItsMe>
        
        
      </div>
      <RouterView />
      <nav>
          <RouterLink to="/">Home</RouterLink>
          <RouterLink to="/about">About</RouterLink>
      
        </nav>

      

    </div>
    <div id="section2" class="   border-t h-full  relative  min-h-[1024px]">
    
     <div class="py-4  w-full space-x-4 h-full">
        
       <ItsMe class="text-5xl"  msg="Hi,i'm Amin Bakhti"></ItsMe>
       
       
     </div>
     <RouterView />
      <nav>
         <RouterLink to="/">Home</RouterLink>
         <RouterLink to="/about">About</RouterLink>
     
      </nav>
        <div id="imgdiv" class="bg-neutral-700  w-full absolute  top-0 bottom-0 h-full "> 

          something
        </div> 
     

    </div>
    <div id="section3" class="   border-t h-full  relative   min-h-[1024px]">
    
    <div class="py-4  w-full space-x-4 h-full">
       
      <ItsMe class="text-5xl"  msg="Hi,i'm Amin Bakhti"></ItsMe>
      
      
    </div>
    <RouterView />
     <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
    
     </nav>
       <div id="imgdiv2" class="bg-neutral-700  w-full absolute  top-0 bottom-0 h-full "> 

         something
       </div> 
    

   </div>
   


  </div>
 
</template>

<style scoped>

</style>

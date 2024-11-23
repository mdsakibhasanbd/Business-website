<template>
    <Nav />
  
    <div class="absolute top-0 -z-10 w-full h-screen">
      <div class="relative w-full h-full">
        <div class="w-full h-full">
          <img src="/img/main image.png" alt="" class="object-cover w-full h-full" />
        </div>
  
        <!-- Centered Heading -->
        <!-- <h1 class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 font-outfit text-4xl text-white">
          fjaks
        </h1> -->
        <div class=" absolute top-1/2 left-4  -translate-y-1/2">
            <div class="">
                <div class=" text-white">
                    <span class="text-5xl font-outfit font-outfit-bold ">
                        Unleashing Potential,
                        <br> With Innovative Business 
                        <br> Solutions
                    </span>

                </div>

                <div class="py-4">
                    <span class="text-md  text-white font-poppins">
                        transforming visions into reality: your successful is our mission
                    </span>
                </div>

                <div class="">
                    <button class="  rounded-lg  font-poppins bg-white text-[#0D0B56] py-2 px-4"> 
                        contact us today
                    </button>
                </div>

            </div>
        </div>
  
       
      </div>
    </div>
  </template>
  
  <script>
  import Nav from '../Nav.vue';
  export default {
    components: {
      Nav,
    },
  };
  </script>
  
  <style >
  @import url('https://fonts.googleapis.com/css2?family=Outfit:wght@400;500;600;700&display=swap');
  .font-outfit {    
    font-family: 'Outfit', sans-serif;  
    font-weight: 700;
  }
 
  .font-poppins {
  font-family: "Poppins", sans-serif;
  font-weight: 400;
  font-style: normal;
}

</style>
  
<template>
  <div class="w-full h-screen relative">
    <div class="w-full h-full">
      <div class="w-full h-full">
        <img
          src="/img/main image.png"
          alt="Main Image"
          class="object-cover w-full h-full"
        />
      </div>

      <div class="absolute  left-4 px-4 sm:left-4 sm:top-1/3 sm:translate-x-0 sm:text-left">
        <div class="">
          <div class="text-white">
            <span class="text-5xl font-outfit font-bold md:text-4xl sm:text-3xl">
              Unleashing Potential,
              <br />
              With Innovative Business
              <br />
              Solutions
            </span>
          </div>

          <div class="py-4">
            <span class="text-md text-white font-poppins md:text-sm">
              Transforming visions into reality: your success is our mission
            </span>
          </div>

          <div>
            <button class="rounded-lg font-poppins bg-white text-[#0D0B56] py-2 px-4 hover:bg-[#0D0B56] hover:text-white transition duration-300">
              Contact Us Today
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Nav from "../Nav.vue";
export default {
  components: {
    Nav,
  },
};
</script>

<style scoped>
.font-outfit {
  font-family: "Outfit", sans-serif;
  font-weight: 700;
}

.font-poppins {
  font-family: "Poppins", sans-serif;
  font-weight: 400;
  font-style: normal;
}
</style>

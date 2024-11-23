<template>
    <nav class="fixed  w-full left-0 top-0 z-50 bg-transparent border-gray-200 transition-all duration-300">
      <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
        <!-- Logo -->
        <span class="text-white self-center uppercase text-2xl font-semibold whitespace-nowrap cursor-pointer">Business</span>
        
        <!-- Hamburger Button -->
        <button 
          data-collapse-toggle="navbar-default" 
          type="button" 
          class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600" 
          aria-controls="navbar-default" 
          :aria-expanded="!isMenuHidden"
          @click="toggleNavMenu">
          <span class="sr-only">Open main menu</span>
          <svg class="w-5 h-5" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14" aria-hidden="true">
            <path 
              stroke="currentColor" 
              stroke-linecap="round" 
              stroke-linejoin="round" 
              stroke-width="2" 
              d="M1 1h15M1 7h15M1 13h15" />
          </svg>
        </button>
    
        <!-- Navbar Menu -->
        <div 
          :class="{'hidden': isMenuHidden}" 
          class="w-full md:block md:w-auto" 
          id="navbar-default">
          <ul class="font-medium flex flex-col p-4 md:p-0 mt-4 border rounded-lg md:flex-row md:space-x-8 rtl:space-x-reverse md:mt-0 md:border-0">
            <!-- Links -->
            <li>
              <a 
                href="#" 
                :class="activeClass('home')" 
                @click="setActiveLink('home')">Home</a>
            </li>
            <li>
              <a 
                href="#" 
                :class="activeClass('about')" 
                @click="setActiveLink('about')">About Us</a>
            </li>
            <!-- Dropdown Menu -->
            <li class="relative">
              <button 
                @click="toggleServicesDropdown" 
                class="relative block py-2 text-white rounded focus:outline-none">
                Services
                <svg 
                  class="inline w-4 h-4 ml-2" 
                  xmlns="http://www.w3.org/2000/svg" 
                  fill="none" 
                  viewBox="0 0 24 24" 
                  stroke-width="2" 
                  stroke="currentColor">
                  <path 
                    stroke-linecap="round" 
                    stroke-linejoin="round" 
                    d="M19 9l-7 7-7-7" />
                </svg>
              </button>
              <ul 
                id="servicesDropdown" 
                :class="{'hidden': isServicesDropdownHidden}" 
                class="absolute left-0 mt-2 bg-gray-800 rounded-md p-2 shadow-lg">
                <li><a href="#" class="block py-1 text-white hover:bg-gray-700 rounded">Web Development</a></li>
                <li><a href="#" class="block py-1 text-white hover:bg-gray-700 rounded">Mobile Apps</a></li>
                <li><a href="#" class="block py-1 text-white hover:bg-gray-700 rounded">Cloud Solutions</a></li>
              </ul>
            </li>
            <li>
              <a 
                href="#" 
                :class="activeClass('contact')" 
                @click="setActiveLink('contact')">Contact Us</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isMenuHidden: true,
        isServicesDropdownHidden: true,
        activeLink: "home", // Default active link
      };
    },
    methods: {
      toggleNavMenu() {
        this.isMenuHidden = !this.isMenuHidden;
      },
      toggleServicesDropdown() {
        this.isServicesDropdownHidden = !this.isServicesDropdownHidden;
      },
      setActiveLink(link) {
        this.activeLink = link;
      },
      activeClass(link) {
        return link === this.activeLink
          ? "relative block py-2 text-blue-400 font-semibold before:absolute before:left-0 before:bottom-0 before:h-[2px] before:w-full before:bg-blue-400"
          : "relative block py-2 text-white hover:text-blue-400 hover:before:w-full before:absolute before:left-0 before:bottom-0 before:h-[2px] before:w-0 before:bg-white before:transition-all before:duration-300";
      },
      handleScroll() {
        const navbar = document.querySelector("nav");
        if (window.scrollY > 50) {
          navbar.classList.add("bg-gray-900");
          navbar.classList.remove("bg-transparent");
        } else {
          navbar.classList.add("bg-transparent");
          navbar.classList.remove("bg-gray-900");
        }
      },
    },
    mounted() {
      window.addEventListener("scroll", this.handleScroll);
    },
    beforeDestroy() {
      window.removeEventListener("scroll", this.handleScroll);
    },
  };
  </script>
  
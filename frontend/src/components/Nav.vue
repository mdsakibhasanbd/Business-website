<template>
<nav class="z-50 bg-transparent border-gray-200">
    <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
        <span class="text-white self-center uppercase text-2xl font-semibold whitespace-nowrap">Business</span>

        <button data-collapse-toggle="navbar-default" type="button" class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600" aria-controls="navbar-default" aria-expanded="false" @click="toggleNavMenu">
            <span class="sr-only">Open main menu</span>
            <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
                <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15" />
            </svg>
        </button>

        <div class="w-full hidden md:block md:w-auto" id="navbar-default">
            <ul class="font-medium flex flex-col p-4 md:p-0 mt-4 border  rounded-lg  md:flex-row md:space-x-8 rtl:space-x-reverse md:mt-0 md:border-0 ">
                <li>
                    <a href="#" class="relative block py-2  text-white rounded before:absolute before:left-0 before:bottom-0 before:h-[2px] before:w-0 before:bg-white before:transition-all before:duration-300 hover:before:w-full">
                      Home
                    </a>
                </li> <li>
                    <a href="#" class="relative block py-2  text-white rounded before:absolute before:left-0 before:bottom-0 before:h-[2px] before:w-0 before:bg-white before:transition-all before:duration-300 hover:before:w-full">
                      About us
                    </a>
                </li> <li>
                    <a href="#" class="relative block py-2  text-white rounded before:absolute before:left-0 before:bottom-0 before:h-[2px] before:w-0 before:bg-white before:transition-all before:duration-300 hover:before:w-full">
                      Services
                    </a>
                </li> <li>
                    <a href="#" class="relative block py-2  text-white rounded before:absolute before:left-0 before:bottom-0 before:h-[2px] before:w-0 before:bg-white before:transition-all before:duration-300 hover:before:w-full">
                      Contact us
                    </a>
                </li>

            </ul>
        </div>
    </div>
</nav>
</template>

<script>
export default {
    methods: {
        toggleNavMenu() {
            const navbarMenu = document.getElementById("navbar-default");
            navbarMenu.classList.toggle("hidden");
        },
        toggleServicesDropdown() {
            const servicesDropdown = document.getElementById("servicesDropdown");
            servicesDropdown.classList.toggle("hidden");
        },
    },
};
</script>

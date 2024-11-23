<template>
<HomeLayout>
    <Nav />
    <Main />
    <Customer />
    <Consult />
</HomeLayout>
</template>

<script>
import Consult from '@/components/Home/Consult.vue';
import Nav from '@/components/Nav.vue';
import Customer from '@/components/Home/Customer.vue';
import Main from '@/components/Home/Main.vue';
import HomeLayout from '@/components/Layout/HomeLayout.vue';
// import Nav from '@/components/Nav.vue';
// import HomePage from '@/components/Nav.vue';
export default {
    components: {
        Main,
        HomeLayout,
        Customer,
        Nav,
        Consult

    },
}
</script>

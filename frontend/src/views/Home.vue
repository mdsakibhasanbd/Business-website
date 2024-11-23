<template>
<HomeLayout>
    <Main />
</HomeLayout>
</template>

<script>
import Main from '@/components/Home/Main.vue';
import HomeLayout from '@/components/Layout/HomeLayout.vue';
// import Nav from '@/components/Nav.vue';
// import HomePage from '@/components/Nav.vue';
export default {
    components: {
        Main,
        HomeLayout
    },
}
</script>

<template>
    <HeaderPage />
    <h1>Hello User, Welcome on Add Restaurant Page</h1>

</template>

<script>
import HeaderPage from './HeaderPage.vue';
export default {
    name: 'AddResto',
    components:{
        HeaderPage
    },
    mounted() {
        let user = localStorage.getItem('user-info');
        if (!user) {
            this.$router.push({ name: 'SignUp' })
        }
    }

}
</script>
<template>
    <Header></Header>
    <main>
        <About></About>
        <Teams></Teams>
        <Customers></Customers>
        <Testimonials></Testimonials>
    </main>
    <Footer></Footer>
</template>
    
<script>
import Header from '~/components/Menu/Header.vue'
import About from '~/components/About/about.vue'
import Teams from '~/components/Team/teams.vue'
import Customers from '~/components/Customers/customers.vue'
import Testimonials from '~/components/Testimonials/testimonials.vue'
import Footer from '~/components/Footer.vue'

export default {
    components: {
        Header,
        About,
        Teams,
        Customers,
        Testimonials,
        Footer,
    }
}
</script>

<style>
body{
 }
</style>
    
    
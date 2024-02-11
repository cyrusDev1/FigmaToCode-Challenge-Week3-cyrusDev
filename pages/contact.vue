<template>
    <Header></Header>
    <main>
        <Contact></Contact>
        <Details></Details>
     </main>
    <Footer></Footer>
</template>
    
<script>
import Header from '~/components/Menu/Header.vue'
import Contact from '~/components/Contact/contact.vue'
import Details from '~/components/Contact/details.vue'
import Footer from '~/components/Footer.vue'

export default {
    components: {
        Header,
        Contact,
        Details,
        Footer,
    }
}
</script>

<style>
body{
}
</style>
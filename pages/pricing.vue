<template>
    <Header></Header>
    <main>
        <InnerHeader :dynamicText="dynamicText"></InnerHeader>
        <Pricing></Pricing>
        <Faqs></Faqs>
        <FreeTrial></FreeTrial>
    </main>
    <Footer></Footer>
</template>
    
<script>
import Header from '~/components/Menu/Header.vue'
import InnerHeader from '~/components/InnerHeader.vue'
import Faqs from '~/components/Pricing/faqs.vue'
import Pricing from '~/components/Pricing/pricing.vue'
import FreeTrial from '~/components/FreeTrial.vue'

import Footer from '~/components/Footer.vue'

export default {
    components: {
        Header,
        InnerHeader,
        Pricing,
        Footer,
        Faqs,
        FreeTrial
    },

    data() {
        return {
            dynamicText: {
                subtitle: 'PRICING',
                title: 'Simple Pricing',
                active: 'Pricing',
            },
        };
    },
}
</script>

<style>
body {
}
</style>
    
    

import { componentNames } from '#build/components';
<template>
    <section class="mt-20 mx-5 xl:mx-40">
        <div class="">
            <div class="text-center space-y-4">
                <h2 class="text-4xl font-bold">Pricing FAQs</h2>
                <p class="xl:w-2/5 text-xl mx-auto"> Problems trying to resolve the conflict between
                    the two major realms of Classical physics: Newtonian mechanics </p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 mt-16 gap-16">
                <Faq></Faq>
                <Faq></Faq>
                <Faq></Faq>
                <Faq></Faq>
                <Faq></Faq>
                <Faq></Faq>
            </div>
            <div class="mt-10">
                <p class="text-[#737373] text-center text-2xl">Haven’t got your answer? Contact our support</p>
            </div>
        </div>
    </section>
</template>

<script>
import Faq from '~/components/Pricing/faq.vue'

export default {
    components: {
        Faq
    }
};

</script>

<style></style>

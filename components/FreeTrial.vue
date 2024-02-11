<template>
    <div class="flex justify-center text-center mt-40 mb-20 mx-10">
        <div class="space-y-8">
            <h2 class="text-4xl font-bold">Start your 14 days free trial</h2>
            <p class="text-md xl:w-3/5 mx-auto text-[#737373]">Met minim Mollie non desert Alamo est sit cliquey dolor
                do met sent. RELIT official consequent.</p>
            <div class="flex justify-center">
                <Button :buttonText="buttonText"></Button>
            </div>
            <div class="flex gap-4 items-center justify-center">
                <img class="" src="../assets/img/icons/facebook.png" alt="">
                <img class="" src="../assets/img/icons/instagram.png" alt="">
                <img class="" src="../assets/img/icons/twitter.png" alt="">
            </div>
        </div>
    </div>
</template>

<script>
import Button from '~/components/Button.vue'

export default {
    components: {
        Button
    },
    data() {
        return {
            buttonText: 'Try it for free'
        }
    }
};

</script>

<style></style>

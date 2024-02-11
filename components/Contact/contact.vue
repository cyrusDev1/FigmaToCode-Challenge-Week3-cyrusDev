<template>
    <section class="mt-20 px-10 xl:px-40">
        <div class="block lg:flex justify-between 2xl:h-screen">
            <div class="flex about-text items-center justify-center text-center lg:text-left lg:justify-left">
                <div class="space-y-8">
                    <div class="space-y-8">
                        <h2 class="uppercase font-bold text-xl">Contact Us</h2>
                        <h1 class="font-bold text-4xl lg:text-6xl w-full lg:w-2/4">Get in touch today!</h1>
                        <p class="text-[#737373] text-2xl w lg:w-2/4 mx-auto lg:mx-0">We know how large
                            objects will act, but things
                            on a small scale</p>
                    </div>
                    <div class="space-y-4">
                        <p class="font-bold text-xl">Phone : +451 215 215</p>
                        <p class="font-bold text-xl">Fax : +451 215 215</p>
                    </div>
                    <div class="flex mt-3 justify-center lg:justify-start space-x-4">
                        <img src="../../assets/img/icons/facebook.png" alt="">
                        <img src="../../assets/img/icons/instagram.png" alt="">
                        <img src="../../assets/img/icons/twitter.png" alt="">
                    </div>
                </div>
            </div>
            <div class="px-5 flex justify-center mt-20 xl:mt-0">
                <div class="relative">
                    <img class="absolute w-[600px] z-20" src="../../assets/img/contact/deco.png" alt="">
                    <img class="w-[600px] deco z-10" src="../../assets/img/contact/none.png" alt="">
                </div>
            </div>
        </div>
    </section>
</template>

<script>

export default {
    components:{
        
    },
    data(){
        return {
        }
    },
    setup() {
        const { $gsap } = useNuxtApp()
        onMounted(() => {
            $gsap.from('.about-text', { opacity: 0, duration: 1, y: 50 });
            $gsap.from('.deco', { scale: 1.05, yoyo: true, repeat: -1, duration: 0.7 });
            $gsap.from('.play', { scale: 1.05, yoyo: true, repeat: -1, duration: 0.7 });
        });
    },
};

</script>
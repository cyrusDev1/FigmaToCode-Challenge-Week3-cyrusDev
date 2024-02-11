<template>
    <section class="mt-20 px-10 xl:px-40 mb-20">
        <div class="block lg:flex justify-between">
            <div class="flex about-text items-center justify-center text-center lg:text-left lg:justify-left">
                <div class="space-y-8">
                    <div class="space-y-8">
                        <h2 class="uppercase font-bold text-xl">About company</h2>
                        <h1 class="uppercase font-bold text-4xl lg:text-6xl">About us</h1>
                        <p class="text-[#737373] text-2xl lg:w-2/4 mx-auto lg:mx-0">We know how large
                            objects will act, but things
                            on a small scale</p>
                    </div>
                    <div class="flex lg:justify-start justify-center">
                        <a class="px-6 py-4 w-60 bg-[#23A6F0] capitalize rounded-lg text-white text-center hover:bg-white hover:text-[#23A6F0] border border-[#23A6F0]" href="#">Get Quote Now</a>
                    </div>
                </div>
            </div>
            <div class="px-5 flex justify-center">
                <div class="relative">
                    <img class="absolute deco w-[600px]" src="../../assets/img/about/deco.png" alt="">
                    <img class="w-[600px]" src="../../assets/img/about/none.png" alt="">
                </div>
            </div>
        </div>
        <div class="mt-20 space-y-20">
            <div class="grid grid-cols-1 sm:grid-cols-2 xl:grid-cols-4 gap-20 sm:gap-10 lg:gap-6">
                <div class="text-center">
                    <h2 class="font-bold text-7xl text-[#252B42]">15k</h2>
                    <p class="text-[#737373] text-2xl">Happy Customers</p>
                </div>
                <div class="text-center">
                    <h2 class="font-bold text-7xl text-[#252B42]">150k</h2>
                    <p class="text-[#737373] text-2xl">Monthly Visitors</p>
                </div>
                <div class="text-center">
                    <h2 class="font-bold text-7xl text-[#252B42]">15</h2>
                    <p class="text-[#737373] text-2xl">Countries  Worldwide</p>
                </div>
                <div class="text-center">
                    <h2 class="font-bold text-7xl text-[#252B42]">100+</h2>
                    <p class="text-[#737373] text-2xl">Top Partners</p>
                </div>
            </div>
            <div class="block xl:flex justify-between px:0 xl:px-20 gap-8">
                <div class="text-center xl:text-left space-y-8 mb-10 xl:mb-0">
                    <h2 class="text-[#E74040]">Problems trying</h2>
                    <p class="text-2xl font-bold w-3/4 text-[#252B42] mx-auto  xl:mx-0">Met minim Mollie non desert Alamo est sit cliquey dolor do met sent.</p>
                </div>
                <div class="flex items-center">
                    <p class="text-xl text-[#737373]">Problems trying to resolve the conflict between the two major realms of Classical physics: Newtonian mechanics </p>
                </div>
            </div>
            <div class="px-0 xl:px-20">
                <div class="relative flex items-center justify-center">
                    <img class="z-10 w-full h-[300px] md:h-[600px] rounded-3xl" src="../../assets/img/about/media-cover.png" alt="">
                    <img class="absolute z-20 play cursor-pointer w-12 md:w-24" src="../../assets/img/about/play.png" alt="">
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import Button from "../Button.vue";

export default {
    components:{
        Button,
    },
    data(){
        return {
            buttonText: 'Get Quote Now'
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

<style></style>
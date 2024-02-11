<template>
    <section class="mt-72 xl:mt-20 px-10 xl:px-40 mb-20">
        <div>
            <div class="text-center space-y-4">
                <h2 class="font-semibold text-md">VISIT OUR OFFICE</h2>
                <h1 class="font-bold text-4xl xl:w-2/5 mx-auto">We help small businesses with big ideas</h1>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 2xl:grid-cols-3 mt-20 gap-8 2xl:gap-0 2xl:px-44">
                <div class="space-y-5 px-2 py-20 shadow 2xl:shadow-none">
                    <div class="flex justify-center">
                        <img src="../../assets/img/icons/phone.png" alt="">
                    </div>
                    <div class="text-center space-y-2">
                        <p class="font-bold text-sm xl:text-xl">georgia.young@example.com</p>
                        <p class="font-bold text-sm xl:text-xl">georgia.young@ple.com</p>
                    </div>
                    <div>
                        <p class="text-center text-xl font-bold ">Get Support</p>
                    </div>
                    <div class="flex justify-center">
                        <a class="px-4 py-4 w-52 font-bold hover:bg-[#23A6F0] text-[#23A6F0] capitalize rounded-[200px] font-bold text-center  hover:text-white border border-[#23A6F0]"
                            href="#">Submit Request</a>
                    </div>
                </div>
                <div class="space-y-5 px-2 bg-[#252B42] py-20">
                    <div class="flex justify-center">
                        <img src="../../assets/img/icons/map.png" alt="">
                    </div>
                    <div class="text-center space-y-2 text-white">
                        <p class="font-bold text-sm xl:text-xl">georgia.young@example.com</p>
                        <p class="font-bold text-sm xl:text-xl">georgia.young@ple.com</p>
                    </div>
                    <div>
                        <p class="text-center text-xl font-bold text-white">Get Support</p>
                    </div>
                    <div class="flex justify-center">
                        <a class="px-4 py-4 w-52 font-bold hover:bg-[#23A6F0] text-[#23A6F0] capitalize rounded-[200px] font-bold text-center  hover:text-white border border-[#23A6F0]"
                            href="#">Submit Request</a>
                    </div>
                </div>
                <div class="space-y-5 px-2 py-20 shadow 2xl:shadow-none">
                    <div class="flex justify-center">
                        <img src="../../assets/img/icons/mail.png" alt="">
                    </div>
                    <div class="text-center space-y-2">
                        <p class="font-bold text-sm xl:text-xl">georgia.young@example.com</p>
                        <p class="font-bold text-sm xl:text-xl">georgia.young@ple.com</p>
                    </div>
                    <div>
                        <p class="text-center text-xl font-bold">Get Support</p>
                    </div>
                    <div class="flex justify-center">
                        <a class="px-4 py-4 w-52 font-bold hover:bg-[#23A6F0] text-[#23A6F0] capitalize rounded-[200px] font-bold text-center  hover:text-white border border-[#23A6F0]"
                            href="#">Submit Request</a>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex justify-center mt-20">
            <div class="space-y-8">
                <div class="flex justify-center">
                    <img class="arrow" src="../../assets/img/icons/arrow.png" alt="">
                </div>
                <div class="text-center space-y-8">
                    <p class="font-bold text-md">WE Can't WAIT TO MEET YOU</p>
                    <h2 class="font-bold text-6xl">Let’s Talk</h2>
                </div>
                <div class="flex justify-center">
                    <Button :buttonText="buttonText"></Button>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import Button from '../Button.vue';
export default {
    components: {
        Button
    },
    data() {
        return {
            buttonText: 'Try it free now'
        }
    },
    setup() {
        const { $gsap } = useNuxtApp()
        onMounted(() => {
             $gsap.from('.arrow', { scale: 1.05, yoyo: true, repeat: -1, y: 20, duration: 0.7 });
         });
    },
};

</script>
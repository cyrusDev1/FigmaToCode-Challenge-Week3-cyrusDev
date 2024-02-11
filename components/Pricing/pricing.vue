<template>
    <section class="mt-20 px-5 xl:px-20 py-20 bg-[#FAFAFA]">
        <div class="space-y-12">
            <div class="text-center space-y-4">
                <h2 class="text-4xl font-bold">Pricing</h2>
                <p class="xl:w-2/5 text-xl mx-auto"> Problems trying to resolve the conflict between
                    the two major realms of Classical physics: Newtonian mechanics </p>
            </div>

            <div class="flex items-center justify-center mt-10 space-x-4">
                <span class="text-base font-bold">Monthly</span>
                <button class="relative rounded-full focus:outline-none" x-cloak
                    @click="billPlan == 'monthly' ? billPlan = 'annually' : billPlan = 'monthly'">
                    <div
                        :class="{ 'w-12 h-6 transition border border-[#23A6F0] rounded-full outline-none': true, 'bg-indigo-500': billPlan == 'annually' }">
                    </div>
                    <div class="absolute inline-flex items-center justify-center w-4 h-4 transition-all duration-200 ease-in-out transform rounded-full shadow-sm top-1 left-1"
                        :class="{
                            'translate-x-0': billPlan == 'monthly', 'translate-x-6': billPlan == 'annually',
                            'bg-white': billPlan == 'annually', ' bg-[#D0D0D0]': billPlan == 'monthly'
                        }"></div>
                </button>
                <span class="text-base font-bold">Annually</span>
                <div class=" rounded-full font-semibold p-1 md:p-2 text-[#23A6F0] bg-[#B2E3FF]">
                    Save 25%
                </div>
            </div>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 lg:px-24 xl:px-28 2xl:px-96 mt-12 xl:mt-28 gap-4 lg:gap-0">
            <div class=" border border-[#23A6F0] rounded-lg py-16 h-[fit-content]">
                <div class="text-center space-y-6">
                    <h3 class="text-3xl font-bold text-[#252B42]">FREE</h3>
                    <p class="w-3/5 mx-auto text-md text-[#737373]">Organize across all
                        apps by hand</p>
                    <div class="text-center text-[#23A6F0]">
                        <div class="flex justify-center gap-2">
                            <div class="flex items-center">
                                <span class="font-bold text-4xl">0</span>
                            </div>
                            <div class="relative text-md">
                                <p class="text-left">$</p>
                                <p class="">Per Month</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="px-5 mt-5">
                    <ul class="space-y-4">
                        <li v-for="feature in features" class="flex gap-2 items-center relative">
                            <svg class="w-10 h-10 absolute" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                            :class="{'text-green-500': feature.available, 'text-gray-300': !feature.available, }"
                                viewBox="0 0 20 20" fill="currentColor">
                                <path fill-rule="evenodd"
                                    d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                                    clip-rule="evenodd" />
                            </svg>
                            <span class="text-[#252B42] text-md font-bold ml-12">{{ feature.text }}</span>
                        </li>
                    </ul>
                </div>
                <div class="mx-5 bg-[#252B42] text-center py-4 rounded-lg mt-5">
                    <a class="w-full text-white font-bold" href="">Try for free</a>
                </div>
            </div>

            <div class="bg-[#252B42] text-white border border-[#23A6F0] relative rounded-lg py-16 lg:py-20  lg:top-[-32px]">
                <div class="text-center space-y-6">
                    <h3 class="text-3xl font-bold text-white">STANDARD</h3>
                    <p class="w-3/5 mx-auto text-md text-white">Organize across all
                        apps by hand</p>
                    <div class="text-center text-[#23A6F0]">
                        <div class="flex justify-center gap-2">
                            <div class="flex items-center">
                                <span class="font-bold text-4xl"> {{ billPlan == 'monthly' ? '9.99' : ((9.99*12)*25)/100  }}</span>
                            </div>
                            <div class="relative text-md">
                                <p class="text-left">$</p>
                                <p class="">Per Month</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="px-5 mt-5">
                    <ul class="space-y-4">
                        <li v-for="feature in features" class="flex gap-2 items-center relative">
                            <svg class="w-10 h-10 absolute " aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                            :class="{'text-green-500': feature.available, 'text-gray-300': !feature.available, }"
                                viewBox="0 0 20 20" fill="currentColor">
                                <path fill-rule="evenodd"
                                    d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                                    clip-rule="evenodd" />
                            </svg>
                            <span class="text-white text-md font-bold ml-12">{{ feature.text }}</span>
                        </li>
                    </ul>
                </div>
                <div class="mx-5 bg-[#23A6F0] text-center py-4 rounded-lg mt-5">
                    <a class="w-full text-white font-bold" href="">Try for free</a>
                </div>
            </div>

            <div class=" border border-[#23A6F0] rounded-lg  py-16 h-[fit-content]">
                <div class="text-center space-y-6">
                    <h3 class="text-3xl font-bold text-[#252B42]">PREMIUM</h3>
                    <p class="w-3/5 mx-auto text-md text-[#737373]">Organize across all
                        apps by hand</p>
                    <div class="text-center text-[#23A6F0]">
                        <div class="flex justify-center gap-2">
                            <div class="flex items-center">
                                <span class="font-bold text-4xl"> {{ billPlan == 'monthly' ? '19.99' : ((19.99*12)*25)/100  }}</span>
                            </div>
                            <div class="relative text-md">
                                <p class="text-left">$</p>
                                <p class="">Per Month</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="px-5 mt-5">
                    <ul class="space-y-4">
                        <li v-for="feature in features" class="flex gap-2 items-center relative">
                            <svg class="w-10 h-10 absolute" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                            :class="{'text-green-500': feature.available, 'text-gray-300': !feature.available, }"
                                viewBox="0 0 20 20" fill="currentColor">
                                <path fill-rule="evenodd"
                                    d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                                    clip-rule="evenodd" />
                            </svg>
                            <span class="text-[#252B42] text-md font-bold ml-12">{{ feature.text }}</span>
                        </li>
                    </ul>
                </div>
                <div class="mx-5 bg-[#252B42] text-center py-4 rounded-lg mt-5">
                    <a class="w-full text-white font-bold" href="">Try for free</a>
                </div>
            </div>
        </div>
        <div class="mt-32 space-y-12">
            <div class="text-center space-y-4">
                <p class="text-xl mx-auto">Trusted By Over 4000 Big Companies </p>
            </div>
            <CustomersRow></CustomersRow>
        </div>
    </section>
</template>

<script>
import CustomersRow from '~/components/Customers/customersRow.vue'
export default {
    data() {
        return {
            billPlan: 'monthly',
            features: [
                {text: 'Unlimited product updates', available: true},
                {text: 'Unlimited product updates', available: true},
                {text: 'Unlimited product updates', available: true},
                {text: '1GB Cloud storage', available: false},
                {text: '1GB Cloud storage', available: false},
            ]
        }
    }
};

</script>

<style></style>

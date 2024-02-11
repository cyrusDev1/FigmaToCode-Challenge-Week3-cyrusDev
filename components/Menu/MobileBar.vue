<template>
    <nav class="px-8" :class="{'bg-[#F6F6F6]': showToggleMenu}">
        <div class="flex justify-between items-center">
            <div>
                <img src="../../assets/img/logo.png" alt="">
            </div>
            <div class="flex space-x-4 ">
                <img class="h-6 w-6" src="../../assets/img/icons/search.png" alt="">
                <img class="h-6 w-6" src="../../assets/img/icons/cart.png" alt="">
                <img v-if="!showToggleMenu" class="h-6 w-6" @click="openToggleMenu()" src="../../assets/img/icons/menu.png" alt="">
                <img v-if="showToggleMenu" class="h-6 w-6" @click="closeToggleMenu()" src="../../assets/img/icons/_menu.png" alt="">
            </div>
        </div>
        <transition name="fade" v-if="showToggleMenu">
            <div class="py-20 text-2xl">
                <ul class="space-y-8 text-center text-[#737373]">
                    <li><a class="hover:text-[#23A6F0] hover:font-bold" href="/">Home</a></li>
                    <li><a class="hover:text-[#23A6F0] hover:font-bold" href="/teams">Teams</a></li>
                    <li><a class="hover:text-[#23A6F0] hover:font-bold" href="/pricing">Pricing</a></li>
                    <li><a class="hover:text-[#23A6F0] hover:font-bold" href="/contact">Contact</a></li>
                </ul>
            </div>
        </transition>

    </nav>
</template>

<script>
export default {
    data() {
        return {
            showToggleMenu: false,
        };
    },
    methods: {
        openToggleMenu() {
            this.showToggleMenu = true;
        },
        closeToggleMenu() {
            this.showToggleMenu = false;
        },

    },
};
</script>
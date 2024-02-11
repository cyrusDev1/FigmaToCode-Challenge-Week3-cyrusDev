<template>
    <header class="">
        <Head>
            <Title>Bandage</Title>
        </Head>
        <NavBar :class="{ 'hidden lg:block': true }"></NavBar>
        <MobileBar :class="{ 'block lg:hidden': true }"></MobileBar>
    </header>
</template>

<script>
import MobileBar from '~/components/Menu/MobileBar.vue'
import NavBar from '~/components/Menu/NavBar.vue'


export default {
    components: {
        MobileBar,
        NavBar
    }
}
</script>
<style>
 .fade-enter-active, .fade-leave-active {
    transition: 0.5s;
}

 
.fade-leave-to{
  transform: translateY(-100%);
}
 
</style>
  
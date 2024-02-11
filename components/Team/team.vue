<template>
    <div>
        <div>
            <nuxt-img class="w-full"  :src="team.img" />
        </div>
        <div class="text-center space-y-3 mt-3">
            <h3 class="font-bold">{{ team.name }}</h3>
            <p>{{ team.role }}</p>
        </div>
        <div class="flex justify-center mt-3 mx-auto space-x-4">
            <img src="../../assets/img/icons/facebook.png" alt="">
            <img src="../../assets/img/icons/instagram.png" alt="">
            <img src="../../assets/img/icons/twitter.png" alt="">
        </div>
    </div>
</template>

<script>
export default {
    props: ['team'],
};

</script>

<style></style>
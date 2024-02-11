<template>
    <section class="mt-20 mx-10">
        <div class="text-center space-y-8">
            <h3 class="text-[#737373] text-sm font-bold">{{ dynamicText.subtitle }}</h3>
            <h2 class="text-4xl font-bold">{{ dynamicText.title }}</h2>
            <div class="flex gap-4 justify-center items-center">
                <h2 class="font-bold"><a href="/" class="hover:text-[#23A6F0]">Home</a></h2>
                <img class="w-3 h-3" src="../assets/img/icons/right.png" alt="">
                <h2 class="cursor-pointer">{{ dynamicText.active }}</h2>
            </div>
        </div>
    </section>
</template>

<script>
export default {
  props: {
    dynamicText: Object,
  },
};
</script>
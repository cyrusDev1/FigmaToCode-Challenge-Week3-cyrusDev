<template>
    <Header></Header>
    <main>
        <InnerHeader :dynamicText="dynamicText"></InnerHeader>
        <HeroPicture></HeroPicture>
        <section class="mt-28 mx-10 lg:mx-52">
            <div class="text-center space-y-4">
                <h2 class="text-4xl font-bold">Meet Our Team</h2>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 gap-12 mt-20">
                <div v-for="team in teams">
                    <Team :team="team"></Team>
                </div>
            </div>
        </section>
        <FreeTrial></FreeTrial>
    </main>
    <Footer></Footer>
</template>
    
<script>
import Header from '~/components/Menu/Header.vue'
import InnerHeader from '~/components/InnerHeader.vue'
import HeroPicture from '~/components/Team/hero-picture.vue'
import Team from '~/components/Team/team.vue'
import FreeTrial from '~/components/FreeTrial.vue'

import Footer from '~/components/Footer.vue'

export default {
    components: {
        Header,
        InnerHeader,
        Team,
        Footer,
        HeroPicture,
        FreeTrial
    },

    data() {
        return {
            dynamicText: {
                subtitle: 'WHAT WE DO',
                title: 'Innovation tailored for you',
                active: 'Teams',
            },
            teams: [
                {name: 'Username', role: 'profession', img: '../../_nuxt/assets/img/team/01.jpg'},
                {name: 'Username', role: 'profession', img: '../../_nuxt/assets/img/team/02.jpg'},
                {name: 'Username', role: 'profession', img: '../../_nuxt/assets/img/team/02.jpg'},
                {name: 'Username', role: 'profession', img: '../../_nuxt/assets/img/team/03.jpg'},
                {name: 'Username', role: 'profession', img: '../../_nuxt/assets/img/team/04.jpg'},
                {name: 'Username', role: 'profession', img: '../../_nuxt/assets/img/team/05.jpg'},
                {name: 'Username', role: 'profession', img: '../../_nuxt/assets/img/team/06.jpg'},
                {name: 'Username', role: 'profession', img: '../../_nuxt/assets/img/team/07.jpg'},
                {name: 'Username', role: 'profession', img: '../../_nuxt/assets/img/team/08.jpg'}
            ]
        };
    },
}
</script>

<style>
body {
}
</style>
    
    
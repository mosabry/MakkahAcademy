<template>
    <v-container class="teal--text darken-3">
        <v-row justify="center">
            <Logo />
        </v-row>
        <SocialVue />
    </v-container>
</template>

<script>
import SocialVue from '@/components/Social.vue'
import Logo from '../components/Logo.vue';
export default {
    name: 'ContactPage',
    components: { SocialVue, Logo }
}
</script>

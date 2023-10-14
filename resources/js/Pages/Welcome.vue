<script setup>
import { Head, Link } from '@inertiajs/vue3';
import Information from '@/Components/Information.vue';
import Hero from '@/Components/Hero.vue';

defineProps({
    canLogin: {
        type: Boolean,
    },
    canRegister: {
        type: Boolean,
    },
    laravelVersion: {
        type: String,
        required: true,
    },
    phpVersion: {
        type: String,
        required: true,
    },
});

</script>

<template>
    <Head title="Welcome" />

    <nav>
        <div v-if="canLogin" class="sm:fixed sm:top-0 sm:right-0 p-6 text-right">
            <Link v-if="$page.props.auth.user" :href="route('dashboard')"
                class="menu-link font-semibold hover:text-gray-900 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500">
            Dashboard</Link>

            <template v-else>
                <Link :href="route('login')"
                    class="menu-link font-semibold hover:text-gray-900 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500">
                Log in</Link>

                <Link v-if="canRegister" :href="route('register')"
                    class="menu-link ml-4 font-semibold hover:text-gray-900 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500">
                Register</Link>
            </template>
        </div>
    </nav>

    <Hero />
    <main>
        <Information>
            <template v-slot:heading>
                <h1>Welkom bij KlantConnect</h1>
            </template>
            <template v-slot:text>
                <p>In de dynamische wereld van vandaag is het essentieel om niet alleen bij te blijven met uw afspraken,
                    maar ook om een diepgaand inzicht te hebben in uw klanten.
                    Hier komt KlantConnect in beeld.</p>
            </template>
            <template v-slot:image>
                <img src="images/information-img/Men-talking-amico.svg" alt="Aangepaste afbeelding">
            </template>
            <template v-slot:source>
                <a href="https://storyset.com/people">People illustrations by Storyset</a>
            </template>
        </Information>
    </main>
</template>

<style>
nav {
    height: 20vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

main {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    width: 100vw;
}

@media (prefers-color-scheme: dark) {}
</style>

<script>

export default {
    components: {
        Information
    }
}
</script>

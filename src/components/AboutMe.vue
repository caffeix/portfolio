<script setup lang="ts">
    import type { Profile } from "@/types/profile";
    import DownloadCvButton from "./DownloadCvButton.vue";

    defineProps<{ profile: Profile }>();
</script>

<template>
    <section class="hero-section">
        <section class="bio">
            <h1>{{ profile.name }}</h1>
            <h2>{{ profile.title }}</h2>
            <h3>{{ profile.subtitle }}</h3>
            <p>{{ profile.description }}</p>
            <DownloadCvButton :profile="profile" />
        </section>
        <img :src="profile.portraitUrl" alt="Profile Picture" width="400" />
    </section>
</template>

<style scoped>
    h1 {
        font-size: 2.5em;
        margin-bottom: 0.5em;
    }
    h2 {
        font-size: 1.5em;
        font-weight: 100;
        margin-bottom: 0.5em;
    }
    p {
        font-size: 1.2em;
        line-height: 1.5;
        margin-bottom: 1em;
    }

    .bio {
        flex: 1 1 0;
        max-width: 60%;
    }

    .hero-section {
        max-width: 80vw;
        min-height: 50vh;
        padding: 5rem;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        gap: 2rem;
    }
    .hero-section img {
        flex: 0 0 auto;
        max-width: 40%;
        height: auto;
        border-radius: 0.6rem;
    }

    @media (max-width: 820px) {
        .hero-section {
            flex-direction: column;
            align-items: flex-start;
        }

        .hero-section img {
            max-width: 100%;
            margin-top: 1.5rem;
            margin: 0 auto;
        }

        .bio {
            max-width: 100%;
            margin: 0 auto;
        }
    }
</style>
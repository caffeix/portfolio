<script setup lang="ts">
  import type { Profile } from "@/types/profile";

  defineProps<{ profile: Profile }>();
</script>

<template>
  <a :href="profile.cvUrl" download>
    <button>Download CV</button>
  </a>
</template>

<style scoped>
    button {
        padding: 0.5rem 1rem;
        font-size: 1em;
        font-family: var(--text-font);
        background-color: var(--primary);
        color: var(--text-on-primary);
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        font-weight: 600;
        border: none;
        border-radius: 0.2em;
        cursor: pointer;
    }
    button:hover {
        background-color: var(--primary-light);
    }
    /* Show a clear focus ring for keyboard users */
    button:focus-visible,
    button:focus {
      outline: 2px solid var(--focus);
      outline-offset: 0px;
    }

    button:active {
    transform: translateY(1px);
    box-shadow: inset 0 2px 6px rgba(0, 0, 0, 0.15);
    }
</style>
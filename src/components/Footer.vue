<script setup lang="ts"></script>

<template>
  <footer>
    <p>&copy; 2026 Margarita Fedulova. All rights reserved.</p>
  </footer>
</template>

<style scoped>
  footer {
    position: fixed;
    left: 0;
    bottom: 0;
    width: 100%;
    text-align: center;
    background-color: var(--background-color-footer);
    color: var(--text-light);
    z-index: 100;
    padding: 0 0;
    font-size: clamp(0.75rem, 1.1vw, 0.9rem);
  }

  @media (max-width: 600px) {
    footer {
      position: sticky;
      padding: 0.1rem 0;
    }
  }
</style>
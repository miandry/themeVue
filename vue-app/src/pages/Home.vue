<template>
  <div>
    <h2>📰 Articles injectés depuis Drupal</h2>
    <ul>
      <li v-for="a in articles" :key="a.id">
        {{ a.title }} <small>({{ a.created }})</small>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from 'vue'

// On lit les données injectées par Drupal
const articles = ref(window.drupalSettings?.vueArticles || [])
</script>

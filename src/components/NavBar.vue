<script lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <nav>
    <ul>
      <li>
        <RouterLink :to="{ name: 'login' }">TodoList</RouterLink>
      </li>
    </ul>
  </nav>
</template>
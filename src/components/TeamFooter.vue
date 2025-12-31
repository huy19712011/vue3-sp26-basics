<script setup>
defineProps({
  team: Object,
});
</script>
<template>
  <footer>
    <h5>{{ team.name }} - {{ team.spots }} member Team</h5>
  </footer>
</template>

<script setup>
import { useTeamStore } from "@/stores/TeamStore";

let team = useTeamStore();
</script>
<template>
  <footer>
    <h5>{{ team.name }} - {{ team.spots }} member Team</h5>
  </footer>
</template>

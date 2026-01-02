<script setup>
import { useTeamStore } from "@/stores/TeamStore";

let team = useTeamStore();
</script>
<template>
  <header>
    <div>
      <button :disabled="!team.spotsRemaining">
        Add Member ({{ team.spotsRemaining }} Spots Left)
      </button>
    </div>
    <div>
      <h3>
        {{ team.name }}
        <div>{{ team.spots }}</div>
      </h3>
    </div>
  </header>
</template>

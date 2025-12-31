<script setup>
defineProps({
  team: Object,
});
</script>
<template>
  <header>
    <div>
      <button :disabled="team.members.length === team.spots">
        Add Member ({{ team.spots - team.members.length }} Spots Left)
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

<script setup>
import TeamFooter from "@/components/TeamFooter.vue";
import TeamHeader from "@/components/Teams/TeamHeader.vue";
import TeamMembers from "@/components/Teams/TeamMembers.vue";
import team from "@/team.json";
console.log(team);
</script>

<template>
  <TeamHeader :team="team" />
  <div>
    <TeamMembers :team="team" />
    <p v-show="team.members.length === team.spots">
      There are no remaining team spots. Upgrade to add more.
    </p>
  </div>
  <TeamFooter :team="team" />
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1.5rem;
}

header button {
  min-width: 180px;
}

header h3 {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin: 0;
}

header h3 div {
  background: #0d6efd;
  color: #fff;
  border-radius: 50%;
  width: 2.2rem;
  height: 2.2rem;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
}

table {
  width: 100%;
  margin-bottom: 1rem;
}

th,
td {
  text-align: left;
  padding: 0.75rem;
  vertical-align: middle;
}

thead {
  background: #f8f9fa;
}

tbody tr:nth-child(even) {
  background: #f2f2f2;
}

button {
  border: none;
  padding: 0.5rem 1rem;
  border-radius: 0.3rem;
  background: #0d6efd;
  color: #fff;
  cursor: pointer;
}

button:disabled {
  background: #adb5bd;
  cursor: not-allowed;
}

footer {
  margin-top: 2rem;
  text-align: center;
  color: #6c757d;
}
</style>

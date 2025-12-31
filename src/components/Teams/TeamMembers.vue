<script setup>
import TeamMember from "./TeamMember.vue";
defineProps({
  team: Object,
});
</script>
<template>
  <table>
    <thead>
      <tr>
        <th>Name</th>
        <th>Email</th>
        <th>Status</th>
      </tr>
    </thead>
    <tbody>
      <TeamMember
        v-for="member in team.members"
        :name="member.name"
        :email="member.email"
        :status="member.status"
      />
    </tbody>
  </table>
</template>

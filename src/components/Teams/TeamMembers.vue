<script setup>
import TeamMember from "./TeamMember.vue";
import { useTeamStore } from "@/stores/TeamStore";

let team = useTeamStore();
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
  <p v-show="!team.spotsRemaining">There are no remaining team spots. Upgrade to add more.</p>
</template>

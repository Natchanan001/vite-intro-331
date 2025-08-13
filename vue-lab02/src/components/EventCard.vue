<script setup lang="ts">
import { type Event } from '@/types';
 defineProps<{
  event: Event;
}>();
</script>
<template>
    <routerLink class="event-link" :to="{ name: 'event-detail-view', params: { id: event.id } }">
    <div class="cursor-pointer border border-gray-600 p-4 w-64 mb-6 hover:scale-101 hover:shadow-sp">
      <h2>{{ event.title }}</h2>
      <span>@{{ event.time }} on {{ event.date }}</span>
    </div>
  </routerLink>
</template>

<style scoped>
/* Removed .event-card and .event-card:hover as per instructions. Now use Tailwind classes. */

.event-link {
  text-decoration: none;
  color: #2c3e50;
}
</style>

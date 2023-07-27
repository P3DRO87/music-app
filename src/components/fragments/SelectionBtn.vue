<script setup>
import { defineProps } from "vue";

defineProps({
   btnText: String,
});
</script>

<template>
   <button class="type-selection">
      <span>{{ btnText }}</span> <i class="fa-solid fa-angle-up me-1"></i>
   </button>
</template>

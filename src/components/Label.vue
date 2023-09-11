<script setup>
const props = defineProps({
  for: String,
  required: Boolean,
});
</script>

<template>
  <label :for="props.for" class="font-bold text-sm"
    ><slot /> <span v-if="props.required" class="text-red-500">*</span></label
  >
</template>

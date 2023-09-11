<script setup>
const props = defineProps({
  id: String,
  required: Boolean,
  invalid: Boolean,
  ariaDescribedBy: String,
  modelValue: [String, Number],
});

const emit = defineEmits(['updated:modelValue']);
</script>

<template>
  <input
    :id="props.id"
    :value="props.modelValue"
    :required="props.invalid"
    @input="($event) => emit('updated:modelValue', $event.target.value)"
    class="w-full border rounded-sm text-sm px-2.5 py-1.5"
    :class="[
      'w-full rounded-md shadow-sm focus:border-green-500 focus:ring-green-500',
      props.invalid ? 'border-red-500' : 'border-gray-300',
    ]"
  />
</template>

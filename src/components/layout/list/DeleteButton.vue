<template>
  <button
    :class="[
      'text-red-600 hover:text-red-900',
      disabled ? 'text-gray-400 cursor-not-allowed' : 'hover:text-red-900',
    ]"
    :title="tooltip || 'Delete'"
    :disabled="disabled"
    @click="!disabled && $emit('click')"
  >
    <svg class="h-4 w-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"
      ></path>
    </svg>
  </button>
</template>

<script setup lang="ts">
  defineProps<{
    disabled?: boolean
    tooltip?: string
  }>()

  defineEmits<{
    click: []
  }>()
</script>

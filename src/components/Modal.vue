<template>
  <div 
    v-show="modelValue" 
    class="fixed inset-0 bg-black bg-opacity-50 flex justify-center items-center z-50"
    :aria-hidden="!modelValue.toString()"
    role="dialog"
    aria-modal="true"
    aria-labelledby="modalTitle"
    tabindex="-1">
    
    <div class="bg-white p-8 rounded-lg shadow-lg max-w-md w-full">
      <div class="bg-amber-100 shadow-md rounded px-8 pt-6 pb-8 mb-4">
        <div class="flex justify-end">
          <i @click="closeModal" class="fa-solid fa-xmark text-4xl ml-auto text-red-400" aria-label="Close modal"></i>
        </div>
        <!-- Slot for Modal content -->
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps, defineEmits } from 'vue';

const props = defineProps({
  modelValue: Boolean // Accepting isOpen as a prop with a more v-model friendly name
});
const emit = defineEmits(['update:modelValue']);

function closeModal() {
  emit('update:modelValue', false); // Notify parent to change the prop's value
}
</script>

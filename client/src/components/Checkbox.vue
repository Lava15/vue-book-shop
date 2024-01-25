<script setup>
defineProps({
  label: String,
  required: Boolean,
  name: String,
  value: Boolean,
})
</script>

<template>
  <div class="flex items-center">
    <label :for="name" class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300">I agree with the <a
        href="#" class="text-blue-600 dark:text-blue-500 hover:underline">{{ label }}</a>.</label>
    <input :id="name"
           type="checkbox"
           :name="name"
           :value="value"
           :required="required"
           class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600">
  </div>
</template>

<style scoped>

</style>
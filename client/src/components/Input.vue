<script setup>
defineProps({
  name: String,
  type: String,
  label: String,
  placeholder: String,
  requred: String,
  min: String,
  max: String,
  value: String
})
</script>

<template>
  <label :for="name" class="block text-sm font-medium leading-6 text-gray-900">{{ label }}</label>

  <input
      :type="type"
      :name="name"
      :requred="requred"
      :min="min"
      :max="max"
      :value="value"
      id="message-input"

      class="block w-full rounded-md border-0 py-1.5 pl-7 pr-20 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
      :placeholder="placeholder">

</template>

<style scoped>

</style>
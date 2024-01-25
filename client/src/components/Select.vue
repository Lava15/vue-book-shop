<script setup>

defineProps({
  items: Array,
  name: String,
  required: Boolean,
  label: String
})

</script>

<template>
  <div class="max-w-2xl mx-auto">
    <label
        :for="name"
        class="block mb-2 text-sm font-medium text-gray-900 dark:text-gray-400">{{ label }}</label>
    <select :id="name"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-indigo-500 focus:border-indigo-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-indigo-500 dark:focus:border-indigo-500"
            name="name"
            :required="required"
    >
      <option v-for="option in items" :value="option.value">{{ option.text }}</option>
    </select>
  </div>
</template>

<style scoped>

</style>
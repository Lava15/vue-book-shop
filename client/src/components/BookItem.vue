<script setup>
import {TrashIcon} from "@heroicons/vue/24/solid/index.js";

const props = defineProps({
  book: Object
});
const emits = defineEmits(['removeBook'])

function triggerRemove() {
  emits('removeBook', props.book.id)
}
</script>

<template>

  <li class="flex flex-col items-center mt-5 bg-white border border-gray-200 rounded-lg shadow md:flex-row md:max-w-xl hover:bg-gray-100 dark:border-gray-700 dark:bg-gray-800 dark:hover:bg-gray-700">
    <img class="object-cover w-full rounded-t-lg h-96 md:h-auto md:w-48 md:rounded-none md:rounded-s-lg"
         src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fedit.org%2Fimages%2Fcat%2Fbook-covers-big-2019101610.jpg&f=1&nofb=1&ipt=2a01c736152ca3e75604669b308e6c8b71066054ad1dfc1b41d494d79e7533ce&ipo=images"
         alt=""
    >
    <div class="flex flex-col justify-between p-4 leading-normal">
      <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
        {{ book.title }}
      </h5>
      <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
        {{ book.authors[0].name }}
      </p>
    </div>
    <button class="p-10 self-end" @click="triggerRemove">
      <TrashIcon class="h-6 w-6 text-red-500 hover:text-red-700"/>
    </button>
  </li>

</template>

<style scoped>

</style>
<script setup>
import {onMounted, ref} from "vue";
import BookItem from "@/components/BookItem.vue";

const books = ref([]);

function removeBook(id) {
  books.value = books.value.filter((book) => book.id !== id)
}

onMounted(() => {
  fetch("https://gutendex.com/books/")
      .then(response => response.json())
      .then(data => {
        books.value = data.results;
      })
})
</script>

<template>
  <div class="container mx-auto">
    <h2 class="mt-5 text-5xl font-bold text-teal-500 text-center">Books {{ books.length }} </h2>
    <ul class="grid lg:grid-cols-2">
      <BookItem
          v-for="book in books"
          :book="book"
          :id="book.id"
          :key="book.id"
          @removeBook="removeBook"
      />
    </ul>
  </div>
</template>

<style scoped>

</style>
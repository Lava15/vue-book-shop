<script setup>
import {  RouterView } from 'vue-router'
let data = {
  message: "Demo"
}

</script>

<template>
  <div class="text-5xl text-center mt-10">
  {{ data.message }}
  </div>
  <RouterView />
</template>


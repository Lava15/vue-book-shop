<script setup>

import Input from "@/components/Input.vue";
import Select from "@/components/Select.vue";
import {items}  from "../data.js"
import Checkbox from "@/components/Checkbox.vue";

function submitForm() {
  console.log('Submit')
}
</script>

<template>
  <div class="flex min-h-full flex-col justify-center px-6 py-12 lg:px-8">
    <div class="sm:mx-auto sm:w-full sm:max-w-sm">
      <img class="mx-auto h-10 w-auto" src="https://tailwindui.com/img/logos/mark.svg?color=indigo&shade=600"
           alt="Your Company">
      <h2 class="mt-10 text-center text-2xl font-bold leading-9 tracking-tight text-gray-900">Register an account</h2>
    </div>

    <div class="mt-10 sm:mx-auto sm:w-full sm:max-w-sm">
      <form
          @submit="submitForm"
          autocomplete="off"
          class="space-y-6"
          method="POST"
      >
        <div>
          <div class="mt-2">
            <Input
                label="First name"
                type="text"
                name="first-name"
            />
          </div>
        </div>

        <div>
          <div class="mt-2">
            <Input
                label="Last name"
                type="text"
                name="last-name"
            />
          </div>
        </div>

        <div>
          <div class="mt-2">
            <Input
                label="Password"
                type="password"
                name="password"
            />
          </div>
        </div>

        <div>
          <div class="mt-2">
            <Input
                label="E-mail"
                type="email"
                name="email"
            />
          </div>

          <div>
            <div class="mt-2">
              <Select label="Favourite Color" name="color" :items="items"/>
            </div>
          </div>

          <div>
            <div class="mt-2">
              <Checkbox label="Favourite Color" name="color" items="data"/>
            </div>
          </div>

          <div class="flex mt-5 items-center justify-between">
            <div class="text-sm">
              <a href="#" class="font-semibold text-indigo-600 hover:text-indigo-500">Forgot password?</a>
            </div>
          </div>
        </div>

        <div>
          <button
              type="submit"
              class="flex w-full justify-center rounded-md bg-indigo-600 px-3 py-1.5 text-sm font-semibold leading-6 text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">
            Register
          </button>
        </div>
      </form>
    </div>
  </div>

</template>

<style scoped>

</style>
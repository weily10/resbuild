<script setup lang="ts">
import Resume from "../components/Resume.vue";
import { ref } from "vue";
import Data from "../global/types";

const data = ref<Data>({
  name: "",
  expertise: "",
});
</script>

<template>
  <div>
    <div
      class="fixed top-0 left-0 right-0 bg-white h-[70px] p-6 mb-6 z-50 border-b border-gray-300"
    >
      <div class="flex space-x-6">
        <div class="font-extrabold primary-text box">MyRes</div>
        <div class="box">Preview</div>
        <div class="box">Download</div>
      </div>
    </div>
    <div class="flex justify-center">
      <Resume :data="data"></Resume>
      <div class="bg-gray-100 p-6 fixed h-full right-0 mt-16 space-y-3">
        <label class="relative block">
          <span>Name</span>
          <span class="absolute inset-y-0 left-0 flex items-center pl-2">
            <svg class="h-5 w-5 fill-slate-300" viewBox="0 0 20 20"></svg>
          </span>
          <input
            v-model="data.name"
            class="mt-2 placeholder:italic placeholder:text-slate-400 block bg-white w-full border border-slate-300 rounded-md py-2 pl-9 pr-3 shadow-sm focus:outline-none focus:border-sky-500 focus:ring-sky-500 focus:ring-1 sm:text-sm"
            placeholder="Name"
            type="text"
            name="search"
          />
        </label>
        <label class="relative block">
          <span>Expertise</span>
          <span class="absolute inset-y-0 left-0 flex items-center pl-2">
            <svg class="h-5 w-5 fill-slate-300" viewBox="0 0 20 20"></svg>
          </span>
          <input
            v-model="data.expertise"
            class="mt-2 placeholder:italic placeholder:text-slate-400 block bg-white w-full border border-slate-300 rounded-md py-2 pl-9 pr-3 shadow-sm focus:outline-none focus:border-sky-500 focus:ring-sky-500 focus:ring-1 sm:text-sm"
            placeholder="Ex: Sales"
            type="text"
            name="search"
          />
        </label>
      </div>
    </div>
  </div>
</template>

<style scoped>
.box:first-child {
  @apply mr-auto;
}
</style>

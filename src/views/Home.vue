<script setup lang="ts">
import Resume from "../components/Resume.vue";
import { ref } from "vue";
import Data from "../global/types";

const data = ref<Data>({
  name: "",
  expertise: "",
  desc: "",
  location: "",
});
</script>

<template>
  <div>
    <div
      class="fixed top-0 left-0 right-0 bg-white h-[70px] p-6 mb-6 z-50 border-b border-gray-300"
    >
      <div class="flex space-x-6">
        <div class="font-extrabold primary-text box">MyRes</div>
        <div class="box">Save</div>
        <div class="box">Preview</div>
        <div class="box">Download</div>
      </div>
    </div>
    <div class="flex justify-center">
      <Resume :data="data"></Resume>
      <div class="bg-gray-100 p-6 fixed h-full right-0 mt-16 space-y-3 w-80">
        <label class="relative block">
          <span>Name</span>
          <span class="absolute inset-y-0 left-0 flex items-center pl-2">
            <svg class="h-5 w-5 fill-slate-300" viewBox="0 0 20 20"></svg>
          </span>
          <input
            v-model="data.name"
            class="mt-2 placeholder:italic placeholder:text-slate-400 block bg-white w-full border border-slate-300 rounded-md py-2 pl-9 pr-3 shadow-sm focus:outline-none focus:border-sky-500 focus:ring-sky-500 focus:ring-1 sm:text-sm"
            placeholder="e.g., Adam Smith"
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
            placeholder="e.g., Sales"
            type="text"
            name="search"
          />
        </label>
        <label class="relative block space-y-3">
          <span>Location</span>
          <span class="absolute inset-y-0 left-0 flex items-center pl-2">
            <svg class="h-5 w-5 fill-slate-300" viewBox="0 0 20 20"></svg>
          </span>
          <input
            v-model="data.location"
            class="mt-2 placeholder:italic placeholder:text-slate-400 block bg-white w-full border border-slate-300 rounded-md py-2 pl-9 pr-3 shadow-sm focus:outline-none focus:border-sky-500 focus:ring-sky-500 focus:ring-1 sm:text-sm"
            placeholder="e.g., Paris, France"
            type="text"
            name="search"
          />
        </label>
        <label class="relative block space-y-3">
          <p>Brief Description</p>
          <textarea
            placeholder="e.g., Highly driven individual with excellent leadership skills and six years of retail sales management experience, looking for the position of Senior Manager. Bringing exceptional communication skills to inspire and strong business skills to provide superior service."
            name="message"
            rows="10"
            cols="26"
            v-model="data.desc"
            class="bg-white p-6 placeholder:italic"
          >
          </textarea>
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

<script setup lang="ts">
import { PropType } from "vue";
import Data from "../global/types";
defineProps({
  data: Object as PropType<Data>,
});
</script>

<template>
  <div class="">
    <div class="m-auto mt-24 flex justify-center">
      <div
        id="template"
        class="w-[210mm] h-[297mm] drop-shadow-2xl bg-white border-x-cyan-950 p-12 m-6"
      >
        <div class="grid grid-rows-2 grid-flow-col grid-cols-2">
          <div class="h-12">
            <p class="text-2xl font-semibold">
              {{ data.name }}
            </p>
            <p class="mt-2">{{ data.expertise }}</p>
            <p>{{ data.location }}</p>
          </div>

          <div class="row-span-2 col-start-2">
            {{ data.desc }}
          </div>
        </div>

        <div class="mt-3 text-xl font-bold">Work Experience</div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>

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
        <div class="grid grid-cols-2 gap-4">
          <div>
            <p class="text-2xl font-semibold">
              {{ data.name }}
            </p>
            <p class="">
              {{ data.expertise }}
            </p>
            <p class="">
              {{ data.location }}
            </p>
          </div>
          <div class="ml-6">
            <div>
              {{ data.desc }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>

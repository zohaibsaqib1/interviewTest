<script setup lang="ts">
import { ref, defineProps } from 'vue';

const props = defineProps({
  productInfo: {
    type: Object,
    required: true,
  },
});

</script>

<template>
  <div class="bg-white h-[20vh] w-[100vw]">
  </div>
  <div class="bg-green-400 h-[60vh] flex justify-center py-8">
    <div class="bg-white h-[50vh] w-[40vw] text-black font-extrabold flex justify-center">
      <div>
        {{ productInfo.title }}
        <div class="font-light text-xs">
          COD: {{ productInfo.COD }}
        </div>
        <div class="flex text-color-red-600">
          <div class="font-light text-lg">{{ productInfo.currency }}</div>
          <div class="font-normal text-5 pl-3">{{ productInfo.price }}</div>
        </div>
        <div>
        </div>
        <div class="font-normal pt-4">
          Select A Color
          <div class="flex font-normal">
            <div v-for="color in productInfo.color" class="flex items-center h-8 w-8 border border-black">
              {{ color.text }}
            </div>
          </div>
        </div>
        <div class="pt-4 font-normal text-xs pb-2">
          Benefits
          <ul>
            <li v-for="benefit in productInfo.benefits" class="font-normal list-disc">
              {{ benefit.text }}
            </li>
          </ul>
        </div>
        <button class="bg-red-500 text-white py-2 px-4 font-normal rounded ">
          Add to Cart
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped>
</style>

<script setup lang="ts">
const productInfo = ref({   
    title: 'Delicious Apples',
    currency: 'R$',
    price: 7.93,
    benefits: [
        {
            id: '1',
            text: 'test',
        },
        {
            id: '2',
            text: 'test',
        },
        {
            id: '3',
            text: 'test',
        }
    ],
    color: [
        {
            id: '1',
            text: 'test',
        },
        {
            id: '2',
            text: 'test',
        },
        {
            id: '3',
            text: 'test',
        }
    ],
    image: 'test',
    images: [
        {
            id: '1',
            text: 'test',
        },
        {
            id: '2',
            text: 'test',
        },
        {
            id: '3',
            text: 'test',
        }
    ],
    category: 'test',
    id: 'test',
    COD:'12345',
    rating: 5,
    hasPrime: true,
    });


</script>

<template>
  <div class="bg-white h-[20vh] w-[100vw]">
    
  </div>
  <div class ="bg-green-400 h-[60vh] flex justify-center py-8">
      <div class="bg-white h-[50vh] w-[40vw] text-black font-extrabold flex justify-center">
        <div>
            {{productInfo.title}}
        <div class = 'font-light text-xs'>
           COD: {{ productInfo.COD }}
        </div>
        <div>
            
        </div>
        <div class="font-normal pt-4">
            Select A Color
            <div class="flex font-normal">
                <div v-for="color in productInfo.color" class="flex items-center h-8 w-8 border border-black">
                    {{color.text}}
                </div>
            </div>
        </div>
        <div class="pt-4 font-normal">
            Benefits
            <ul>
            <li v-for="benefit in productInfo.benefits" class="font-normal list-disc ">
            {{benefit.text}}
            </li>
            </ul>
        </div>
        </div>
      </div>
</div>
</template>

<style scoped>
    
</style>
```

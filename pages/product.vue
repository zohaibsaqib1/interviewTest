<template>
    <div>
      <ProductCard :productInfo="appleProductInfo" />
    </div>
  </template>
  
  <script>
import ProductCard from '../components/ProductCard.vue';
  
  export default {
    components: {
      ProductCard,
    },
    data() {
      return {
        appleProductInfo: {
          title: 'Delicious Apples',
          currency: 'R$',
          price: 7.93,
          benefits: [
            { id: '1', text: 'Apples are nutritious' },
            { id: '2', text: 'Apples may be good for weight loss' },
            { id: '3', text: 'Apples may be good for bone' },
          ],
        },
      };
    },
  };
  </script>
  
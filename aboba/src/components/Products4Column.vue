<template>
    <div class="products-container">
      <div class="products">
        <Product
            v-for="product of products"
            :key="product.id"
            :img="product.img"
            :title="product.title"
            :price="product.price"/>
      </div >
      <a href="#" class="products-link">View collection</a>
    </div >
</template>    

<script setup>
import {ref} from 'vue'
import Product from '@/components/Product.vue'


const products = ref ([
  {
    id: 1,
    img: '/img/Product-1.jpg',
    title: 'The Dandy chair',
    price: 250
  },
  {
    id: 2,
    img: '/img/Product-2.jpg',
    title: 'Rustic Vase Set',
    price: 155
  },
  {
    id: 3,
    img: '/img/Product-3.jpg',
    title: 'The Silky Vase',
    price: 125
  },
  {
    id: 4,
    img: '/img/Product-4.jpg',
    title: 'The Lucy Lamp',
    price: 399
  }
])
 
</script>

<style lang="scss" scoped>
.products {
  padding:0 80px ;
  display: flex;
  grid-template-columns: repeat(4, 1fr);
  column-gap: 20px;
  margin-bottom:64px;
  &-container{
    margin-bottom: 56px;
  }
  &-link{
    display: block;
    text-align: center;
    color: var(--black);
    text-decoration: none;
    &:hover{
      text-decoration: underline;
    }
  }
}
</style>
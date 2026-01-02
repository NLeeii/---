<script setup>
import { ref } from 'vue'
import ProductCard from '../components/ProductCard.vue'
import fishOilImg from '@/assets/images/08.jpg' // 測試用
</script>

<template>
  <div class="mall-page">
    <h1>UniCare 樂活商城</h1>
    <p>這裡是商城</p>
    <button class="test-btn">測試按鈕</button>
  </div>
  <div class="test-area">
    <h3>商品卡片</h3>

    <ProductCard 
    :image="fishOilImg" title="頂級深海rTG魚油" spec="60錠/瓶" :price="1280" />

  </div>
</template>

<style lang="scss" scoped>
.mall-page {
  padding: 20px;

  h1 {
    // color: $primary-dark;
    font-size: 30px;
  }

  .test-btn {
    // background-color: $orange;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 8px;
  }
}

.test-area {
  padding: 50px;
  margin-bottom: 100px;
  width: 400px; /* 先限制一個寬度，模擬它在網格裡的樣子 */
  margin: 0 auto;
  background-color: #f0f0f0; /* 給個背景色比較好分辨 */
}
</style>
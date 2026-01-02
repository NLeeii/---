<script setup>
defineProps({
  id: Number,
  image: String,
  title: String,
  spec: String, // 規格
  price: Number
})
</script>
<template>
  <div class="product_card">
    <div class="card_img">
      <img v-if="image" :src="image" :alt="title">
      <div v-else>尚無圖片</div>
      <div class="product_tag">熱銷</div>
    </div>

    <div class="card_body">
      <h3 class="product_title">{{ title }}</h3>
      <p class="product_price">${{ price }}</p>
      <div class="card_button">
        <a href="#">加入購物車</a>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.product_card {
  box-shadow: 0 4px 10px rgba(0, 0, 0, .25);
  border-radius: 10px 10px 0 0;

  .card_img {
    width: 100%;
    position: relative;

    img {
      border-radius: 10px 10px 0 0;
      display: block;
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .product_tag {
      position: absolute;
      left: 12px;
      top: 12px;
      padding: 5px 16px;
      background-color: $accent;
      color: $white;
      @include body3;
      border-radius: 5px;
    }
  }

  .card_body {
    padding: 24px;
    display: flex;
    flex-direction: column;
    gap: 16px;
    flex: 1;
    background-color: $white;
    border-radius: 0 0 10px 10px;

    .product_title {
      @include subtitle2(true);
      color: $primaryDark;
    }

    .product_price {
      @include body1(true);
    }

    .card_button {
      background-color: $primaryDark;
      color: $white;
      @include body2(true);
      text-align: center;
      border-radius: 5px;
      transition: all .3s;

      a {
        display: block;
        padding: 8px;
      }

      &:hover {
        background-color: $primary;
      }
    }
  }
}
</style>
<script setup>
//import { Swiper, SwiperSlide } from 'swiper/vue';
//import 'swiper/css';

const props = defineProps({
  picture: String,
  title: String,
  period: String,
  price: String,
  rating: String,
  badge: String,
})

const likebtn = () => {
}

</script>
<template>
  <div class="slide-item">
    <div class="item-img">
      <img :src="props.picture" />
    </div>
    <ul class="item-info">
      <li class="item-location">
        {{ props.title }}
      </li>
      <li class="item-date">
        {{ props.period }}
      </li>
      <li class="">
        <span class="item-period">
          {{ props.price }}
        </span>
        <span class="item-rating">
          <font-awesome-icon :icon="['fas', 'star']" />
          {{ props.rating }}
        </span>
      </li>
    </ul>
    <div class="item-icon">
      <span v-if="props.badge" class="icon-cate">
        {{ props.badge }}
      </span>
      <span class="icon-heart">
        <font-awesome-icon :icon="['far', 'heart']" @click="likebtn()" />
      </span>
    </div>
  </div>
</template>
<style lang="scss">

.slide-item {
  position: relative;
  .item-img {
    border-radius: 20px;
    overflow: hidden;
    aspect-ratio: 1 / 1;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }
  .item-info {
    padding: 7px 5px;
    display: flex;
    flex-direction: column;
    gap: 5px;
    li {
      color: #999;
      font-size: 0.9em;
      &.item-location {
        font-size: 1em;
        font-weight: 500;
        color: #000;
      }
      &.item-date {
      }
      span {
        &:not(:first-child) {
          padding-left: 10px;
          position: relative;
          &:before {
            position: absolute;
            content: '';
            background: #999;
            width: 2px;
            height: 2px;
            left: 5px;
            top: 50%;
            transform: translateY(-50%);
          }
        }
      }
      .item-price {
      }
      .item-period {
      }
      .item-rating {
      }
    }
  }
  .item-icon {
    position: absolute;
    top: 0;
    display: flex;
    width: 100%;
    justify-content: space-between;
    padding: 15px;
    box-sizing: border-box;
    .icon-cate {
      font-size: 0.7em;
      font-weight: 600;
      background: rgba(255, 255, 255, 0.7);
      border: 1px solid #fff;
      border-radius: 10px;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 5px 8px;
    }
    .icon-heart {
      color: #fff;
    }
  }
}
</style>

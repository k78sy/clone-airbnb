<script setup>
const props = defineProps(['foo'])
console.log(props.foo)
// foo = section.sectionData
</script>
<template>
  <div class="slider-list">
    <div v-for="item in foo.items" class="slide-item" :key="item.contextualPictures[0].id">
      <div class="item-img">
        <img :src="item.contextualPictures[0].picture" />
      </div>
      <ul class="item-info">
        <li class="item-location">{{ item.title }}</li>
        <li class="item-date">{{ item.structuredContent.primaryLine[0].body }}</li>
        <li class="">
          <span class="item-period">
            {{item.structuredDisplayPrice.primaryLine.accessibilityLabel}}
          </span>
          <span class="item-rating">{{ item.avgRatingLocalized }}</span>
        </li>
      </ul>
      <div class="item-icon">
        <span v-if="item.badges.length" class="icon-cate">{{ item.badges[0].text }}</span>
        <span class="icon-heart"><font-awesome-icon :icon="['far', 'heart']" /></span>
      </div>
    </div>
  </div>
</template>
<style lang="scss">
section {
  max-width: $width-pc;
  padding: $pd;
  .slider-top {
    display: flex;
    justify-content: space-between;
    padding-bottom: 20px;
    a {
      text-decoration: none;
      color: #000;
      font-size: 1.2em;
      font-weight: 500;
    }
    .slider-button {
    }
  }
}
.slider-list {
  display: grid;
  gap: 15px;
  grid-template-columns: repeat(7, 1fr);
  .slide-item {
    position: relative;
    .item-img {
      border-radius: 20px;
      overflow: hidden;
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
}
</style>

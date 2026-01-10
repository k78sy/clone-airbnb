<script></script>
<template>
  <main>
    <section>
      <div class="slider-top">
        <a href="">서울의 인기숙소 ></a>
        <div class="slider-button">
          <button class="arrow-btn btn-arctive"><i class="fa-solid fa-angle-left"></i></button>
          <button class="arrow-btn"><i class="fa-solid fa-angle-right"></i></button>
        </div>
      </div>
      <div class="slider-list">
        <div class="slide-item">
          <div class="item-img">
            <img src="https://picsum.photos/200" />
          </div>
          <ul class="item-info">
            <li class="item-location">후암동의 방</li>
            <li class="item-date">5월 29일~31일</li>
            <li class="">
              <span class="item-price">₩79,882</span>
              <span class="item-period">2박</span>
              <span class="item-rating">4.89</span>
            </li>
          </ul>
          <div class="item-icon">
            <span class="icon-cate">게스트 선호</span>
            <span class="icon-heart"><i class="fa-regular fa-heart"></i></span>
          </div>
        </div>
        <div class="slide-item">
          <div class="item-img">
            <img src="https://picsum.photos/209" />
          </div>
          <ul class="item-info">
            <li class="item-location">후암동의 방</li>
            <li class="item-date">5월 29일~31일</li>
            <li class="">
              <span class="item-price">₩79,882</span>
              <span class="item-period">2박</span>
              <span class="item-rating">4.89</span>
            </li>
          </ul>
          <div class="item-icon">
            <span class="icon-cate">게스트 선호</span>
            <span class="icon-heart"><i class="fa-regular fa-heart"></i></span>
          </div>
        </div>
        <div class="slide-item">
          <div class="item-img">
            <img src="https://picsum.photos/201" />
          </div>
          <ul class="item-info">
            <li class="item-location">후암동의 방</li>
            <li class="item-date">5월 29일~31일</li>
            <li class="">
              <span class="item-price">₩79,882</span>
              <span class="item-period">2박</span>
              <span class="item-rating">4.89</span>
            </li>
          </ul>
          <div class="item-icon">
            <span class="icon-cate">게스트 선호</span>
            <span class="icon-heart"><i class="fa-regular fa-heart"></i></span>
          </div>
        </div>
        <div class="slide-item">
          <div class="item-img">
            <img src="https://picsum.photos/202" />
          </div>
          <ul class="item-info">
            <li class="item-location">후암동의 방</li>
            <li class="item-date">5월 29일~31일</li>
            <li class="">
              <span class="item-price">₩79,882</span>
              <span class="item-period">2박</span>
              <span class="item-rating">4.89</span>
            </li>
          </ul>
          <div class="item-icon">
            <span class="icon-cate">게스트 선호</span>
            <span class="icon-heart"><i class="fa-regular fa-heart"></i></span>
          </div>
        </div>
        <div class="slide-item">
          <div class="item-img">
            <img src="https://picsum.photos/203" />
          </div>
          <ul class="item-info">
            <li class="item-location">후암동의 방</li>
            <li class="item-date">5월 29일~31일</li>
            <li class="">
              <span class="item-price">₩79,882</span>
              <span class="item-period">2박</span>
              <span class="item-rating">4.89</span>
            </li>
          </ul>
          <div class="item-icon">
            <span class="icon-cate">게스트 선호</span>
            <span class="icon-heart"><i class="fa-regular fa-heart"></i></span>
          </div>
        </div>
        <div class="slide-item">
          <div class="item-img">
            <img src="https://picsum.photos/204" />
          </div>
          <ul class="item-info">
            <li class="item-location">후암동의 방</li>
            <li class="item-date">5월 29일~31일</li>
            <li class="">
              <span class="item-price">₩79,882</span>
              <span class="item-period">2박</span>
              <span class="item-rating">4.89</span>
            </li>
          </ul>
          <div class="item-icon">
            <span class="icon-cate">게스트 선호</span>
            <span class="icon-heart"><i class="fa-regular fa-heart"></i></span>
          </div>
        </div>
        <div class="slide-item">
          <div class="item-img">
            <img src="https://picsum.photos/205" />
          </div>
          <ul class="item-info">
            <li class="item-location">후암동의 방</li>
            <li class="item-date">5월 29일~31일</li>
            <li class="">
              <span class="item-price">₩79,882</span>
              <span class="item-period">2박</span>
              <span class="item-rating">4.89</span>
            </li>
          </ul>
          <div class="item-icon">
            <span class="icon-heart"><i class="fa-regular fa-heart"></i></span>
          </div>
        </div>
      </div>
    </section>
  </main>
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
      gap:5px;
      li {
        color: #999;
        font-size: .9em;
        &.item-location {
          font-size: 1em;
          font-weight: 500;
          color: #000;
        }
        &.item-date {
          
        }
        span{
          &:not(:first-child){
            padding-left: 10px;
            position: relative;
            &:before{
              position: absolute;
              content: "";
              background: #999;
              width: 2px;
              height: 2px;
              left: 5px;top: 50%;
              transform:translateY(-50%)
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
        font-size: .7em;
        font-weight: 600;
        background: rgba(255,255,255,.7);
        border: 1px solid #fff;
        border-radius: 10px;
        display: flex;
        justify-content: center;
        align-items: center;
        padding:5px 8px;
      }
      .icon-heart {
        color: #fff;
      }
    }
  }
}
</style>

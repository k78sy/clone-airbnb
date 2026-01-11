<script setup></script>
<template>
  <nav class="nav-list">
    <div class="nav-icon"></div>
    <div class="nav-button">
      <button class="active">
        <span class="img"></span>
        <span class="text">숙소</span>
      </button>
      <button>
        <span class="img"></span>
        <span class="text">체험</span>
      </button>
      <button>
        <span class="img"></span>
        <span class="text">서비스</span>
      </button>
    </div>
    <div class="nav-right">
      <a href="">호스팅하기</a>
      <button><i class="fa-solid fa-globe"></i></button>
      <button><i class="fa-solid fa-bars"></i></button>
    </div>
  </nav>
</template>
<style lang="scss">
.nav-list {
  padding: 20px $pd;
  display: flex;
  justify-content: space-between;
  .nav-icon {
    width: 126px;
    height: 56px;
    background: $main-color;
  }
  .nav-button {
    display: flex;
    align-items: center;
    gap: 15px;
    button {
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      background: none;
      border: none;
      position: relative;
      span {
        display: inline-block;
        &.img {
          background: $main-color;
          width: 36px;
          height: 36px;
        }
        &.text {
          padding-left: 10px;
          opacity: .5;
          font-weight: bold;
        }
      }
      &.active{
        &:after{
          width: 100%;
          height: 3px;
          position: absolute;
          content: "";
          background-color: #000;
          bottom: -5px;
          border-radius: 5px;
        }
        span{
          &.text{opacity: 1;}
        }
      }
    }
  }
  .nav-right {
    display: flex;
    gap: 15px;
    align-items: center;
    a {
      font-size: 0.8em;
      font-weight: bold;
      color: #000;
      text-decoration: none;
    }
    button {
      width: 40px;
      height: 40px;
      background: $icon-gray;
      display: flex;
      justify-content: center;
      align-items: center;
      border-radius: 50%;
      border: none;
      cursor: pointer;
    }
  }
}
</style>

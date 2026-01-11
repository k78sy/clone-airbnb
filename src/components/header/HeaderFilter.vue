<script setup></script>
<template>
  <nav class="nav-filter">
    <div>
      <ul>
        <li>
          <div>
            <span class="des">여행지</span>
            <input type="text" placeholder="여행지 검색" />
          </div>
        </li>
        <li>
          <div>
            <span class="des">날짜</span>
            <button>날짜 추가</button>
          </div>
        </li>
        <li>
          <div>
            <span class="des">여행자</span>
            <button>게스트 추가</button>
          </div>
        </li>
      </ul>
      <button class="filter-search"><i class="fa-solid fa-magnifying-glass"></i></button>
    </div>
  </nav>
</template>
<style lang="scss">
.nav-filter {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-bottom: 30px;
  & > div {
    background: #fff;
    box-shadow: 0 5px 20px $icon-gray;
    border: 1px solid #ddd;
    max-width: 850px;
    width: 100%;
    border-radius: 50px;
    position: relative;
    ul {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      li {
        cursor: pointer;
        position: relative;
        & > div{
          position: relative;
          z-index: 1;
        display: flex;
        flex-direction: column;
        }
        &:not(:first-child) {
          &:after {
            position: absolute;
            left: 0;
            top: 50%;
            transform: translateY(-50%);
            content: '';
            width: 1px;
            height: 50%;
            background: #ddd;
          }
        }
        &:before {
          border-radius: 30px;
          width: 100%;
          height: 100%;
          position: absolute;
          content: '';
          left: 0;
          top: 0;
          z-index: 0;
        }
        &:hover:before{
          background: $icon-gray;
        }
        padding: 20px 25px;
        .des {
          font-size: 0.9em;
        }
        input,
        button {
          background: transparent;
          border: none;
          text-align: left;
          color: #999;
          padding: 0;
        }
      }
    }
    .filter-search {
      position: absolute;
      right: 10px;
      top: 10px;
      width: 48px;
      height: 48px;
      border-radius: 50%;
      background: $main-color;
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      border: none;
      cursor: pointer;
      z-index: 6;
    }
  }
}
</style>

<script setup></script>
<template>
  <div class="reco">
    <p>다음 여행을 위한 추천 여행지</p>
    <nav>
      <li class="active">인기</li>
      <li>예술 및 문화</li>
      <li>해변</li>
      <li>산맥</li>
      <li>야외</li>
      <li>즐길 거리</li>
    </nav>
    <ul>
      <li>
        <span class="loca">클리블랜드</span>
        <span class="cont">장기 숙소</span>
      </li>
      <li>
        <span class="loca">필라델피아</span>
        <span class="cont">아파트 숙소</span>
      </li>
      <li>
        <span class="loca">걸프 쇼어스</span>
        <span class="cont">저택 숙소</span>
      </li>
      <li>
        <span class="loca">몬트리올</span>
        <span class="cont">휴가지 숙소</span>
      </li>
      <li>
        <span class="loca">도쿄 </span>
        <span class="cont">콘도 숙소</span>
      </li>
      <li>
        <span class="loca">교토시</span>
        <span class="cont">아파트 숙소</span>
      </li>
      <li>
        <span class="loca">찰스턴 </span>
        <span class="cont">아파트 숙소</span>
      </li>
      <li>
        <span class="loca">Government of Amsterdam</span>
        <span class="cont">아파트 숙소</span>
      </li>
      <li>
        <span class="loca">Raleigh</span>
        <span class="cont">독채 숙소</span>
      </li>
      <li>
        <span class="loca">카우아이카운티</span>
        <span class="cont">휴가지 숙소</span>
      </li>
      <li>
        <span class="loca">휘슬러</span>
        <span class="cont">장기 숙소</span>
      </li>
      <li>
        <span class="loca">세인트피터즈버그 </span>
        <span class="cont">별장 숙소</span>
      </li>
      <li>
        <span class="loca">포틀랜드</span>
        <span class="cont">장기 숙소</span>
      </li>
      <li>
        <span class="loca">웨스트팜비치</span>
        <span class="cont">장기 숙소</span>
      </li>
      <li>
        <span class="loca">갤버스턴</span>
        <span class="cont">독채 숙소</span>
      </li>
      <li>
        <span class="loca">샬럿</span>
        <span class="cont">저택 숙소</span>
      </li>
      <li>
        <span class="loca">플라야 델 카르멘 해변</span>
        <span class="cont">독채 숙소</span>
      </li>
      <li>
        <span>더 보기</span>
      </li>
    </ul>
  </div>
</template>
<style lang="scss">
.reco {
  padding: $pd 0;
  p {
    font-size: 1.5em;
  }
  nav {
    display: flex;
    gap: 15px;
    border-bottom: 1px solid #ddd;
    li {
      font-size: 0.9em;
      list-style: none;
      cursor: pointer;
      padding: 10px 0;
      opacity: 0.5;
      &.active {
        opacity: 1;
      }
    }
  }
  ul {
    padding: 20px 0;
    display: grid;
    gap: 20px;
    grid-template-columns: repeat(6, 1fr);
    li {
      font-size: 0.9em;
      display: flex;
      flex-direction: column;
      .loca {
        font-weight: 500;
      }
      .cont {
        opacity: 0.7;
      }
    }
  }
}
</style>

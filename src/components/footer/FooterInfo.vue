<script></script>
<template>
  <div class="footer">
    <ul>
      <li>에어비앤비 지원</li>
      <li><a href="">도움말 센터</a></li>
      <li><a href="">안전 문제 관련 도움받기</a></li>
      <li><a href="">에어커버</a></li>
      <li><a href="">차별 반대</a></li>
      <li><a href="">장애인 지원</a></li>
      <li><a href="">예약 취소 옵션</a></li>
      <li><a href="">이웃 민원 신고</a></li>
    </ul>
    <ul>
      <li>호스팅</li>
      <li><a href="">당신의 공간을 에어비앤비하세요</a></li>
      <li><a href="">에어비앤비에서 체험 호스팅하기</a></li>
      <li><a href="">에어비앤비에서 서비스 호스팅하기</a></li>
      <li><a href="">호스트를 위한 에어커버</a></li>
      <li><a href="">호스팅 자료</a></li>
      <li><a href="">커뮤니티 포럼</a></li>
      <li><a href="">책임감 있는 호스팅</a></li>
      <li><a href="">무료 호스팅 클래스 참여하기</a></li>
      <li><a href="">공동 호스트 찾기</a></li>
      <li><a href="">호스트 추천</a></li>
    </ul>
    <ul>
      <li><a href="">에어비앤비</a></li>
      <li><a href="">2025 여름 업그레이드</a></li>
      <li><a href="">뉴스룸</a></li>
      <li><a href="">채용정보</a></li>
      <li><a href="">투자자 정보</a></li>
      <li><a href="">Airbnb.org 긴급 숙소</a></li>
    </ul>
  </div>
  <address>
    <div class="info">
      <ul>
        <li>© 2026 Airbnb, Inc.</li>
        <li>개인정보 처리방침</li>
        <li>쿠키 정책</li>
        <li>이용약관</li>
        <li>한국의 변경된 환불 정책</li>
        <li>회사 세부정보</li>
      </ul>
    </div>
    <div class="sns">
      <ul>
        <li><font-awesome-icon :icon="['fas', 'globe']" /> 한국어 (KR)</li>
        <li>₩ KRW</li>
        <li><font-awesome-icon :icon="['fab', 'facebook']" /></li>
        <li><font-awesome-icon :icon="['fab', 'x-twitter']" /></li>
        <li><font-awesome-icon :icon="['fab', 'instagram']" /></li>
      </ul>
    </div>
  </address>
  <div class="copy">
    웹사이트 제공자: Airbnb Ireland UC, private unlimited company, 8 Hanover Quay Dublin 2, D02 DP23
    Ireland | 이사: Dermot Clarke, Killian Pattwell, Andrea Finnegan | VAT 번호: IE9827384L | 사업자
    등록 번호: IE 511825 | 연락처: terms@airbnb.com, 웹사이트, 080-822-0230 | 호스팅 서비스
    제공업체: 아마존 웹서비스 | 에어비앤비는 통신판매 중개자로 에어비앤비 플랫폼을 통하여 게스트와
    호스트 사이에 이루어지는 통신판매의 당사자가 아닙니다. 에어비앤비 플랫폼을 통하여 예약된 숙소,
    체험, 호스트 서비스에 관한 의무와 책임은 해당 서비스를 제공하는 호스트에게 있습니다.
  </div>
</template>
<style lang="scss">
.footer {
  font-size: 0.8em;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  border-bottom: 1px solid #ddd;
  padding-bottom: 50px;
  ul {
    display: flex;
    flex-direction: column;
    gap: 10px;
    li {
      &:first-child {
        font-weight: 500;
      }
      a {
        text-decoration: none;
        color: #000;
      }
    }
  }
}
address {
  display: flex;
  justify-content: space-between;
  border-bottom: 1px solid #ddd;
  padding: 30px 0 20px;
  div {
    &.info {
    }
    &.sns {
    }
    ul {
      display: flex;
      li {
      }
    }
  }
}
.copy {
  padding-top: 10px;
  font-size: 0.6em;
}
</style>

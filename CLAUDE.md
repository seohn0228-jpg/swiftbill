# SwiftBill — 작업 규칙

- **대표(사용자)에게 하는 말은 무조건 한국어(해요체)로만 한다.** 툴 화면은 영어지만 설명·보고·질문은 전부 한국어로 쓴다. 영어 문구를 보여 줄 때는 뜻을 한국어로 풀어 준다.
- 짧고 쉽게, 결론 먼저. 전문 용어는 풀어서 쓴다.
- 사이트: GitHub Pages(main 브랜치), 주소 https://seohn0228-jpg.github.io/swiftbill/
- 설정: `index.html` 스크립트 맨 위 `CUSTOMER_CODES`(구매자 코드), `CHECKOUT_URL`(검롯 상품 주소).
- 작업 방식: `dev` 브랜치에서 고치고 시험한 뒤, 대표 확인을 받고 `main`에 합친다(사이트는 main으로 열림).
- 문의 메일: swiftbill26@gmail.com (index.html `CONTACT_EMAIL`과 정책 페이지 3개에 들어 있음). 환불: 구매 후 7일 안 전액(2026-11-26 대표 결정).
- 무료: 한 달 PDF 3회(2026-11-26 대표 결정). Pro: 검롯 라이선스 키, 기기 3대까지.
- 가격: 출시 기념가 $9(정가 $15). 화면에는 정가 대신 "40% 할인"으로 표시(2026-11-26 대표 결정, 검롯이 손님 나라 돈으로 바꿔 보여 줘서 줄 그은 $15와 섞이지 않게). 첫 구매 20건 또는 1~2달 뒤 12~15달러로 올릴지 정함.
- 검롯: 상품 SwiftBill Pro(id r_D8j14r5tISLeNkBdcCbg==, https://swiftbill4.gumroad.com/l/Pro, 계정 swiftbill26). 맞춤 랜딩 페이지 = marketing/landing.html, 2026-11-26 공개. 고칠 때 검롯 CLI(go로 빌드, 키는 환경 네트워크 시크릿 api.gumroad.com)로 page preview → publish → 실제 페이지에서 구매 버튼 눌러 결제 화면 확인. 되돌리기: products page clear.
- 방문 통계: GoatCounter(쿠키 없음, IP 저장 안 함, 추적 거부·GPC 브라우저는 안 셈). index.html `GOATCOUNTER_CODE`='swiftbill'(2026-11-27 켬, 대시보드 https://swiftbill.goatcounter.com, 계정 swiftbill26). 이벤트: export-free, export-pro, limit-hit, pro-window-*, checkout-click, pro-unlocked(인보이스 내용·키는 안 보냄). 결제 링크에 utm 꼬리표가 이어 붙음. 홍보 링크는 marketing/utm-links.md. **방문·클릭은 GoatCounter, 검롯 페이지 방문·구매·전환율은 검롯 Analytics 숫자만 쓴다(클릭 ≠ 구매).**
- 라이선스(2026-11-27 개편): Pro는 저장된 증거로만 판단(pro:true 무시). 관리자 키는 해시로 매번 확인. 검롯 키는 방문 때마다(10분에 1번까지) 재확인, 잘못된/환불/비활성 키는 Pro 끔, 서버·인터넷 오류로는 끄지 않음(마지막 확인 후 30일까지 오프라인 사용). 기기 등록(+1) 성공해야 Pro, 3대 넘으면 거절. 기기 수 초기화는 검롯 CLI `licenses decrement`로 대표 요청 시.
- 백업 브랜치: backup-2026-11-27(개편 전 사이트). Pro 기능: 백업(.json)·복원, 복제, 번호 이어 매기기, 같은 번호 저장 시 덮어쓰기.
- 서버 없는 한계(과장 금지): 코드 수정·검롯 요청 차단·시크릿 창/저장소 삭제로 무료 횟수·Pro를 완전히 막을 수 없음.

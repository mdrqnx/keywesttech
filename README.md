# KeyWest Tech 웹사이트 (리뉴얼)

주식회사 키웨스트테크(KeyWest Tech Co., Ltd.) 기업 웹사이트 리뉴얼 버전입니다.
빌드 도구 없이 동작하는 정적 원페이지 사이트(HTML · CSS · 바닐라 JS)로, 어떤 웹 서버/정적 호스팅에도 그대로 올릴 수 있습니다.
디자인 시스템은 앨리웍스(Allyworks) 리뉴얼 사이트와 같은 구조를 쓰고, 색상만 키웨스트(바다·섬) 톤으로 바꿨습니다.

## 구성 (index.html 한 페이지)

| 섹션 | 앵커 | 내용 |
| --- | --- | --- |
| 히어로 | `#top` | 슬로건(Never Ending, Keep Going), 핵심 소개 |
| 사업분야 | `#business` | 시스템 통합사업 · 시스템 유지보수 · 정보화전략 컨설팅 |
| 회사소개 | `#company` | 인사말, 설립 2017년 1월 · 주업종 · 대표이사 |
| 미션·비전·슬로건 | `#vision` | 고객의 가치 향상 / 집념과 도전은 새로운 역사의 시작 / Never Ending, Keep Going |
| 핵심가치 · Our Goal | `#values` | 신뢰 · 소통 · 열정 · 혁신 |
| 시스템 통합 | `#si` (`#si-build`, `#maintenance`) | 공공기관 SI 구축, 시스템 통합 유지보수 |
| IT 컨설팅 | `#consulting` | 방향성 수립 → 현황 분석 → To-Be 모델 수립 → 이행계획 수립 |
| 문의 | `#contact` | 이메일 · 주소 · 지도 링크 · 문의 양식(메일 앱 연동) |

## 폴더 구조

```
assets/
  css/style.css        공통 디자인 시스템 (색상 토큰은 파일 상단 :root)
  css/pages/home.css   페이지 스타일
  js/main.js           헤더, 모바일 메뉴, 스크롤 애니메이션, 메뉴 하이라이트(scrollspy), 문의 양식(mailto)
  img/brand/           공식 로고(기존 홈페이지 로고를 벡터화한 SVG), 파비콘
  img/photos/          히어로 사진(Pexels) · 회사소개 섬 사진(기존 홈페이지 이미지)
  img/consulting/      IT 컨설팅 단계 사진(Pexels)
```

## 로컬에서 보기

```bash
python3 -m http.server 8000
# 브라우저에서 http://localhost:8000
```

## 참고
- 문의 양식은 서버 없이 방문자의 메일 앱을 여는 방식입니다(`<form data-mailto="...">`).
- 기존 사이트의 오탈자(주소 "통안구" → "동안구", "Imfra" → "Infra" 등)를 바로잡았습니다.
- IT 컨설팅 STEP 4(이행계획 수립)의 세부 항목은 기존 사이트에 STEP 1 항목이 중복 게시되어 있어,
  일반적인 정보화전략(ISP) 이행계획 항목(이행과제 우선순위 도출 · 추진 일정 수립 · 소요 자원·예산 산정)으로 채웠습니다. 실제 내용으로 확인·수정해 주세요.

## 사진 출처 (Pexels License — 상업적 이용 가능, 출처 표기 의무 없음)
| 파일 | Pexels 사진 |
| --- | --- |
| `assets/img/photos/hero-flight.jpg` | https://www.pexels.com/photo/airplane-wing-above-clouds-731217/ |
| `assets/img/consulting/step-1.jpg` | https://www.pexels.com/photo/colleagues-having-a-meeting-5439478/ |
| `assets/img/consulting/step-2.jpg` | https://www.pexels.com/photo/close-up-shot-of-a-laptop-computer-12969403/ |
| `assets/img/consulting/step-3.jpg` | https://www.pexels.com/photo/white-printer-paper-196645/ |
| `assets/img/consulting/step-4.jpg` | https://www.pexels.com/photo/manager-considering-project-strategy-by-the-task-board-6804077/ |

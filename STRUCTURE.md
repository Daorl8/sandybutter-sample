# STRUCTURE — Sandy Butter (샌디버터)

**링크 허브(링크인바이오)** 단일 페이지. 고객 요청 = "링크로만". 오븐 버터 디저트 온라인 주문 브랜드.

```
/ (배포 루트, CF [assets] directory="./")
├─ index.html          단일 파일 (인라인 CSS/JS, 모바일 우선 링크허브)
├─ sb-badge.webp       주황 원형 로고 배지 (상단 아바타)
├─ sb-logo.webp        캐릭터 워드마크 로고 (버터 소녀+쿠키 소년)
├─ sb-eggtart.webp     에그타르트 (쇼케이스)
├─ sb-fruitsand.webp   과일 샌드(딸기·샤인머스캣) (쇼케이스)
├─ sb-cake.webp        딸기 생크림 케이크 (쇼케이스)
├─ favicon.png         배지 기반 파비콘 (180px)
├─ wrangler.toml       name=sandybutter-sample, [assets] ./
├─ .assetsignore       .git·문서·img·_cs 제외
├─ CHANGELOG.md / STRUCTURE.md
└─ img/                원본 47장 + 원본 사본 (배포 제외)
```

## 링크 (고객 제공 = 이게 전부)
1. **오븐 주문하기** → https://oven-sandybutter.web.app/ (primary, 주황 버튼)
2. **카카오톡 채널** → https://pf.kakao.com/_vpXxkn (문의·예약·비즈니스 제안)
3. **인스타그램** → https://www.instagram.com/sandybutter_/

## 디자인 (미국 팝아트 / 캐릭터 프랜차이즈)
- **키컬러 주황** `--orange #F37828`(배지 실측) · `--orange-deep #E45B12`(버튼 hover) · `--orange-text #AE3F08`(크림 위 텍스트, AA 4.88) · 골드 `#F1A037` · 크림 배경 `#F6E6CF`(도트 패턴) · 코믹 블랙 `--ink #1C140F` · 캐릭터 액센트 핑크 `#F27E9D`·블루 `#5B9BD5`.
- **폰트(시안=CDN)**: 헤딩·버튼 라벨·워드마크 **Bagel Fat One**(동글+강한 팻 라운드, 한글 지원) + 본문 Pretendard. ⚠️납품 시 서브셋 self-host.
- **팝아트 스타일**: 3px 코믹 블랙 아웃라인 + 하드 오프셋 그림자(5px 5px 0), 라운드(16~20px), 버튼 press 효과(translate+그림자 축소), 살짝 기울인 쇼케이스, 배지 pop-in.
- a11y: reveal + 2s 타임아웃 + noscript 폴백, :focus-visible, reduced-motion 폴백, 아이콘 aria-hidden.

## ⚠️ 확인/보류
- 실주소·영업시간 미확보(온라인 주문 브랜드) → JSON-LD는 Organization(주소 없이 name·logo·sameAs 3채널).
- og:image 상대경로·og:url·canonical = **도메인 확정 후** 절대경로 3줄 동시 추가.
- 쇼케이스 3컷 = 사장님 실제 제품 사진(에그타르트·과일샌드·케이크). 리포스트/그래픽/텍스트오버레이 컷은 제외.
- 폰트 CDN(시안) → 납품 시 self-host.

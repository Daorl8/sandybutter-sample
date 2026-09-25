# CHANGELOG — Sandy Butter (샌디버터)

## v0.2 — 2026-09-25 (모찌 라인 전환)
- **문구**: 버튼 "오븐 주문하기"→"택배 주문하기". 태그라인 "에그타르트·과일샌드·두바이 김밥"→"과일모찌·초코모찌·요거트모찌". meta description·JSON-LD description·og:image도 모찌로 일관화(og→sb-mochi-fruit).
- **쇼케이스 사진 → 모찌 3컷**: sb-mochi-fruit(딸기 과일모찌)·sb-mochi-choco(초코모찌)·sb-mochi-muscat(샤인머스캣 과일모찌). #10 과일모찌 원본의 "Shine Muscat/Strawberry" 텍스트는 컵별 크롭으로 제거. #18 초코모찌.
- ⚠️**요거트모찌 실물 사진은 폴더에 없음** → 쇼케이스는 과일모찌(딸기·머스캣)+초코모찌로 구성. 요거트모찌 사진 확보 시 교체.
- 기존 sb-eggtart·fruitsand·cake.webp는 미참조 orphan.
- QA: 자산 무결성·태그균형·이모지0·alt5/5 통과.

## v0.1.1 — 2026-09-25 (리뷰 반영)
- **Pretendard CDN 무버전화**: `pretendard@v1.3.9` → `pretendard`(버전 제거). CF 이메일 난독화 함정 회피 + 타 샘플(saru·hausment)과 일관. (시안 CDN, 납품 시 self-host라 최신핀 무해)
- JSON-LD 관련 주석 명확화(JSON-LD는 이미 포함=Organization, 보류는 canonical·og:url·절대 og:image뿐).

## v0.1 — 2026-09-25 (최초 시안)
- **유형**: 링크 허브(링크인바이오) — 고객 요청 "링크로만". 오븐 버터 디저트 온라인 주문 브랜드(에그타르트·과일샌드·두바이 김밥·딸기 케이크).
- **이미지 큐레이션**: IG 원본 47장에서 로고 2종(캐릭터 워드마크 #0, 주황 원형 배지 #44) + 사장님 실제 제품 사진 3컷(에그타르트·과일샌드·딸기케이크) 선별. 리포스트(MOSSHOUR)·그래픽·텍스트오버레이·재료샷 제외. webp 변환·`sb-` slug. favicon 생성.
- **디자인**: 미국 팝아트/캐릭터 프랜차이즈 방향. 키컬러 주황(#F37828 배지 실측), 코믹 블랙 아웃라인+하드 오프셋 그림자, Bagel Fat One(동글+강한) 헤딩 + Pretendard 본문.
- **빌드**: 단일 index.html — 배지 아바타 → 캐릭터 로고 → 태그라인 → 제품 쇼케이스 3컷 → 링크 버튼 3종(오븐 주문/카카오톡 채널/인스타) → 푸터. 버튼 press 효과, reveal+noscript, JSON-LD Organization.
- **QA**: 자산 무결성·태그균형·이모지0·alt5/5·lazy 3/5 통과. AA 보정(크림 위 주황 텍스트 #E45B12→#AE3F08=4.88; 버튼 블랙/주황 6.51).
- **레포 스캐폴드**: wrangler.toml·.assetsignore·STRUCTURE.md.

### 보류/확인
- og:image 절대경로·og:url·canonical → 배포 도메인 확정 후 3줄 동시 추가.
- 폰트 CDN(시안) → 납품 시 서브셋 self-host.
- 헤드리스 렌더 스크린샷: 브라우저 다운로드 제한으로 미실행 → 정적 QA 갈음, 로컬 육안 확인 권장.

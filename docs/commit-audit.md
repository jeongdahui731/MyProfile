# 과제 커밋 집계 근거

## 집계 기준

- 검토일은 2026년 11월 8일이다. 이번 문서를 작성하기 전 main 이력의 모든 사이트 diff와 README·검증 문서 변경을 검토했다.
- 시작 기준은 [fb99e5987e883dce2d4fb031da923fdb7d46baac](https://github.com/jeongdahui731/MyProfile/commit/fb99e5987e883dce2d4fb031da923fdb7d46baac)이며 후보에는 포함하고 유효 산정에서는 제외한다.
- 끝 기준은 [a101400b328151bb9fed86b930f6d72f780728d0](https://github.com/jeongdahui731/MyProfile/commit/a101400b328151bb9fed86b930f6d72f780728d0)이다. 이는 집계 시점 main이며 최종 제출 SHA는 이후 문서 커밋에 따라 갱신해야 한다.
- 커밋 목록은 https://github.com/jeongdahui731/MyProfile/commits/a101400b328151bb9fed86b930f6d72f780728d0/ 이다. 범위 비교는 https://github.com/jeongdahui731/MyProfile/compare/fb99e5987e883dce2d4fb031da923fdb7d46baac...a101400b328151bb9fed86b930f6d72f780728d0 이며 이 비교 화면은 시작 커밋 자체를 제외한다. 전체 후보 수는 루트부터 rev-list로 계산했다.
- 2026년 11월 8일 01시 17분 08초 KST에 원격 main과 위 끝 SHA 일치를 조회했다. 같은 SHA의 push 실행은 completed / success이며 https://github.com/jeongdahui731/MyProfile/actions/runs/42390326905 이다.

## 개수와 판정 범위

| 항목 | 수 |
| --- | --- |
| 전체 고유 후보 N | 60 |
| 초기 등록 보수적 제외 | 1 |
| 빈 틀 분리 단계 보수적 추가 제외 | 3 |
| 제외 합계 E | 4 |
| 잠정 유효 N−E | 56 |

이 문서는 교수님의 최종 채점 판정이 아닌 diff 검토에 따른 보수적 자기 집계다. 단계별 제목·설명·스타일 변경을 나누어 커밋한 사실을 숨기지 않는다. 모든 비제외 커밋에는 실제 변경이 있지만, 분할 목적과 변경의 의미에 관한 최종 인정은 교수님 기준에 따른다. 50개 충족을 무조건 보장하는 표현은 사용하지 않는다.

빈 커밋 0개, 병합 커밋 0개, 작성자 이름에 bot이 표시된 커밋 0개를 기계적으로 확인했다. 작성자 이름 검사는 봇 여부의 완전한 증명은 아니다. 빌드 결과만의 자동 커밋이나 번호·날짜만 변경한 커밋은 검토한 범위에서 발견하지 못했다.

커미터 기록 시각만으로 마감 전 구간을 나누면 후보 59개, 같은 제외 기준 적용 후 55개다. 마감 이후 커밋은 a101400의 검증 문서·증거 추가다. 커미터 시각은 GitHub 수신 시각이나 LMS 제출 시각을 증명하지 않으며 지각·재제출 판단은 수업 공지에 따른다.

## 제외 SHA와 이유

| SHA | 개수 | 이유 |
| --- | --- | --- |
| [fb99e5987e883dce2d4fb031da923fdb7d46baac](https://github.com/jeongdahui731/MyProfile/commit/fb99e5987e883dce2d4fb031da923fdb7d46baac) | 1 | 원본 테마·ZIP 등록과 생성된 초기 배포 설정이 한 커밋에 섞였다. 원본 단순 등록 제외 원칙을 보수적으로 적용해 전체 1개를 제외한다. |
| [83405e4c1fa48c6b32164c9b5fe92d999a09bb94](https://github.com/jeongdahui731/MyProfile/commit/83405e4c1fa48c6b32164c9b5fe92d999a09bb94) | 1 | 기술 역량의 빈 목록과 잠시 쓰고 제거한 높이만 먼저 추가한 분리 단계다. 개수 확보용 빈 틀로 판단될 여지를 고려해 보수적으로 제외한다. |
| [aacf70cc91f232c5168aefd633d854e41f400baa](https://github.com/jeongdahui731/MyProfile/commit/aacf70cc91f232c5168aefd633d854e41f400baa) | 1 | 관심 분야의 빈 목록과 임시 높이만 먼저 추가한 분리 단계다. 이후 실제 제목·동기 작성과 구분하여 이 빈 틀 단계는 보수적으로 제외한다. |
| [320e62a44ae73a9cb6302d54e9baef2f8782f09e](https://github.com/jeongdahui731/MyProfile/commit/320e62a44ae73a9cb6302d54e9baef2f8782f09e) | 1 | 실제 활동의 비어 있는 다섯 항목과 임시 높이만 먼저 추가한 분리 단계다. 보수적으로 제외한다. |

## 검토 방법과 세부 판단

- main의 rev-list와 부모 목록, diff-tree로 개수·빈 변경·병합을 확인하고 각 사이트 diff를 실제로 읽었다. 본인 과제 문서인 README와 실제 검증 기록도 검토했다.
- 초기 커밋은 원본 ZIP뿐 아니라 생성 배포 설정도 포함하지만 혼합 등록 1개 전체를 보수적으로 제외했다.
- 학습 목표 첫 틀 82465fe는 이후 여러 페이지가 실제 사용하는 공통 목록·타이포그래피·선 스타일을 새로 구현했으므로 포함 후보로 두었다. 다른 세 빈 틀은 공통 클래스를 연결하고 임시 높이를 추가한 단계여서 별도로 보수 제외했다.
- 87a1d11과 e4ca993은 메시지가 같지만 각각 홈 설정과 별도 글 제목을 바꾼 서로 다른 diff다. 자동 중복 제거하지 않았다.
- c953b92 이후 홈 요약이 비는 현상을 019a811에서 홈 소개 partial 재정의로 해결했다. 문제 대응 수정이며 무의미한 변경·되돌림으로 단정하지 않았다.
- 45d2ad5는 사용자 요구가 현재 위치 효과만 표시에서 실제 같은 페이지 링크로 바뀐 변경이다. 이전 버튼 코드와 같게 되돌린 것이 아니라 새 링크 동작을 추가했다.
- 각 카드의 효과·연결·본문을 여러 단계에 나누어 요청·커밋했다. 각 SHA의 실제 변경은 아래에 공개하고 최종 인정 가능성은 별도 판단 사항으로 남긴다.
- 당시 각 커밋에서 개별 Hugo 빌드 성공을 모두 수집한 것은 아니다. 당시 정적 검사와 확인 범위는 docs/work-log.md, 현재 공개 검증은 docs/verification.md를 참조한다. 현재 결과가 모든 과거 커밋의 동작을 증명하지 않는다.

## 단계별 대표 커밋

| 단계 | 커밋과 메시지 | 실제 변경과 확인 근거 |
| --- | --- | --- |
| 초기 본인 설정 | [71d84b1 포트폴리오 사이트 제목 설정](https://github.com/jeongdahui731/MyProfile/commit/71d84b170c041b28069225eee8333604c8c128ed) | pages.json의 테마 기본 제목을 포트폴리오 제목으로 변경한 diff |
| 홈 구현·문제 대응 | [019a811 이름과 짧은 자기소개 위치 변경](https://github.com/jeongdahui731/MyProfile/commit/019a811633c1e1a3f8ec7b878e56fc42697ff847) | 홈 소개 partial과 Content 추가, 중복 카드 숨김. 현재 홈 캡처와 연결 |
| 활동 콘텐츠 | [5f5b754 실제 활동 상세 화면 내용 추가](https://github.com/jeongdahui731/MyProfile/commit/5f5b754df8425c1c50311b78426ca0d924a1e83a) | 실제 활동의 목적·역할·과정·결과·배운 점과 계획 작성 |
| 배치 개선 | [da1103d 학습 목표 상세 화면 수정](https://github.com/jeongdahui731/MyProfile/commit/da1103d283ce25c68093276b52e6c4014921b011) | 선 굵기·임시 높이 제거·내용에 따른 목록 길이 개선 |
| 실제 검증 기록 | [a101400 공개 사이트 검증표와 화면 증거 정리](https://github.com/jeongdahui731/MyProfile/commit/a101400b328151bb9fed86b930f6d72f780728d0) | 5영역 검사표·실제 캡처·API 배포 증거 추가 |

## 전체 커밋별 검토 목록

아래 파일명은 저장소 상대 경로다. 초기 원본 등록은 파일 수가 많아 총수와 대표 경로만 적고 커밋 링크로 전체를 확인한다. 포함 후보는 확정 채점 결과를 뜻하지 않는다.

| 번호 | SHA와 커밋 메시지 | 커미터 시각 | 변경 파일 | 실제 변경 | 관련 기준 | 자기 집계 |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | [fb99e59](https://github.com/jeongdahui731/MyProfile/commit/fb99e5987e883dce2d4fb031da923fdb7d46baac) Initial PaperMod theme and GitHub Pages setup | 2026-11-07T14:00:25+09:00 | 총 272개. site/·assets/·layouts/·.github/·LICENSE 등 | 원본과 초기 배포 등록 | P08~P10 | 제외 |
| 2 | [71d84b1](https://github.com/jeongdahui731/MyProfile/commit/71d84b170c041b28069225eee8333604c8c128ed) 포트폴리오 사이트 제목 설정 | 2026-11-07T16:05:04+09:00 | `docs/work-log.md`<br>`site/pages.json` | 사이트 제목을 실제 포트폴리오 제목으로 설정 | P80 | 포함 후보 |
| 3 | [02fa815](https://github.com/jeongdahui731/MyProfile/commit/02fa81537da3a11365145926978fbd0b36f10b80) 사이트 설명과 작성자 정보 설정 | 2026-11-07T16:26:00+09:00 | `docs/work-log.md`<br>`site/pages.json` | 사이트 설명과 작성자 설정 추가 | P10·P80 | 포함 후보 |
| 4 | [1770df7](https://github.com/jeongdahui731/MyProfile/commit/1770df7bfeab56a0c4d0758878699cfe7625675b) 작성자 실명 반영 및 한국어 문서 언어 설정 | 2026-11-07T16:42:20+09:00 | `docs/work-log.md`<br>`site/pages.json` | 실명과 한국어 언어 코드 반영 | P48 | 포함 후보 |
| 5 | [87a1d11](https://github.com/jeongdahui731/MyProfile/commit/87a1d112d9372abd0d2ed2b70b7943656dc836fe) 홈페이지에 이름 배치 | 2026-11-07T18:31:40+09:00 | `docs/work-log.md`<br>`site/content/_index.md`<br>`site/pages.json` | 홈 이름 설정과 Welcome 제거 | P59·P80 | 포함 후보 |
| 6 | [e4ca993](https://github.com/jeongdahui731/MyProfile/commit/e4ca993102c01c53534b214fae18f3a195100218) 홈페이지에 이름 배치 | 2026-11-07T18:39:41+09:00 | `docs/work-log.md`<br>`site/content/posts/hello.md` | 별도 예시 글 제목을 Hello에서 정다희로 변경 | P80 | 포함 후보 |
| 7 | [73d2093](https://github.com/jeongdahui731/MyProfile/commit/73d2093fd5f80e6985d12c79a3eba92be7e31782) 홈페이지에 짧은 자기소개 배치 | 2026-11-07T18:43:38+09:00 | `docs/work-log.md`<br>`site/content/posts/hello.md` | 예시 본문을 소개로 교체하고 날짜·작성자 표시 숨김 | P59·P80 | 포함 후보 |
| 8 | [6c7f4c9](https://github.com/jeongdahui731/MyProfile/commit/6c7f4c9a2fedb5856a6397740c0561ddf522b2e8) 밝은 화면 배경을 연한 회색으로 변경 | 2026-11-07T18:57:10+09:00 | `docs/work-log.md`<br>`site/assets/css/core/theme-vars.css` | 밝은 테마 배경색 변경 | P11·P49 | 포함 후보 |
| 9 | [c953b92](https://github.com/jeongdahui731/MyProfile/commit/c953b9233302e4fd09590f53d818c089edaa40a2) 짧은 자기소개를 진한 회색으로 설정 | 2026-11-07T19:04:01+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/intro.css`<br>`site/content/posts/hello.md` | 소개를 description으로 옮기고 회색 스타일 추가 | P49 | 포함 후보 |
| 10 | [009a54f](https://github.com/jeongdahui731/MyProfile/commit/009a54f0cd3d5b6f9446cddf2d75782c81496dd7) 상단 메뉴에 텍스트 배치 | 2026-11-07T19:11:49+09:00 | `docs/work-log.md`<br>`site/assets/css/common/header.css`<br>`site/themes/template/layouts/_partials/header.html` | 상단 두 소셜 문구와 글자 크기 추가 | P29 | 포함 후보 |
| 11 | [59c97dd](https://github.com/jeongdahui731/MyProfile/commit/59c97dd9482470d1b3cc63b91f8086950ac7b028) 인스타 연결 | 2026-11-07T19:19:34+09:00 | `docs/work-log.md`<br>`site/themes/template/layouts/_partials/header.html` | Instagram을 본인 프로필로 연결 | P28 | 포함 후보 |
| 12 | [13ef05e](https://github.com/jeongdahui731/MyProfile/commit/13ef05ec63d4beedba89f1ae371727b9a1238304) GitHub 연결 | 2026-11-07T19:28:21+09:00 | `docs/work-log.md`<br>`site/themes/template/layouts/_partials/header.html` | GitHub를 본인 계정으로 연결 | P27 | 포함 후보 |
| 13 | [ad8479c](https://github.com/jeongdahui731/MyProfile/commit/ad8479cade7fd3aa8f0f330e86b9820ca47b7517) 왼쪽 상단 클릭 효과 추가 | 2026-11-07T19:32:50+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/social-links.css`<br>`site/themes/template/layouts/_partials/header.html` | 두 소셜 링크의 active 회색 효과 추가 | P49 | 포함 후보 |
| 14 | [019a811](https://github.com/jeongdahui731/MyProfile/commit/019a811633c1e1a3f8ec7b878e56fc42697ff847) 이름과 짧은 자기소개 위치 변경 | 2026-11-07T19:38:55+09:00 | `docs/work-log.md`<br>`site/content/posts/hello.md`<br>`site/layouts/_partials/home_info.html`<br>`site/pages.json` | 홈 소개가 직접 표시되도록 partial 재정의·중복 카드 숨김 | P59·P80 | 포함 후보 |
| 15 | [0fcaba1](https://github.com/jeongdahui731/MyProfile/commit/0fcaba1027ed33d4e7faee9f3f6cc42dcaf186da) 본문 이름 글씨 크기 변경 | 2026-11-07T19:45:26+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/intro.css`<br>`site/layouts/_partials/home_info.html` | 홈 이름에만 34px 적용 | P31·P32 | 포함 후보 |
| 16 | [46c0653](https://github.com/jeongdahui731/MyProfile/commit/46c065342ffcd888e71c34388a14d2ce3a993e1b) 관심 분야 영역  생성 | 2026-11-07T19:52:48+09:00 | `docs/work-log.md`<br>`site/content/posts/interests.md` | 관심 분야 페이지와 홈 카드 생성 | P21·P71 | 포함 후보 |
| 17 | [d598104](https://github.com/jeongdahui731/MyProfile/commit/d5981046251c8043b7ba3ff15b4564a7ae05c1f2) 관심 분야 상세 페이지 제목 위치 변경 | 2026-11-07T20:01:53+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/interests.css`<br>`site/content/posts/interests.md`<br>`site/themes/template/layouts/single.html` | 관심 분야에 페이지 클래스와 제목 여백 적용 | P31·P32 | 포함 후보 |
| 18 | [87a4341](https://github.com/jeongdahui731/MyProfile/commit/87a4341755b28f92a43095447bab1414f2d097cc) 관심분야 상세 페이지 경로 추가 | 2026-11-07T20:05:07+09:00 | `docs/work-log.md`<br>`site/content/posts/interests.md`<br>`site/themes/template/layouts/single.html` | 텍스트 경로 출력과 기본 경로 fallback 추가 | P22 | 포함 후보 |
| 19 | [84ec0b4](https://github.com/jeongdahui731/MyProfile/commit/84ec0b41ec9b3d179c77135ca71bc2d86ef86fc2) 홈을 홈페이지에 연결 | 2026-11-07T20:09:29+09:00 | `docs/work-log.md`<br>`site/content/posts/interests.md`<br>`site/themes/template/layouts/single.html` | 홈 경로를 실제 홈페이지 링크로 연결 | P23 | 포함 후보 |
| 20 | [a3ac170](https://github.com/jeongdahui731/MyProfile/commit/a3ac170c3eccbb4fb4a2db4e270562577e8676f7) 경로 위치 및 크기 변경 | 2026-11-07T20:12:49+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/interests.css` | 경로·제목 크기와 간격 조정 | P31·P32 | 포함 후보 |
| 21 | [a1e8d65](https://github.com/jeongdahui731/MyProfile/commit/a1e8d65b485bbf87f4ae12320876e151986b6aaa) 경로 색상 및 굵기  변경 | 2026-11-07T20:15:53+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/interests.css` | 경로 색상과 구분 기호 굵기 조정 | P49 | 포함 후보 |
| 22 | [fab0c6b](https://github.com/jeongdahui731/MyProfile/commit/fab0c6b4374e54b62b93259a298401fb85a16536) 경로에 클릭 효과 추가 | 2026-11-07T20:20:50+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/interests.css`<br>`site/themes/template/layouts/single.html` | 경로 누름 회색 효과와 현재 위치 버튼 적용 | P49 | 포함 후보 |
| 23 | [d0bed38](https://github.com/jeongdahui731/MyProfile/commit/d0bed387a95f92fb1e90c1364b6ec305ed967331) 흰 카드 클릭 효과 추가 | 2026-11-07T20:29:43+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/cards.css`<br>`site/themes/template/layouts/baseof.html` | 홈 카드 active 축소와 움직임 줄이기 조건 적용 | P39·P50 | 포함 후보 |
| 24 | [a17417e](https://github.com/jeongdahui731/MyProfile/commit/a17417e5870d135660916691f77ffdbe2255fa10) 학습 목표 영역 추가 | 2026-11-07T20:33:45+09:00 | `docs/work-log.md`<br>`site/assets/css/common/post-entry.css`<br>`site/themes/template/layouts/list.html` | 학습 목표 카드와 공통 카드 모양 추가 | P21·P72 | 포함 후보 |
| 25 | [4132a3d](https://github.com/jeongdahui731/MyProfile/commit/4132a3d61b4f8b5f79e156d88196594e5e26fc56) 기술 역량 영역 추가 | 2026-11-07T20:39:32+09:00 | `docs/work-log.md`<br>`site/themes/template/layouts/list.html` | 기술 역량 카드 및 두 카드 안내 문구 추가 | P21·P73 | 포함 후보 |
| 26 | [3e7afce](https://github.com/jeongdahui731/MyProfile/commit/3e7afce3e51bbebf5b73c827df3d1a8f8b7e92ab) 실제 활동 영역 추가 | 2026-11-07T20:41:55+09:00 | `docs/work-log.md`<br>`site/themes/template/layouts/list.html` | 실제 활동 안내 카드 추가 | P21·P60 | 포함 후보 |
| 27 | [68bf082](https://github.com/jeongdahui731/MyProfile/commit/68bf0821c862b88b5dec752a391514257adf3c6f) 학습 목표 영역 클릭 효과 | 2026-11-07T20:45:39+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/cards.css`<br>`site/themes/template/layouts/list.html` | 학습 목표 카드에 축소 효과 연결 | P39·P50 | 포함 후보 |
| 28 | [aa87c73](https://github.com/jeongdahui731/MyProfile/commit/aa87c73480579e00f27591f59e6faf4fc620d23c) 기술 역량 영역 클릭 효과 추가 | 2026-11-07T20:48:15+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/cards.css`<br>`site/themes/template/layouts/list.html` | 기술 역량 카드에 축소 효과 연결 | P39·P50 | 포함 후보 |
| 29 | [ff583f6](https://github.com/jeongdahui731/MyProfile/commit/ff583f64ea9c39389ae4122181126e704c2fac2a) 실제 활동 영역 클릭 효과 추가 | 2026-11-07T20:50:55+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/cards.css`<br>`site/themes/template/layouts/list.html` | 실제 활동 카드에 축소 효과 연결 | P39·P50 | 포함 후보 |
| 30 | [5da4559](https://github.com/jeongdahui731/MyProfile/commit/5da4559fe3eccb041ab77185dd4e3c591e792182) 학습 목표 연결 | 2026-11-07T20:54:42+09:00 | `docs/work-log.md`<br>`site/content/posts/learning-goals.md`<br>`site/themes/template/layouts/list.html` | 학습 목표 상세 파일 생성과 카드 링크 연결 | P21·P22 | 포함 후보 |
| 31 | [644d05f](https://github.com/jeongdahui731/MyProfile/commit/644d05fe016a497cee3ad55b07ab6e06a2ade774) 기술 역량 영역 연결 | 2026-11-07T20:57:58+09:00 | `docs/work-log.md`<br>`site/content/posts/skills.md`<br>`site/themes/template/layouts/list.html` | 기술 역량 상세 파일 생성과 카드 링크 연결 | P21·P22 | 포함 후보 |
| 32 | [1ab16fe](https://github.com/jeongdahui731/MyProfile/commit/1ab16fe629706cf72586b7b325722f85e79c6b1e) 실제 활동 영역 연결 | 2026-11-07T21:02:19+09:00 | `docs/work-log.md`<br>`site/assets/css/common/post-entry.css`<br>`site/assets/css/extended/cards.css`<br>`site/content/posts/activities.md`<br>`site/themes/template/layouts/list.html` | 실제 활동 상세 연결·세 카드 hover와 움직임 설정 보완 | P21·P22·P50 | 포함 후보 |
| 33 | [b49039b](https://github.com/jeongdahui731/MyProfile/commit/b49039b9a70a8f5d62a7622ba3d6c81702295197) 경로 위치 변경 및 추가 | 2026-11-07T21:05:32+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/interests.css`<br>`site/themes/template/layouts/single.html` | 경로 가로 위치 보정과 끝 구분 기호 추가 | P31·P32 | 포함 후보 |
| 34 | [45d2ad5](https://github.com/jeongdahui731/MyProfile/commit/45d2ad50d5ac85f08ae4334fdf93a57476bc19a1) 경로 새로고침 | 2026-11-07T21:10:57+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/interests.css`<br>`site/themes/template/layouts/single.html` | 현재 위치 버튼을 같은 페이지 링크로 변경 | P22·P25 | 포함 후보 |
| 35 | [bd23f34](https://github.com/jeongdahui731/MyProfile/commit/bd23f3403b9a3613d374da7d029aeae7912a8a6f) 학습 목표 경로 생성 | 2026-11-07T21:15:47+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/interests.css`<br>`site/content/posts/learning-goals.md` | 학습 목표에 공통 경로·제목 스타일 적용 | P22·P23 | 포함 후보 |
| 36 | [b755530](https://github.com/jeongdahui731/MyProfile/commit/b755530c51fd1a93062bfdbb23e80da73c3730db) 기술 역량 경로 생성 | 2026-11-07T21:18:22+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/interests.css`<br>`site/content/posts/skills.md` | 기술 역량에 공통 경로·제목 스타일 적용 | P22·P23 | 포함 후보 |
| 37 | [6801d12](https://github.com/jeongdahui731/MyProfile/commit/6801d1252e5704a29fb20acbef1b3bc985982f9a) 실제 활동 경로 생성 | 2026-11-07T21:22:10+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/interests.css`<br>`site/content/posts/activities.md` | 실제 활동에 공통 경로·제목 스타일 적용 | P22·P23 | 포함 후보 |
| 38 | [82465fe](https://github.com/jeongdahui731/MyProfile/commit/82465feb5ff920cb01150a6a3aad330c074dcc30) 학습 목표 상세 화면 구성 | 2026-11-07T21:29:06+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/learning-goals.css`<br>`site/content/posts/learning-goals.md`<br>`site/layouts/shortcodes/learning-goals.html` | 학습 목표의 공통 목록·글자·선 스타일과 shortcode 구현 | P47·P49 | 포함 후보 |
| 39 | [5953775](https://github.com/jeongdahui731/MyProfile/commit/5953775a11885a08a80c6adafc616e1870478cbc) 학습 목표 상세 화면에 학습 목표 추가 | 2026-11-07T21:33:25+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/learning-goals.css`<br>`site/layouts/shortcodes/learning-goals.html` | 학습 목표 제목 두 개와 h2 구조 작성 | P47·P72 | 포함 후보 |
| 40 | [dc5df5b](https://github.com/jeongdahui731/MyProfile/commit/dc5df5b9a8f3059748065b47a50d9fe00b295cb3) 학습 목표 상세 화면에 구체적인 실습 계획 내용 추가 | 2026-11-07T21:35:42+09:00 | `docs/work-log.md`<br>`site/layouts/shortcodes/learning-goals.html` | 두 목표의 구체적인 실행 계획 작성 | P72 | 포함 후보 |
| 41 | [22f70b9](https://github.com/jeongdahui731/MyProfile/commit/22f70b9c9f95ee396cbd42d86822fb01bce022bc) 학습 목표 상세 화면 회색 구분선 추가 | 2026-11-07T21:37:52+09:00 | `docs/work-log.md`<br>`site/layouts/shortcodes/learning-goals.html` | 목록 아래 가로 구분선 추가 | P47 | 포함 후보 |
| 42 | [da1103d](https://github.com/jeongdahui731/MyProfile/commit/da1103d283ce25c68093276b52e6c4014921b011) 학습 목표 상세 화면 수정 | 2026-11-07T21:42:17+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/learning-goals.css`<br>`site/layouts/shortcodes/learning-goals.html` | 선 굵기 변경과 내용에 맞는 세로선 높이 개선 | P31·P32 | 포함 후보 |
| 43 | [83405e4](https://github.com/jeongdahui731/MyProfile/commit/83405e4c1fa48c6b32164c9b5fe92d999a09bb94) 기술 역량 상세 화면 틀 생성 | 2026-11-07T21:49:07+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/skills.css`<br>`site/content/posts/skills.md`<br>`site/layouts/shortcodes/skills-outline.html` | 기술 역량 빈 틀 추가 | P47 | 제외 |
| 44 | [a4b188a](https://github.com/jeongdahui731/MyProfile/commit/a4b188a4fa96266d660d72b156f228c2009396d0) 기술 역량에 내용 추가 | 2026-11-07T21:51:41+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/skills.css`<br>`site/layouts/shortcodes/skills-outline.html` | 기술 역량 제목 작성과 임시 높이·접근성 숨김 제거 | P47·P73 | 포함 후보 |
| 45 | [afa5dbb](https://github.com/jeongdahui731/MyProfile/commit/afa5dbb41640d22060894ed7a7dd55f354a48e88) 기술 역량 상세 화면 사례 내용 추가 | 2026-11-07T21:54:19+09:00 | `docs/work-log.md`<br>`site/layouts/shortcodes/skills-outline.html` | 기술 역량의 실제 적용 사례 두 문단 작성 | P73 | 포함 후보 |
| 46 | [aacf70c](https://github.com/jeongdahui731/MyProfile/commit/aacf70cc91f232c5168aefd633d854e41f400baa) 관심 분야 틀 생성 | 2026-11-07T22:05:09+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/interests.css`<br>`site/content/posts/interests.md`<br>`site/layouts/shortcodes/interests-outline.html` | 관심 분야 빈 틀 추가 | P47 | 제외 |
| 47 | [b27fc93](https://github.com/jeongdahui731/MyProfile/commit/b27fc9379028e7f75daa1ba60e723d72264a3741) 관심 분야 상세 화면 내용 추가 | 2026-11-07T22:07:44+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/interests.css`<br>`site/layouts/shortcodes/interests-outline.html` | 웹 개발 제목 작성과 임시 높이·접근성 숨김 제거 | P47·P71 | 포함 후보 |
| 48 | [c95f212](https://github.com/jeongdahui731/MyProfile/commit/c95f212c10171aecb8c12ec9e295847b9bfcfc3e) 관심 분야 상세 화면 동기 추가 | 2026-11-07T22:10:04+09:00 | `docs/work-log.md`<br>`site/layouts/shortcodes/interests-outline.html` | 웹 개발 관심 계기 작성 | P71 | 포함 후보 |
| 49 | [92d94b1](https://github.com/jeongdahui731/MyProfile/commit/92d94b161c9df8f220e4781c2f8b21f546647938) 내용 수정 | 2026-11-07T22:15:36+09:00 | `docs/work-log.md`<br>`site/content/posts/interests.md`<br>`site/layouts/shortcodes/learning-goals.html`<br>`site/themes/template/layouts/list.html` | 홈 카드 설명과 미래 실행 계획 문체 정리 | P71~P73 | 포함 후보 |
| 50 | [0193af4](https://github.com/jeongdahui731/MyProfile/commit/0193af4effc2794cf67617d1931dbb64d45eef1a) 실제 활동 회색 카드 추가 | 2026-11-07T22:27:22+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/activities.css`<br>`site/content/posts/activities.md`<br>`site/layouts/shortcodes/activity-summary.html` | 실제 활동 정보 카드·날짜·진행 상태 작성 | P74 | 포함 후보 |
| 51 | [320e62a](https://github.com/jeongdahui731/MyProfile/commit/320e62a44ae73a9cb6302d54e9baef2f8782f09e) 실제 활동 영역 상세 화면 틀 생성 | 2026-11-07T22:31:21+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/activities.css`<br>`site/content/posts/activities.md`<br>`site/layouts/shortcodes/activity-outline.html` | 실제 활동 빈 틀 추가 | P47 | 제외 |
| 52 | [1fa5eba](https://github.com/jeongdahui731/MyProfile/commit/1fa5eba25bf93b2456a64116358db0a862001d6c) 실제 활동 상세 화면 제목 변경 | 2026-11-07T22:34:49+09:00 | `docs/work-log.md`<br>`site/content/posts/activities.md` | 실제 활동 h1을 구체적 활동명으로 변경 | P60 | 포함 후보 |
| 53 | [30815d2](https://github.com/jeongdahui731/MyProfile/commit/30815d2437807b01fc05bf621804947bdc128c18) 실제 활동 상세 화면 활동 형태 추가 | 2026-11-07T22:36:42+09:00 | `docs/work-log.md`<br>`site/layouts/shortcodes/activity-summary.html` | 개인 활동 형태 명시 | P76 | 포함 후보 |
| 54 | [076314d](https://github.com/jeongdahui731/MyProfile/commit/076314d81a52581e8fad2abc06dca819b4ba094a) 실제 활동 상세 화면 목차 추가 | 2026-11-07T22:38:56+09:00 | `docs/work-log.md`<br>`site/assets/css/extended/activities.css`<br>`site/layouts/shortcodes/activity-outline.html` | 실제 활동 다섯 제목 작성과 임시 스타일 제거 | P47 | 포함 후보 |
| 55 | [5f5b754](https://github.com/jeongdahui731/MyProfile/commit/5f5b754df8425c1c50311b78426ca0d924a1e83a) 실제 활동 상세 화면 내용 추가 | 2026-11-07T22:40:59+09:00 | `docs/work-log.md`<br>`site/layouts/shortcodes/activity-outline.html` | 활동 목적·역할·과정·결과·배운 점과 개선 설명 작성 | P75~P79 | 포함 후보 |
| 56 | [7b0256a](https://github.com/jeongdahui731/MyProfile/commit/7b0256aaeccb36da51c1bccc2e93c158ac58f24d) 실제 활동 활동 결과 추가 | 2026-11-07T22:56:45+09:00 | `docs/work-log.md`<br>`site/layouts/shortcodes/activity-summary.html`<br>`site/static/artifacts/profile-card/about-me.html`<br>`site/static/artifacts/profile-card/토트넘 로고.jpg` | 사용자 HTML·로고 산출물 복사와 결과 링크 연결 | P30·P78 | 포함 후보 |
| 57 | [67b8f36](https://github.com/jeongdahui731/MyProfile/commit/67b8f36bdb8782ab34d2006adbeb77c202efd4b1) 실제 활동 상세 화면 소스 코드 추가 | 2026-11-07T23:00:37+09:00 | `docs/work-log.md`<br>`site/layouts/shortcodes/activity-summary.html` | 동일 HTML의 GitHub 소스 링크 추가 | P30·P78 | 포함 후보 |
| 58 | [51df06f](https://github.com/jeongdahui731/MyProfile/commit/51df06f658bd6d48534e98d4ca4e4c9ecc3e1c8e) 상세 화면 내용 수정 | 2026-11-07T23:04:53+09:00 | `docs/work-log.md`<br>`site/layouts/shortcodes/activity-summary.html` | 두 자료 링크의 표시 문구 정리 | P30 | 포함 후보 |
| 59 | [c8da121](https://github.com/jeongdahui731/MyProfile/commit/c8da12131047bbe000cd8df1754f7030390acb40) README 보안 | 2026-11-07T23:12:14+09:00 | `README.md`<br>`docs/work-log.md` | 실제 설치·빌드·재배포·수정 위치·출처 README 작성 | P56~P58 | 포함 후보 |
| 60 | [a101400](https://github.com/jeongdahui731/MyProfile/commit/a101400b328151bb9fed86b930f6d72f780728d0) 공개 사이트 검증표와 화면 증거 정리 | 2026-11-08T01:14:43+09:00 | `docs/evidence/activity-390.jpg`<br>`docs/evidence/activity-detail.jpg`<br>`docs/evidence/artifact-390.jpg`<br>`docs/evidence/artifact-result.jpg`<br>`docs/evidence/deployment-check.json`<br>`docs/evidence/home-1440.jpg`<br>`docs/evidence/home-390.jpg`<br>`docs/evidence/home-768.jpg`<br>`docs/evidence/home-current.jpg`<br>`docs/evidence/home-dark.jpg`<br>`docs/evidence/keyboard-focus.jpg`<br>`docs/evidence/source-code.jpg`<br>`docs/verification.md`<br>`docs/work-log.md` | 실제 공개 검증표·캡처·배포 증거 작성 | P62·P64 | 포함 후보 |

## 집계 재현 명령

아래는 읽기 전용 명령이다. 최신 main이 바뀌어도 위 끝 SHA를 사용하면 동일한 후보 구간을 확인할 수 있다.

```powershell
git rev-list --count a101400b328151bb9fed86b930f6d72f780728d0
git log --reverse --format="%H %s" a101400b328151bb9fed86b930f6d72f780728d0
git show --stat 83405e4
git show --stat aacf70c
git show --stat 320e62a
git show 019a811 -- site
```

이 문서를 포함한 후속 커밋을 제출한다면 전체 후보·제외·유효 수와 끝 SHA·Actions를 다시 확인해야 한다. 이후 커밋을 이미 포함한 것으로 선계산하지 않았다.

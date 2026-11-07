# 공개 사이트 기능 검증 기록

## 대상 버전과 환경

- 사이트는 https://jeongdahui731.github.io/MyProfile/ 이다.
- 현재 원격 main은 `c8da12131047bbe000cd8df1754f7030390acb40`이며 2026년 11월 8일 01시 10분 56초 KST에 공개 GitHub API로 확인했다.
- 해당 커밋은 https://github.com/jeongdahui731/MyProfile/commit/c8da12131047bbe000cd8df1754f7030390acb40 이다.
- 같은 SHA의 push Actions는 completed / success다. 실행은 https://github.com/jeongdahui731/MyProfile/actions/runs/42380499015 이다. 원시 조회 결과는 `docs/evidence/deployment-check.json`이다.
- 브라우저 화면 검사는 2026년 11월 7일 23시 13분~23시 17분 KST에 시작했고, 소스 화면 캡처와 후속 확인은 11월 8일에 수행했다. 캡처 당시 원격 SHA를 매번 조회하지 않았으므로 각 그림의 SHA를 단정하지 않는다. 직전 확인한 `51df06f`와 현재 `c8da121` 사이에는 README와 작업 기록만 변경됐고 사이트 파일 차이는 없다.
- 자동 화면 검증 브라우저는 ChatGPT in-app browser다. 브라우저 엔진 버전은 도구에서 확인하지 못해 미표시다. OS는 Windows이며 앞서 레지스트리에서 25H2·빌드 26200.9711을 확인했다. OS 제품명은 별도 확인이 필요하다.
- 화면 폭은 CSS viewport 기준으로 1440px·768px·390px를 사용했다. 브라우저 도구의 저장 이미지 폭은 스크롤바·캡처 영역을 포함한 CSS viewport와 다르게 반환된 경우가 있어 아래에 실제 이미지 픽셀도 함께 적었다.
- 200% 확대는 사용자가 Edge에서 직접 확인했다고 이 채팅에서 답했다. 자동 검증과 구분한다. 사용자 브라우저 버전·정확한 검사 시각·확대 비율이 표시된 캡처는 미확보다.
- 기록 시각은 실제 수행일을 사용한다. 11월 8일 수행한 검사를 변경 공지의 마감인 11월 7일 23시 59분 이전에 수행한 것으로 소급하지 않는다.

## 실제 검사표

| 번호와 영역 | 기준 | 대상과 환경·시각 KST | 확인 동작과 예상 | 실제 결과 | 근거와 한계 |
| --- | --- | --- | --- | --- | --- |
| T01 배포 | P01·P02·P03·P04·P05·P07 | 공개 홈·저장소·Actions, API 11/8 01:10:56 | 비로그인 홈 접속, 공개 저장소 main과 같은 SHA의 push 실행 성공 확인 | 홈 화면 열람 성공. 공개 저장소, 원격 main SHA와 push / completed / success 확인 | `deployment-check.json`, 그림 1. API의 전체 실행 성공을 확인했으며 이 기록에서 각 job의 상세 로그는 별도로 저장하지 않았다. |
| T02 경로와 자산 | P11·P12·P17·P19·P20·P24 | `/MyProfile/posts/activities/`, IAB, 11/7 23:15~23:17, 768px·390px | 내부 주소 직접 열기, 스타일시트 적용·테마 버튼 조작·주요 참조 검사. 운영 하위 경로로 자산 로딩 예상 | 활동 제목·다섯 문단·회색 카드 표시. DOM에서 stylesheet의 sheet 존재, 로컬·file·HTTP 참조 없음 확인. 테마 전환 성공. 검사 당시 도구 오류·경고 로그 빈 목록 | 그림 4·5·9. 개발자 도구 Network와 캐시 제거를 이용한 전 자산 재검사는 미실시다. CSS 로딩 관찰과 DOM 참조 검사 범위의 결과다. |
| T03 메뉴와 이동 | P21·P22·P23·P25·P26 | 홈과 학습 목표 상세, IAB, 11/7 23:14~23:15 | 학습 목표 카드 클릭, 상세 새로고침, 경로 홈 클릭, 뒤로 가기. 올바른 내용·복귀 예상 | 학습 목표와 두 계획 표시. 새로고침 후 유지. 홈 이동과 뒤로 가기 후 학습 목표 복귀 확인 | 당시 DOM snapshot과 이 수행 채팅의 실제 도구 결과. 이번 기록은 각 동작의 별도 영상이나 화면을 확보하지 못했다. |
| T04 반응형 | P31·P32·P33·P34·P35·P36 | 홈과 활동 상세, IAB, 최종 캡처 11/7 23:17, 1440×1000·768×1000·390×844 | 홈에서 새로고침 없이 폭 변경, 모바일 카드 클릭, 긴 활동 제목 확인. 가로 넘침·조작 누락이 없어야 함 | 최종 재검사에서 1440px의 client/scroll 1425/1425, 390px의 375/375 확인. 768px 검사에서도 가로 넘침 없음. 모바일 메뉴는 두 번째 줄에 표시. 실제 활동 카드 이동과 긴 제목 줄바꿈 확인 | 그림 1~4. 초기에는 비활성 탭의 폭 적용이 불안정해 새 활성 탭에서 재검사했다. 상세 모바일 이미지의 오른쪽 경계는 캡처 영역과 viewport 차이가 있어 최종 보고서 사용 전 사용자 화면과 대조할 필요가 있다. |
| T05 키보드 | P41·P42·P43 | 홈과 관심 분야, IAB, 11/7 23:15 | 마우스 없이 Tab으로 로고→테마 버튼→Instagram→GitHub→관심 분야 카드 이동 후 Enter. 초점 표시와 정상 도착 예상 | 순서대로 도달했고 각 요소 outline이 auto로 관찰됨. 관심 분야 카드에서 Enter 실행 후 관심 분야 제목·설명 도착 확인 | 그림 6과 도구의 activeElement·URL 관찰. 초점 outline은 rgb(16,16,16) auto 0.666667px로 반환됐다. 모든 페이지의 끝까지 연속 Tab·Shift+Tab 검사는 미실시다. |
| T06 자료와 이미지 | P13·P14·P18·P30·P37·P78 | 실제 활동→결과 HTML, IAB, 11/7 23:16~23:17, 768px·390px | 결과 링크 클릭 후 로고 표시와 500px 이하 세로 배치 확인 | 결과 HTML 열림. 로고 complete=true·naturalWidth=960. 390px에서 profile flex-direction=column, client/scroll 390/390 확인 | 그림 7·8. 로고 alt를 DOM에서 확인했다. 버튼의 실제 누름 축소·색상 변화는 이번 브라우저 검사에서 재현하지 않았다. |
| T07 외부 소스 | P07·P28·P30·P78 | 실제 활동→GitHub blob, IAB, 클릭 11/7 23:17, 캡처 11/8 01:00:01 | about-me.html 링크가 공개 코드 페이지를 여는지 확인 | Sign in 링크가 있는 비로그인 GitHub 화면에서 main의 about-me.html 코드 내용과 Flexbox·500px 미디어 쿼리를 읽을 수 있었음 | 그림 10. GitHub 계정·Instagram 프로필 링크의 실제 외부 도착은 이번 검사에서 확인하지 않았다. |
| T08 확대 | P40 | 공개 홈, Edge, 사용자 직접 검사·11/8 대화 제공 | 200% 확대에서 글·링크·카드를 읽고 클릭할 수 있어야 함 | 사용자가 잘림 없음과 상단 링크·카드 정상 이동을 확인했다고 답함. 사용자 첨부 이미지에서 보이는 이름·소개·상단 링크·관심 분야·학습 목표 배치에 겹침이나 잘림 없음 | 사용자 제공 채팅 캡처. 화면에 200% 표시가 없고 아래 기술 역량·실제 활동 영역은 해당 이미지에 보이지 않는다. 검사 시각·브라우저 버전 미제공. AI의 Edge 제어는 URL 식별 제한으로 중단되어 직접 검증으로 기록하지 않는다. |

## 캡처 목록과 그림 설명

각 경로는 저장소 상대 경로다. 시각은 파일을 저장한 시각이며 일부 캡처는 직전 동작과 간격이 있다. 그림 번호는 최종 보고서 편집 시 전체 그림 순서에 맞춰 변경할 수 있다.

| 그림 | 설명 | URL | 저장 시각 KST | 검사 viewport | 실제 JPG 픽셀 | 파일 |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | 밝은 테마의 데스크톱 홈 | https://jeongdahui731.github.io/MyProfile/ | 2026-11-07 23:17:10 | 1440×1000 | 1424×1000 | `docs/evidence/home-1440.jpg` |
| 2 | 태블릿 홈 | https://jeongdahui731.github.io/MyProfile/ | 2026-11-07 23:17:10 | 768×1000 | 752×1000 | `docs/evidence/home-768.jpg` |
| 3 | 모바일 홈과 두 번째 줄 메뉴 | https://jeongdahui731.github.io/MyProfile/ | 2026-11-07 23:17:10 | 390×844·전체 페이지 | 390×928 | `docs/evidence/home-390.jpg` |
| 4 | 모바일 활동 상세·긴 제목·다섯 설명 | https://jeongdahui731.github.io/MyProfile/posts/activities/ | 2026-11-07 23:17:11 | 390×844·전체 페이지 | 374×1581 | `docs/evidence/activity-390.jpg` |
| 5 | 활동 상세 직접 접근 화면 | https://jeongdahui731.github.io/MyProfile/posts/activities/ | 2026-11-07 23:15:59 | 768×1000·전체 페이지 | 752×1204 | `docs/evidence/activity-detail.jpg` |
| 6 | 관심 분야 카드 키보드 초점 | https://jeongdahui731.github.io/MyProfile/ | 2026-11-07 23:15:47 | 768×1000 | 752×1000 | `docs/evidence/keyboard-focus.jpg` |
| 7 | 활동 산출물 프로필 카드 | https://jeongdahui731.github.io/MyProfile/artifacts/profile-card/about-me.html | 2026-11-07 23:16:09 | 768×1000 | 768×1000 | `docs/evidence/artifact-result.jpg` |
| 8 | 390px에서 산출물 세로 배치 | https://jeongdahui731.github.io/MyProfile/artifacts/profile-card/about-me.html | 2026-11-07 23:17:29 | 390×844 | 390×844 | `docs/evidence/artifact-390.jpg` |
| 9 | 어두운 테마 홈 | https://jeongdahui731.github.io/MyProfile/ | 2026-11-07 23:16:42 | 1440×1000 | 1424×1000 | `docs/evidence/home-dark.jpg` |
| 10 | 비로그인 GitHub 소스 표시 | https://github.com/jeongdahui731/MyProfile/blob/main/site/static/artifacts/profile-card/about-me.html | 2026-11-08 01:00:01 | 390×844 | 375×812 | `docs/evidence/source-code.jpg` |

`home-current.jpg`는 그림 1과 같은 구성을 추가 저장한 보조 파일이다. 최종 보고서에는 중복 삽입하지 않는다. 사용자의 200% 캡처는 채팅에 있으며 아직 저장소에 별도 파일로 보관하지 못했다.

## 남은 확인과 제출 한계

- 브라우저 버전과 정확한 OS 제품명, 사용자 200% 검사 시각·확대 비율 표시 캡처를 보완해야 한다.
- 캐시 없는 새 접속의 전체 Network 검사, 다른 브라우저, 잘못된 주소 처리, 모든 페이지의 연속 키보드·초점 가두기·200% 직접 동작은 미검증이다.
- 로고 원본 출처와 이용 조건, 로컬 새 환경 빌드 재현은 미확인이다.
- 이 문서는 실제 수행한 검사를 기록한 것이며 P01~P80 전체를 통과로 판정한 문서가 아니다. P51 최종 커밋 집계, P61~P70 최종 보고서와 AI 사례는 별도로 완료해야 한다.
- 사이트 코드 수정은 이번 작업에서 수행하지 않았다. 이 기록을 커밋하면 제출 SHA가 달라지므로 최종 보고서의 SHA와 Actions URL을 해당 커밋에 맞춰 갱신해야 한다.

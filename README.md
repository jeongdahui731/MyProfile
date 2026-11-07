# 정다희 개인 포트폴리오

컴퓨터인공지능학부 25학번 정다희의 소개, 관심 분야, 학습 목표, 기술 역량과 실제 활동을 정리한 Hugo PaperMod 사이트입니다.

- 공개 사이트는 https://jeongdahui731.github.io/MyProfile/ 입니다.
- 공개 저장소는 https://github.com/jeongdahui731/MyProfile 입니다.
- 제출 및 배포 브랜치는 `main`입니다.

## 설치와 도구 버전

이 저장소의 최상위 폴더에서 명령을 실행합니다. 실제 Hugo 사이트는 `site/`, 빌드 결과는 `public/`입니다.

| 도구 | 사용할 버전과 설치 방법 |
| --- | --- |
| Git | 작업 환경에서 2.55.0.windows.5를 확인했습니다. https://git-scm.com/downloads 에서 설치합니다. |
| Python | 3.12 계열을 사용합니다. 준비 스크립트는 3.9 이상이 필요합니다. https://www.python.org/downloads/ 에서 설치하고 실행 파일을 PATH에 추가합니다. |
| Hugo Extended | 0.167.0을 사용합니다. https://github.com/gohugoio/hugo/releases/tag/v0.167.0 에서 운영체제에 맞는 Extended 압축 파일을 받아 풀고 hugo 실행 파일의 폴더를 PATH에 추가합니다. |
| Go | Actions는 1.27.1을 지정합니다. https://go.dev/dl/ 에서 같은 버전을 설치할 수 있습니다. `site/go.mod`의 Go 선언은 1.25.0입니다. |

설치 후 새 터미널에서 다음 명령으로 확인합니다.

```powershell
git --version
python --version
hugo version
go version
```

`hugo version`에 `extended`가 포함되는지 확인합니다. Windows에서 `python`이 Microsoft Store 별칭으로만 연결되면 실제 Python 설치 경로를 PATH에 등록하거나 설치한 python.exe의 전체 경로를 사용합니다. 이 작업 환경에서는 Codex 번들 Python 3.12.14로 자료를 읽었고, 일반 python 별칭 실행은 실패했습니다.

Actions는 위 도구 외에 Node.js 24, Dart Sass 1.105.0을 설치하며 `.github/pages_build.py --dependencies`로 추가 CLI 도구를 준비합니다. 정확한 설치 명령과 버전은 `.github/workflows/hugo-pages.yml`에 있습니다. 현재 PaperMod의 테마별 npm 의존성 목록은 `.github-pages.json`에서 빈 배열입니다.

## 저장소 받기와 로컬 실행

새 환경에서는 다음과 같이 저장소를 받습니다. 기존 작업 폴더에서는 해당 폴더를 터미널에서 열어 사용합니다.

```powershell
git clone https://github.com/jeongdahui731/MyProfile.git
cd MyProfile
```

PaperMod와 필요한 사이트 파일은 저장소에 포함되어 있습니다. 이미 준비된 저장소이므로 초기 준비 스크립트를 다시 실행할 필요는 없습니다.

로컬 미리보기는 다음과 같이 실행합니다. localhost 주소는 미리보기 명령에만 사용하며 운영 baseURL은 `site/pages.json`에 설정되어 있습니다.

```powershell
cd site
hugo server --config pages.json --baseURL http://localhost:1313/MyProfile/ --appendPort=false
```

터미널에 표시된 주소를 열어 확인하고 Ctrl+C로 종료합니다. 이후 다음 명령으로 저장소 최상위로 돌아옵니다.

```powershell
cd ..
```

## 운영 빌드와 확인

저장소 최상위에서 제공 빌드 스크립트를 실행합니다.

```powershell
$env:HUGO_ENVIRONMENT = "production"
python .github/pages_build.py --build
Test-Path public/index.html
Test-Path public/posts/activities/index.html
Test-Path public/artifacts/profile-card/about-me.html
```

스크립트는 `site/pages.json`을 읽고 Hugo 빌드 후 `/MyProfile/` 자산 경로를 보정합니다. 세 파일 확인 명령은 정상 빌드 후 True를 반환해야 합니다. `public/`은 빌드 결과이며 `.gitignore`에서 제외합니다.

로컬 빌드 명령은 현재 작업 환경에서 Hugo가 PATH에 없어 미실행 상태입니다. 위 명령과 경로는 실제 스크립트·설정을 대조해 작성했습니다. Actions에서 동일한 `python .github/pages_build.py --build` 명령이 실행되며, README 작성 직전 커밋 `51df06f658bd6d48534e98d4ca4e4c9ecc3e1c8e`의 push 실행 성공을 확인했습니다. 실행 기록은 https://github.com/jeongdahui731/MyProfile/actions/runs/42379904043 입니다. 새 환경의 재현 검증은 별도로 기록해야 합니다.

## 수정할 파일 위치

| 수정 대상 | 파일 위치 |
| --- | --- |
| 사이트 제목·작성자·한국어·홈 이름과 소개 | `site/pages.json` |
| 홈 카드 구성과 상세 페이지 연결 | `site/themes/template/layouts/list.html` |
| 홈 소개의 제목과 문장 배치 | `site/layouts/_partials/home_info.html` |
| 상단 Instagram·GitHub 링크 | `site/themes/template/layouts/_partials/header.html` |
| 관심 분야·학습 목표·기술 역량·실제 활동의 페이지 설정 | `site/content/posts/interests.md`, `learning-goals.md`, `skills.md`, `activities.md` |
| 관심 분야 본문 | `site/layouts/shortcodes/interests-outline.html` |
| 학습 목표 본문 | `site/layouts/shortcodes/learning-goals.html` |
| 기술 역량 본문 | `site/layouts/shortcodes/skills-outline.html` |
| 활동 정보 카드와 활동 설명 | `site/layouts/shortcodes/activity-summary.html`, `activity-outline.html` |
| 소개·카드·경로·목록·활동 카드 스타일 | `site/assets/css/extended/` |
| 공통 배경색과 기존 카드 스타일 | `site/assets/css/core/theme-vars.css`, `site/assets/css/common/post-entry.css` |
| 실제 활동 산출물과 로고 | `site/static/artifacts/profile-card/` |
| 빌드 상태·준비 버전·운영 주소 | `.github-pages.json` |
| 자동 배포 | `.github/workflows/hugo-pages.yml` |
| 수행 중 변경과 검증 기록 | `docs/work-log.md` |

루트의 `assets/`와 `layouts/`는 원본 테마 자료입니다. 실제 배포에는 `site/`의 사이트 자산과 `site/themes/template/` 테마가 사용됩니다. 새 외부 자산을 넣을 때는 출처와 이용 조건도 기록합니다.

## 수정 후 재배포

변경 후 로컬 빌드 또는 미리보기로 확인하고, 변경 내용을 검토한 다음 관련 파일을 직접 선택해 커밋합니다. 아래 `git add`는 사이트 설정을 수정했을 때의 예시이며 작업한 파일에 맞게 선택합니다.

```powershell
git status
git diff --check
git diff
git add site/pages.json
git commit -m "실제 변경 내용을 설명하는 메시지"
git push origin main
```

GitHub Settings → Pages → Source는 GitHub Actions로 설정합니다. `main` push로 Deploy Hugo to GitHub Pages가 자동 실행됩니다. Actions에서 해당 커밋 SHA의 build와 deploy 성공을 확인한 뒤, 공개 홈과 수정한 내부 주소를 열어 결과를 확인합니다. 내부 주소 직접 열기·새로고침, 자산 로딩도 함께 검사합니다. 변경이 보이지 않으면 배포 SHA를 먼저 대조하고 브라우저 캐시를 새로고침합니다.

네트워크 시간 초과 등으로 실행이 실패하면 해당 실행을 재실행합니다. 실행 기록을 삭제한 경우 Actions의 Deploy Hugo to GitHub Pages에서 Run workflow로 `main`을 수동 실행할 수 있습니다. 수동 실행은 push 자동 실행을 확인한 기록과 구분해서 보고서에 기재합니다.

최종 보고서에는 최종 원격 main 전체 SHA·커밋 URL과 같은 SHA의 Actions URL·실제 상태를 기록합니다. 유효 커밋 수는 원본 등록 등 제외 대상을 검토한 뒤 확정합니다.

## 출처와 제작 구분

| 자료와 사용 위치 | 제작 구분 | 출처와 이용 조건 |
| --- | --- | --- |
| PaperMod 테마 | 외부 자료 | https://themes.gohugo.io/themes/hugo-papermod/ 및 https://github.com/adityatelange/hugo-PaperMod . 2026년 11월 7일 원본 저장소 Download ZIP으로 다운로드했다고 사용자가 확인했습니다. MIT 고지는 루트 `LICENSE`와 `site/themes/template/LICENSE`에 있습니다. |
| 준비·빌드 스크립트 | 수업 제공 자료 | 교수님 제공 prepare_github_pages.py v3.1. 배포용 복사본은 `.github/pages_build.py`입니다. 별도 라이선스 부여는 확인하지 않았습니다. |
| 프로필 카드 HTML | 사용자 제공 직접 제작 산출물 | 사용자가 제공한 `about-me.html`을 `site/static/artifacts/profile-card/about-me.html`에 복사했습니다. 본문 CSS도 이 파일에 포함됩니다. |
| 토트넘 로고 | 외부 이미지 | `site/static/artifacts/profile-card/토트넘 로고.jpg`. 사용자 원본 HTML이 참조한 이미지를 함께 복사했습니다. 원본 URL·권리자 이용 조건은 확인 대기입니다. 프로젝트의 MIT 고지를 이 이미지의 이용 허락으로 해석하지 않습니다. |
| 소개·관심 분야·목표·역량·활동 문안 | 사용자 제공 내용 및 AI 반영 도움 | 사용자가 제공한 사실과 문안을 이 수행용 Codex 채팅에서 사이트 파일에 반영했습니다. |
| 사이트별 템플릿·CSS·자료 연결·작업 기록 | AI 도움을 받은 사용자 과제 작업 | Codex가 실제 파일 수정·정적 검사를 도왔고, 사용자가 디자인·문구·단계별 적용을 선택하고 커밋·push를 수행했습니다. 실제 화면 직접 검증은 별도 증거로 기록합니다. |

AI는 기준 분석·계획, 설정·코드·문구 반영, 오류 원인 확인과 정적 검사, README 작성에도 사용했습니다. AI 도움을 받은 부분과 사용자의 판단·수행·직접 검증을 최종 보고서에서 구분합니다. 사용 모델의 정확한 이름은 이 저장소에서 확인할 수 없어 미표시로 기록합니다.

## PaperMod 원본 안내

# Hugo PaperMod

**A fast, clean, and responsive theme for [Hugo](https://gohugo.io/).**

[![hugo-papermod](https://img.shields.io/badge/Hugo--Themes-@PaperMod-blue)](https://themes.gohugo.io/themes/hugo-papermod/)
[![Minimum Hugo Version](https://img.shields.io/static/v1?label=Hugo&message=v0.158.0%2B&color=blue&logo=hugo)](https://github.com/gohugoio/hugo/releases/tag/v0.158.0)
[![Discord](https://img.shields.io/discord/971046860317921340?label=Discord&logo=discord)](https://discord.gg/ahpmTvhVmp)

> Based on [hugo-paper](https://github.com/nanxiaobei/hugo-paper/tree/4330c8b12aa48bfdecbcad6ad66145f679a430b3), with additional features and customization options.

<table>
	<tbody>
		<tr>
			<td>Live Demo</td>
			<td><a href="https://adityatelange.github.io/hugo-PaperMod/">adityatelange.github.io/hugo-PaperMod</a></td>
		</tr>
		<tr>
			<td>Documentation 📚</td>
			<td><a href="https://github.com/adityatelange/hugo-PaperMod/wiki">Github Wiki</a></td>
		</tr>
		<tr>
			<td>Example Site Source</td>
			<td><a href="https://github.com/adityatelange/hugo-PaperMod/tree/exampleSite">exampleSite branch</a></td>
		</tr>
		<tr>
			<td><a href="https://www.star-history.com/adityatelange/hugo-papermod"><img src="https://api.star-history.com/badge?repo=adityatelange/hugo-PaperMod&amp;theme=dark" alt="Star History Rank" /></a></td>
			<td><a href="https://ko-fi.com/H2H229ZWH"><img src="https://ko-fi.com/img/githubbutton_sm.svg" alt="ko-fi" /></a></td>
		</tr>
	</tbody>
</table>


<p align="center">
  <img src="https://user-images.githubusercontent.com/21258296/114303440-bfc0ae80-9aeb-11eb-8cfa-48a4bb385a6d.png" alt="Mockup image" title="Mockup"/>
</p>

---

## Features 💥

`☄️ Fast | ☁️ Fluent | 🌙 Smooth | 📱 Responsive`

- **Asset pipeline** -- Hugo's built-in asset generator with fingerprinting, bundling, and minification.
- **Three layout modes** -- [Regular](https://github.com/adityatelange/hugo-PaperMod/wiki/Features#regular-mode-default-mode), [Home-Info](https://github.com/adityatelange/hugo-PaperMod/wiki/Features#home-info-mode), and [Profile](https://github.com/adityatelange/hugo-PaperMod/wiki/Features#profile-mode).
- **Light and dark themes** -- Automatic switching based on browser preference, plus a manual toggle.
- **Multilingual support** -- Includes a built-in language selector.
- **Search** -- Client-side search powered by Fuse.js.
- **SEO optimized** -- Open Graph, Twitter Cards, and Schema.org structured data out of the box.
- **Cover images** -- Per-post cover images with responsive image support.
- **Table of contents** -- Auto-generated from heading structure.
- **Multiple authors** -- Native support for multi-author sites.
- **Social icons and share buttons** -- Configurable social links and per-post sharing.
- **Breadcrumb navigation**
- **Post archives and taxonomies**
- **Code block copy buttons** -- One-click copying with Chroma syntax highlighting.
- **Related post suggestions**
- **Zero JS build dependencies** -- No webpack, Node.js, or other tooling required.

| Topic                                                                                             | Description                                     |
| ------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| **[Installation guide](https://github.com/adityatelange/hugo-PaperMod/wiki/Installation)**        | Detailed installation and update instructions   |
| **[Features wiki page](https://github.com/adityatelange/hugo-PaperMod/wiki/Features)**            | In-depth explanations of all features           |
| **[FAQ wiki](https://github.com/adityatelange/hugo-PaperMod/wiki/FAQs)**                          | Common questions and configuration walkthroughs |
| **[Icons wiki](https://github.com/adityatelange/hugo-PaperMod/wiki/Icons)**                       | Documentation for social icons and share icons  |
| **[Variables wiki](https://github.com/adityatelange/hugo-PaperMod/wiki/Variables)**               | List of all available template variables        |
| **[Overiding templates](https://github.com/adityatelange/hugo-PaperMod/wiki/Template_Overrides)** | Guide to customizing templates without forking  |
| **[Releases](https://github.com/adityatelange/hugo-PaperMod/releases)**                           | Detailed history of releases                    |

---

## Performance ☄️

PaperMod consistently scores near-perfect results on [Pagespeed Insights](https://pagespeed.web.dev/report?url=https://adityatelange.github.io/hugo-PaperMod/).

<img width="481" height="116" alt="image" src="https://github.com/user-attachments/assets/497d831b-d143-4a46-bc11-b1d7f8ef4a83" />

---

## Support 🫶

- Star this repository to show your support.
- Share PaperMod with others who might find it useful.
- Sponsor the project on [GitHub Sponsors](https://github.com/sponsors/adityatelange) or [Ko-Fi](https://ko-fi.com/adityatelange).

---

## Special Thanks 🌟

- [Highlight.js](https://github.com/highlightjs/highlight.js)
- [Fuse.js](https://github.com/krisk/fuse)
- [Feather Icons](https://github.com/feathericons/feather)
- [Simple Icons](https://github.com/simple-icons/simple-icons)
- All contributors and supporters

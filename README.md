# MyWebpage: 개인 포트폴리오 사이트

컴퓨터인공지능학부인 제 개인 포트폴리오 사이트입니다. Hugo와 Stacknote 테마로 만들어 GitHub Pages로 공개했습니다.

- 사이트: https://alsdk4570.github.io/MyWebpage/
- 저장소: https://github.com/alsdk4570/MyWebpage


## 필요한 도구와 버전

배포용 워크플로(`.github/workflows/hugo-pages.yml`)에 지정된 버전입니다.

| 도구 | 버전 |
|---|---|
| Hugo (extended) | 0.167.0 (테마 요구: 0.160.0 이상) |
| Dart Sass | 1.105.0 |
| Go | 1.27.1 |
| Node.js | 24 |
| Python | 3.12 |

Hugo는 반드시 extended 버전이어야 합니다. 설치는 [Hugo 공식 설치 안내](https://gohugo.io/installation/)를 따릅니다.


## 사이트 빌드와 확인

main 브랜치에 push하면 GitHub Actions가 위 도구를 설치하고 `python .github/pages_build.py --build`로 사이트를 빌드해 배포합니다. 결과는 저장소의 Actions 탭에서 확인합니다.


## 수정하고 다시 배포하는 방법

1. 아래 표의 파일을 수정하고 저장합니다.
2. `git add`, `git commit`, `git push`로 main에 올립니다.
3. 저장소의 Actions 탭에서 실행이 초록 체크(성공)인지 확인합니다.
4. 공개 주소를 `Ctrl+F5`로 새로고침해 바뀐 화면을 확인합니다.

| 바꿀 내용 | 파일 |
|---|---|
| 사이트 제목, 소개 문구, 메뉴, 링크 | `site/config.yaml` |
| 글 | `site/content/articles/*.md` |
| 소개 페이지 | `site/content/about.md` |
| 화면의 고정 문구 | `site/themes/template/i18n/en.yaml` |
| 푸터와 화면 구조 | `site/themes/template/layouts/` |
| 배포 설정 (수정하지 않음) | `.github/` |


## 글 작성 시 주의할 점

- 글 파일 맨 위의 `---` 두 줄과 `title`, `date`, `tags` 형식이 틀리면 빌드가 실패합니다.
- 오늘보다 뒤 날짜(배포 서버 기준 UTC)의 글은 사이트에 나타나지 않습니다.
- 태그는 같은 이름이 2개 이상의 글에 붙어야 화면에 나타납니다.


## 출처와 이용 조건

- 테마: [Stacknote](https://github.com/myimilo/hugo-theme-stacknote), 제작 Long Wang, MIT License (`site/themes/template/LICENSE`)
- 사이트 생성 도구: [Hugo](https://gohugo.io/)
- 배포 준비 스크립트(`.github/pages_build.py`): 수업에서 제공받은 도구로 생성
- 글, 설정, 문구 수정: 직접 작성 (AI 도움 범위는 제출 보고서에 기록)

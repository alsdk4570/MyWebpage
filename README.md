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


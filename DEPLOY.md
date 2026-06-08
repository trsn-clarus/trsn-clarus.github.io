# Clarus 사이트 GitHub Pages 배포 방법

이 사이트는 정적 사이트라서 `index.html`, `zh.html`, `styles.css`, `script.js`, `assets/`만 올리면 바로 배포할 수 있습니다.

## 현재 상태

- GitHub 계정: `trsn-clarus`
- 추천 저장소 이름: `trsn-clarus.github.io`
- 배포 후 기본 주소: `https://trsn-clarus.github.io`
- 중국어 페이지 주소: `https://trsn-clarus.github.io/zh.html`
- 업로드용 ZIP: `../clarus-github-pages-deploy.zip`

## GitHub 웹에서 배포하기

1. GitHub에서 새 저장소를 만듭니다.
   - Repository name: `trsn-clarus.github.io`
   - Public 선택
   - README는 만들어도 되고 안 만들어도 됩니다.
2. 저장소 화면에서 `Add file > Upload files`를 누릅니다.
3. `clarus-github-pages-deploy.zip` 압축을 풀고, 압축 안의 파일들을 저장소 루트에 업로드합니다.
   - 중요한 점: `portfolio-site` 폴더 자체를 올리는 것이 아니라, 그 안의 `index.html`, `zh.html`, `styles.css`, `assets/` 등이 저장소 최상단에 있어야 합니다.
4. `Commit changes`를 누릅니다.
5. 저장소 `Settings > Pages`로 이동합니다.
6. `Build and deployment > Source`를 `Deploy from a branch`로 설정합니다.
7. Branch를 `main`, folder를 `/root`로 선택하고 저장합니다.
8. 몇 분 후 `https://trsn-clarus.github.io`에서 사이트가 열립니다.

## Codex가 직접 배포하려면 필요한 것

현재 이 PC에는 `git`과 `gh`가 설치되어 있지 않습니다. 자동 배포를 맡기려면 아래 둘 중 하나가 필요합니다.

1. PC에 Git과 GitHub CLI 설치 후 로그인
   - Git: https://git-scm.com/downloads
   - GitHub CLI: https://cli.github.com/
   - 설치 후 PowerShell에서 `gh auth login`
2. GitHub 웹에서 저장소를 먼저 만들고, Codex GitHub 앱이 그 저장소에 접근할 수 있도록 설치 범위를 허용

## `www.` 주소를 쓰려면 필요한 것

1. 도메인 구매: 예를 들어 `clarus-minsoo.com`
2. DNS 설정:
   - `www` 레코드: 호스팅 서비스가 안내하는 CNAME 값으로 연결
   - 루트 도메인도 쓰려면 `A`, `ALIAS`, 또는 `ANAME` 설정이 필요할 수 있음
3. 예시 주소:
   - `https://www.clarus-minsoo.com`
   - `https://clarus-minsoo.com`

도메인 이름이 정해지면 `CNAME` 파일과 DNS 설정값까지 맞춰서 준비하면 됩니다.

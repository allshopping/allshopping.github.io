# Hugo Starter (PaperMod + GitHub Pages)

## 1) 새 계정에서 블로그 저장소 생성
- 저장소 이름: `allshopping.github.io`
- Public 저장소로 생성

## 2) 이 폴더 내용 복사
- 이 `hugo-starter` 폴더 내용을 새 저장소 루트에 복사

## 3) PaperMod 테마 연결
다음 명령을 새 저장소에서 실행:

```bash
git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
```

## 4) GitHub Pages 활성화
- 저장소 Settings → Pages
- Source: `GitHub Actions`

## 5) 배포 확인
- `main` 브랜치에 푸시하면 `.github/workflows/hugo-pages.yml`가 자동 배포
- 접속 주소: `https://allshopping.github.io/`

## 6) 이 자동화 저장소 시크릿 설정
자동 포스팅 워크플로우가 새 Hugo 저장소에 쓰도록 아래 시크릿을 설정:

- `MY_BLOG_USERNAME`: allshopping
- `MY_BLOG_REPO`: allshopping.github.io
- `MY_BLOG_TOKEN`: 새계정 PAT (`repo` 권한)
- `MY_BLOG_BRANCH`: `main`
- `MY_BLOG_ENGINE`: `hugo`
- `MY_BLOG_BASE_URL`: `https://allshopping.github.io`
- `MY_BLOG_POSTS_PATH`: `posts`

이후 이 저장소의 `GitHub Blog Auto Post` 워크플로우를 실행하면
`content/posts/*.md`로 자동 업로드됩니다.

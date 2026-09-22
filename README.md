# ung / research notes

Overleaf에서 작성한 연구 노트 PDF를 GitHub Pages로 공개하는 작은 정적 블로그입니다. 빌드 도구나 CMS 없이 `index.html`과 PDF 파일만 사용합니다.

## 글 올리기

1. Overleaf에서 문서를 PDF로 내려받습니다.
2. PDF를 `pdf/` 폴더에 넣습니다.
3. `index.html`의 해당 노트에서 `PDF 준비 중`을 PDF 링크로 바꿉니다.

예시:

```html
<a class="file-state" href="./pdf/fast-treeshap.pdf">PDF ↗</a>
```

파일명은 영문 소문자와 하이픈을 사용하는 것을 권장합니다.

## 배포

`main` 브랜치에 push하면 `.github/workflows/publish.yml`이 루트의 정적 파일을 GitHub Pages에 배포합니다. 저장소 Settings → Pages에서 Source를 **GitHub Actions**로 설정하면 됩니다.

기존 Quarto 원본은 `legacy-quarto/`에 보관해 두었습니다. PDF로 옮긴 뒤 필요 없으면 삭제해도 됩니다.

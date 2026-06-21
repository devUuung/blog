# Research Notes

Quarto로 만든 연구 노트 블로그입니다.

## Local commands

```bash
quarto render
```

정적 사이트를 `_site/`에 생성합니다.

```bash
quarto preview . --no-browser --port 4321
```

로컬 미리보기를 실행합니다. 브라우저에서 <http://localhost:4321/>을 열면 됩니다.

## Writing posts

새 글은 `posts/` 아래에 폴더를 만들고 `index.qmd`를 추가합니다.

```text
posts/
  my-topic/
    index.qmd
```

글의 기본 front matter 예시는 다음과 같습니다.

```yaml
---
title: "글 제목"
description: "짧은 설명"
author: "Ungsik Kim"
date: "2026-06-21"
categories: [theory, paper]
---
```

## Deployment

`.github/workflows/publish.yml`은 GitHub Pages 배포용 워크플로입니다.

1. GitHub에 새 저장소를 만듭니다.
2. 이 폴더를 remote에 연결하고 `main` 브랜치로 push합니다.
3. 저장소 Settings > Pages에서 Source를 GitHub Actions로 설정합니다.
4. `_quarto.yml`의 `website.site-url`과 GitHub 링크를 실제 주소로 바꿉니다.

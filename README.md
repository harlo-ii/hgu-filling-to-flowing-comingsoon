# FILLING TO FLOWING — Coming Soon

2026 한동대학교 콘텐츠융합디자인학부 졸업작품전 웹사이트 공개 전 대기 페이지.
전시 개막(2026.11.04 10:00 KST)까지 카운트다운과 로딩 바를 보여준다.

- 페이지: `public/index.html` (단일 파일, 빌드 없음)
- 개막 시각·로딩 바 시작일: `index.html` 하단 스크립트의 `OPEN_AT`, `LOADING_FROM`
- 푸터 이미지 (Figma Footer Black `1807:14180`) — `public/assets/`
  - `footer-subvisual.png` — 마블링 서브비주얼 원본. CSS 로 -90° 회전·크롭해서 쓴다
  - `footer-logos.png` — 로고 스프라이트. HGU 워드마크·심볼 부분만 CSS 로 잘라 쓴다

## 로컬 확인

```bash
npx wrangler dev
```

## 배포 (Cloudflare Workers 정적 에셋)

1. Cloudflare 대시보드 → Workers & Pages → Create → Import a repository → 이 레포 선택
2. Build command: 비움 / Deploy command: `npx wrangler deploy`
3. 배포 후 Settings → Domains & Routes 에서 전시 도메인 연결

본 사이트(`hgu-filling-to-flowing`)를 오픈할 때 도메인을 그쪽 Worker 로 옮기면 된다.

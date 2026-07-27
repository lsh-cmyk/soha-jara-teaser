# 소하 (Soha) 티저 페이지 프로젝트

## 목표
- `index.html` 단일 파일을 GitHub 레포에 push
- Vercel GitHub 연동으로 자동 배포

## 레포 정보
- GitHub: `lsh-cmyk/soha-jara-teaser`
- 브랜치: `main`
- 배포 URL: Vercel (GitHub 연동)

## 파일 구성
- `index.html` — 소하 티저 페이지 (단일 파일, 전체 포함)
  - 앨범 커버: Suno CDN 이미지 (`image_large_e5376f2c-af73-4183-848c-241bb95b7d03.jpeg`)
  - 프로필 사진: base64 임베드 (기타 든 20대 초반 여성)
  - 가사: 전체 8섹션 (Intro / Verse 1 / Pre-Chorus / Chorus / Verse 2 / Chorus / Bridge / Outro)
  - 오디오: Suno 링크 (`https://suno.com/song/e5376f2c-af73-4183-848c-241bb95b7d03`)
  - 색상 테마: `--cream: #FAF6F0`, `--brown: #3A2E20`, `--amber: #C4956A`, `--sage: #7A9E7E`

## 작업 순서
1. `git init` (또는 기존 레포 clone)
2. `index.html`, `CLAUDE.md` 추가
3. `git push origin main`
4. Vercel에서 `lsh-cmyk/soha-jara-teaser` import → 배포

## 주의사항
- 앨범 커버는 Suno에 적용하지 말 것 (이미 완료, 재작업 금지)
- 단일 파일 구조 유지 (CSS/JS 분리하지 말 것)

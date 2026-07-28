# 소하 (Soha) 티저 페이지 프로젝트

## 목표
- `index.html` 단일 파일을 GitHub 레포에 push
- Vercel GitHub 연동으로 자동 배포

## 레포 정보
- GitHub: `lsh-cmyk/soha-jara-teaser`
- 브랜치: `main`
- 배포 URL: Vercel (GitHub 연동)

## 파일 구성
- `index.html` — 소하 티저 페이지 (CSS/JS 인라인, 미디어 base64 임베드)
  - 앨범 커버: base64 임베드 (수채화 새싹 + "자라나 / NECTORIAL" 텍스트 포함)
  - 프로필 사진: base64 임베드
  - 오디오: base64 임베드 (2:06). ID3 태그는 제거 후 재작성됨
  - 가사: Part.1 / Part.2 두 박스, 줄 단위 자동 하이라이트 (총 26줄)
  - 색상 테마: `--cream: #FAF6F0`, `--brown: #3A2E20`, `--amber: #C4956A`, `--sage: #7A9E7E`, `--petal: #E8B4B8`
  - 폰트: Cormorant Garamond + Noto Serif KR + Nanum Pen Script(손글씨)
- `cover.jpg` — og:image 전용 (1200x1200, 280KB). data URI는 SNS 크롤러가 못 읽어서 별도 파일 필요

## 페이지 섹션 순서
Hero → 앨범커버 → Listen Now(플레이어) → 가사 → 프레스 인용 → Release·Credits → Discography → Live → Artist(바이오/손글씨 노트/근황/구독) → Footer(스트리밍 링크)

## 콘셉트 설정 (AI 스터디 과제용 가상 설정)
- "소하"는 가상의 인디 싱어송라이터. **AI 생성 곡이라는 사실은 페이지에 드러내지 않는다**
- 크레딧·유통사·공연장·매체명은 전부 가상 (달선 레코드, 새벽 스튜디오, Foliage Sound, 월간 사운드테이블, 연남동 브릭홀 등)
- 스트리밍/SNS 버튼은 실제 링크 없이 "발매와 함께 공개됩니다" 토스트로 처리

## 인터랙티브 요소
- 스크롤 연동 배경 (상단 새벽 톤 → 하단 햇빛 톤, `--dawn`/`--day` CSS 변수)
- 스티키 미니 플레이어 (플레이어 섹션이 화면 밖으로 나가면 상단 고정)
- 가사 줄 클릭 → 캔버스로 공유 카드 PNG 생성·저장
- 앨범 커버 마우스 틸트, 배경 꽃잎 (재생 중 진해짐)

## 작업 순서
1. `git init` (또는 기존 레포 clone)
2. `index.html`, `CLAUDE.md` 추가
3. `git push origin main`
4. Vercel에서 `lsh-cmyk/soha-jara-teaser` import → 배포

## 주의사항
- 앨범 커버는 Suno에 적용하지 말 것 (이미 완료, 재작업 금지)
- CSS/JS는 `index.html` 안에 인라인 유지 (분리하지 말 것)
- **Suno 흔적을 다시 넣지 말 것** — 링크·크레딧·mp3 ID3 태그 모두 제거된 상태
- `og:image`는 반드시 실제 호스팅 URL(`cover.jpg`)로 유지. data URI로 되돌리면 공유 카드가 깨짐
- 곡 길이는 하드코딩하지 말 것 (오디오 메타데이터에서 자동 계산됨)

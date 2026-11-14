# oakhillever-web — 옥성환 대표님 회사 소개 사이트

## 배경
- 이전 회사 대표님(옥성환 대표님)의 회사 소개 사이트. platform7351이 협업자로 구축을 돕는다.
- 모든 계정(GitHub, Cloudflare, Supabase, 도메인)은 **대표님 명의**. 나는 멤버/협업자로 초대받아 작업한다.
- 게시판·CMS 없는 **정적 사이트**(HTML/CSS/JS). 빌드 과정 없음, 서버 없음.

## 저장소
- 원격: https://github.com/oakhillever-web/-1 (대표님 소유), 기본 브랜치 `main`
- 저장소 이름이 `-1`이라 로컬 폴더명은 `oakhillever-web`.
- git 사용자는 이 저장소 로컬 설정으로 `platform7351 <platform7351@users.noreply.github.com>`을 쓴다.

## 구조
```
index.html             원페이지: 히어로 / 회사소개(#about) / 사업분야(#business) / 연혁(#history) / 오시는 길(#contact)
404.html               없는 주소용 페이지
assets/css/style.css   스타일 (Pretendard 폰트 CDN, 메인 색 #1f4e3d, 모바일 대응 720px)
assets/js/main.js      모바일 메뉴 토글, 푸터 연도
assets/img/favicon.svg 임시 파비콘
_headers               Cloudflare Pages 보안·캐시 헤더
robots.txt             검색 허용
```
- 회사명, 문구, 연락처, 사업자번호는 전부 **자리표시용**. 실제 내용은 아직 받지 못했다. 임의로 지어내지 않는다.

## 배포 (Cloudflare Pages)
- 계정: "Oakhillever@gmail.com's Account" (나는 멤버)
- Pages ↔ GitHub 연결은 **대표님이 직접** 한다 (GitHub 앱 설치가 저장소 소유자 권한).
- 설정: Framework preset None / Build command 비움 / Output directory `/` / Production branch `main`
- 연결 후에는 main 푸시 = 자동 배포. 푸시 전에 로컬 확인을 끝낸다.

## 대기 중
- 대표님: Pages ↔ GitHub 연결, Supabase 조직 생성 후 초대, 도메인 정보·로고·참고 사이트 전달
- 나: 회사명, 업종, 소개 문구, 메뉴 확정 후 내용 반영

## Supabase (문의 폼을 넣을 때만)
- RLS를 반드시 켠다.
- 프론트에는 anon/publishable 키만 쓴다. **service_role 키 금지.**

## 규칙
- 비밀번호, API 키, 토큰은 절대 저장소에 커밋하지 않는다.
- 저장소 설명이 "출판사의 책 저장 금고만들기"로 되어 있음. 회사 사이트 용도로 써도 되는지 대표님 확인 전. **저장소 설명·이름 변경은 platform7351이 지시할 때만.**
- 커밋은 작은 단위로, 한국어 메시지로.
- 디자인을 바꾸면 로컬에서 `python -m http.server 8000`으로 띄워 http://localhost:8000 에서 확인한다.
- README의 "진행 현황" 체크리스트를 작업에 맞춰 갱신한다.

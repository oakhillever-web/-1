# 회사 웹사이트

빌드 과정이 없는 정적 사이트입니다. Cloudflare Pages로 배포합니다.

## 구조

```
index.html          메인 페이지 (회사소개, 사업분야, 연혁, 오시는 길)
404.html            없는 주소로 들어왔을 때 보이는 페이지
assets/css/         스타일
assets/js/          모바일 메뉴 등 스크립트
assets/img/         로고, 이미지, 파비콘
_headers            Cloudflare Pages 보안·캐시 헤더
robots.txt          검색엔진 수집 허용
```

## 로컬에서 보기

```
python -m http.server 8000
```

브라우저에서 http://localhost:8000 을 엽니다.

## Cloudflare Pages 배포 설정

- Workers & Pages → Create → Pages → Connect to Git → 이 저장소 선택
- Framework preset: None
- Build command: (비워 둠)
- Build output directory: `/`
- Production branch: `main`

main에 푸시하면 자동으로 배포됩니다.

## 진행 현황
- [x] 사이트 기본 구조 (자리표시용 문구)
- [ ] 실제 회사 정보와 문구 반영
- [ ] Cloudflare Pages 연결
- [ ] 도메인 연결
- [ ] 문의 폼 (필요 시 Supabase)

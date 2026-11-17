# 콘텐츠 스튜디오

블로그(워드프레스 또는 정적 블로그) + 인스타 + 스레드 글을 AI로 만들고, 내가 승인하면 정해진 시간에 자동으로 올리는 프로그램이에요.

- 처음 설정 순서: 함께 받은 '콘텐츠 스튜디오 시작 매뉴얼'을 위에서부터 따라 해요.
- 구조와 기능 설명: STUDIO.md
- 비밀키(키, 토큰, 비밀번호)는 이 저장소 Settings > Secrets and variables > Actions 에만 넣어요. 파일에 적지 않아요.
- 사이트 추가: 관리화면 > 사이트 > 새 사이트 (sites/_template/site.json 이 틀이에요)
- 새 글 검색엔진 알림(IndexNow): sites/<사이트>/site.json 의 indexnow_key 설명 참고


## 속보 트랙 (선택)
- sites/<id>/site.json 의 issue_track.enabled 를 true 로, queries 에 이 사이트 주제 검색어를 넣어요
- 한국 7~23시 매시간 뜨는 이슈를 확인해 스레드 글을 승인 대기에 올려요. 승인하면 바로 올라가요
- 휴대폰 알림: ntfy 앱 설치 → 주제 구독 → 그 주제 이름을 비밀키 NTFY_TOPIC 에. 관리화면 주소는 비밀키 STUDIO_URL 에
- 인스타는 카드를 세로 영상(릴스)으로 올려요. 카드뉴스로 올리려면 instagram.format 을 "carousel" 로

## 사이트 고정 형식 (선택)
- site.json 의 signature 를 "myth_check"(흔히 듣는 말과 공식 기준 대조표, 건강·생활 정보) 또는 "verdict"(쟁점 판정표와 법안 단계, 시사·정치)로 두면 글마다 첫 소제목 앞에 들어가요

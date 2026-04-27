# YouTube API 가이드 스크린샷

이 폴더에 아래 파일명과 일치하게 스크린샷을 저장하면 `youtube-api-guide.html` 에 자동으로 표시됩니다.

없는 파일은 플레이스홀더(점선 박스)로 대체되어 페이지는 정상 동작합니다. 시간 날 때 하나씩 채우면 됩니다.

## 필요한 스크린샷 (8장)

| 파일명 | 내용 | 찍는 시점 |
|--------|------|-----------|
| `step1-new-project.png` | "새 프로젝트" 생성 대화상자 | 상단 드롭다운 → "새 프로젝트" 클릭 직후 |
| `step2-enable-api.png` | YouTube Data API v3 페이지 ("사용" 버튼 보이게) | 라이브러리에서 검색 후 결과 페이지 |
| `step3-1-get-started.png` | "Google 인증 플랫폼이 아직 구성되지 않음" + 시작하기 버튼 | OAuth 동의 화면 진입 직후 |
| `step4-wizard.png` | 마법사 화면 (앱 정보 입력창 / 대상 선택 / 연락처 등 중 하나) | 시작하기 누른 직후 1~4단계 중 어느 것이든 |
| `step5-test-users.png` | "대상" 탭의 테스트 사용자 섹션 (+ 추가 버튼 보이게) | 앱 구성 완료 후 대상 탭 |
| `step6-create-client.png` | OAuth 클라이언트 생성 대화상자 ("데스크톱 앱" 유형) 또는 생성 완료 팝업 | 클라이언트 탭 → 만들기 클릭 후 |
| `step7-register-in-app.png` | Cozy Uploader 설정 탭의 "YouTube API 인증 파일" 섹션 | 앱 설정 탭 열어서 |
| `step8-advanced-warning.png` | "Google 에서 이 앱을 확인하지 않았습니다" 경고 화면 + 고급 링크 | OAuth 연결할 때 브라우저 경고 |

## 권장 사양

- 포맷: PNG (PIL 품질 손실 없음)
- 너비: 1000~1600px (반응형 자동 축소됨)
- 개인정보 마스킹: 이메일, 프로젝트 ID 등 민감 정보는 흐리게 처리 (Windows 캡처 도구의 형광펜 기능 활용)

## 찍는 법

1. Windows `Win + Shift + S` → 영역 선택
2. 그림판 등 열고 `Ctrl + V` 붙여넣기
3. 개인정보 마스킹 (있으면)
4. 위 파일명으로 `images/guide/` 에 저장
5. `git add`, `commit`, `push` 하면 홈페이지에 반영

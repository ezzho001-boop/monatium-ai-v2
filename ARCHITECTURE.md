# 모나티엄AI v2 구조

```
brain/       판단, 대화 전략, 개인화 규칙
main-core/   요청 수명주기와 모듈 조율
actions/     일정·할 일·문서 등 실행 가능한 작업
security/    권한 확인, 민감정보 보호, 감사 기록
network/     모델 API와 외부 서비스 연결
memory/      사용자 설정과 대화·지식 저장소
ui/          웹 화면과 사용자 입력
config/      환경별 설정과 기능 플래그
tests/       모듈 단위 및 통합 검증
```

실행 권한은 항상 `main-core`가 요청하고 `security`가 검증한 뒤 `actions`가 수행합니다.

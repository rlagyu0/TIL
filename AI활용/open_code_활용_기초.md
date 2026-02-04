# oh-my-opencode

### open code

`scoop` 설치

```jsx
irm get.scoop.sh | iex
scoop --version
```

관리자 권한 PowerShell에서 실행했기 때문 실행 정책 관련 오류

```jsx
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

`scoop` 저장소 추가 및 오픈 코드 설치

```jsx
scoop bucket add extras
scoop install extras/opencode
```

### oh-my-opencode

`bunx`명령어를 사용해 설치하는 것을 권장하고 있어서 bun을 먼저 설치한다. 아래 명령어로 bun을 설치한다.

```jsx
powershell -c "irm bun.sh/install.ps1|iex"
bunx oh-my-opencode install
```

### 프로젝트 셋팅

`init` 프로젝트 루트 폴더에서 초기화 작업

- 에이전트 md 파일 자동으로 생

**oh my code** int command

```jsx
Install and configure oh-my-opencode by following the instructions here:
https://raw.githubusercontent.com/code-yeongyu/oh-my-opencode/refs/heads/master/docs/guide/installation.md
```

`ulw` **oh-my-opencode의 모든 기능(워크플로우/자동화/프리셋)** 이 활성화

- 병렬 에이전트 실행
- 백그라운드 작업 활성화
- Todo Continuation Enforcer 작동
- 전문 에이전트 자동 위임
- 완료까지 지속 실행

### 설정

```jsx
# 글로벌 설정 디렉토리 (모든 프로젝트에 적용)
~/.config/opencode/
├── opencode.json           # 플러그인 및 provider 설정
├── oh-my-opencode.json     # 에이전트별 모델 매핑
└── antigravity-accounts.json

# 인증 정보 디렉토리
~/.local/share/opencode/
└── auth.json               # API 키 및 인증 정보

# 프로젝트별 설정 (글로벌 설정을 override)
프로젝트루트/.opencode/
└── oh-my-opencode.json     # 해당 프로젝트에만 적용
```

- 특정 프로젝트만 설정이 필요하면 루트에 json 파일 생성
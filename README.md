# .github

GitHub 조직 [horon-ai](https://github.com/horon-ai)의 공개 프로필 저장소입니다. 실행 코드를 담지 않고 조직 Overview에 보이는 소개 페이지와 브랜드 이미지만 담습니다.

GitHub은 이름이 `.github`인 저장소의 [`profile/README.md`](profile/README.md)를 조직 첫 화면에 그대로 그립니다. 그래서 이 저장소의 산출물은 소개 문서 하나와 그 문서가 참조하는 이미지입니다.

## 구성

| 경로 | 역할 |
| --- | --- |
| [`profile/README.md`](profile/README.md) | 조직 Overview 본문. 조직 소개, 구성 표, 철학, 시작 안내 |
| `profile/assets/banner.png` | Overview 상단 배너 |
| `profile/assets/horon-wave.png` | 마스코트 이미지 |
| `profile/assets/horon-icon.png`, `horon-wordmark.png`, `horon-avatar.png` | 조직 아이콘, 워드마크, 아바타 |

## 고칠 때

- 조직 첫 화면 본문은 [`profile/README.md`](profile/README.md) 하나만 고칩니다. GitHub이 그 파일만 읽습니다.
- 이미지는 `profile/assets/`에 두고 본문에서도 `assets/banner.png`처럼 `profile/` 기준 상대 경로로 참조합니다. 루트 절대 경로나 외부 이미지 주소를 쓰면 Overview에서 깨집니다.
- 제품과 저장소 서술은 실제 코드·매니페스트와 맞춰 적습니다. 현재 공개 프로필이 다루는 구성은 세 가지입니다.
  - [`agent`](https://github.com/horon-ai/agent): Rust 2024 에이전트 백엔드(`horon-agent`, `horon-tui`). 공개 저장소이며 문서는 [agent.horon.ai](https://agent.horon.ai)에 있습니다.
  - [`design`](https://github.com/horon-ai/design): 디자인 토큰(`@horon-ai/tokens`)과 React·Expo 컴포넌트(`@horon-ai/react`, `@horon-ai/expo`) 모노레포(TypeScript, Bun, Turborepo). 공개 저장소이며 문서는 [design.horon.ai](https://design.horon.ai)에 있습니다.
  - Horon 앱: Expo + React Native 클라이언트(`ai.horon.app`)와 자체 API(Hono + Bun + Postgres). 저장소는 비공개이므로 공개 준비 중으로만 표기합니다.
- 공개 조직 프로필이므로 내부 경로, 비밀키, 비공개 저장소 이름·주소, 개인 정보를 넣지 않습니다.
- `.omo/`와 `.hyper/`는 하네스 작업 상태와 도구 산출물이므로 저장소에 올리지 않습니다([`.gitignore`](.gitignore)).

## 확인

이 저장소에는 별도 빌드나 테스트가 없으며 기본 브랜치는 `main`입니다. 수정 뒤에는 상대 이미지 경로와 외부 링크가 모두 열리는지 확인하고 [조직 페이지](https://github.com/horon-ai)에서 렌더 결과를 점검합니다.

# 태산 (taesan)

> 티끌 모아 태산

AI 에이전트와 일하면서 만든 스킬, 에이전트, 그 밖의 도구를 모아 두는 곳입니다.

## 구성

| 폴더 | 내용 |
|---|---|
| [`skills/`](skills) | Claude Code 등에서 쓰는 에이전트 스킬 (SKILL.md 형식) |

에이전트 정의 등 다른 종류는 생기는 대로 폴더를 추가합니다.

## 스킬

### [interview](skills/interview)

막연한 아이디어나 작업 요청을 인터뷰로 파고들어, AI 에이전트가 추가 질문 없이 실행할 수 있는 스펙 파일로 만듭니다.

- **이슈 트리와 진행률**: 정해야 할 것을 트리로 먼저 보여주고, 해소될 때마다 진행률을 갱신합니다. 언제 끝나는지 알 수 있습니다.
- **조사로 알 수 있는 건 묻지 않음**: 사실은 에이전트가 찾고, 사용자에게는 결정만 묻습니다.
- **깊은 질문은 하나씩, 빠른 결정은 묶어서**: 가설을 먼저 내놓고 그것이 틀릴 수 있는 지점을 묻습니다.
- **압박 검증**: 전제 확인, 반대 논거, 사전 부검, 이해관계자 관점 검토(멀티에이전트).
- **독립 감사**: 대화를 보지 못한 에이전트가 스펙만 읽고 막히는 지점을 보고합니다.

설치:

```bash
git clone https://github.com/HSUNEH/taesan.git
cp -r taesan/skills/interview ~/.claude/skills/
```

Claude Code에서 `/interview` 또는 "나랑 인터뷰하면서 구체화하자"처럼 요청하면 실행됩니다.

참고한 것:

- [Q00/ouroboros](https://github.com/Q00/ouroboros): 사실과 결정의 분리, 되말하기
- [prekuter/dryforge](https://github.com/prekuter/dryforge): 열거와 질문의 분리, 질문의 근거 요건, 독립 감사
- [obra/superpowers](https://github.com/obra/superpowers): 왜를 알기 전에는 열린 질문, 출처 구분
- [mattpocock/skills](https://github.com/mattpocock/skills): 선행 결정이 끝난 질문만 묶어 묻기
- [garrytan/gstack](https://github.com/garrytan/gstack): 전제 확인, 입장을 가진 인터뷰어
- [github/spec-kit](https://github.com/github/spec-kit): 질문마다 왜 묻는지 밝히기
- 맥킨지식 문제 해결: 문제 정의, MECE 이슈 트리, 가설 주도 접근

###`목차`
[1. commit log 카테고리화](#commit-log-카테고리화)
[2. 기능목록](#기능목록)

<br>

## commit log 카테고리화

- **feat**: 기능 구현 (기능 추가, 삭제)
- **fix**: 기능 수정 (처리하지 않은 케이스 발견해 수정)
- **refactor**: 코드 개선 (확장 가능하게, 작게 쪼개기 등)
- **docs**: 문서 수정 (README .md)
- **style**: 디자인 요소(.css), 코드 스타일(Prettier, ESLint)

참고 - [AngularJS Commit Message Conventions](https://gist.github.com/stephenparish/9941e89d80e2bc58a153#allowed-type)

<br>

## 기능목록

- [ ] 게임 시작 시, 난수 3개를 생성한다.
- [ ] input에 제출된 값이 게임에 이용할 수 있는 값인지 확인한다.
  - [ ] 개수확인: 3개인지
  - [ ] 타입확인: 숫자인지
  - [ ] 중복확인: 중복된 수가 있는지
- [ ] 잘못된 입력값 인지하고 수정할 수 있게 alert 메시지를 띄운다.
- [ ] 난수와 비교한 결과값을 볼, 스트라이크를 이용해 보여준다.
- [ ] 생성된 난수와 동일할 경우, 정답 메시지와 재시작 버튼을 보여준다.
- [ ] 재시작 버튼을 누를 경우, 게임이 다시 시작된다.

<br>
### 작동흐름
**생각하게 된 배경**  
기능목록에 어떤 걸 적어야할지 감이 잡히지 않아서 생각해보게 되었습니다.

**1.** 난수 생성
**2.** 확인버튼 클릭 시, input으로 제출된 값 유효한지 체크
**2.1 유효하다면**, 난수와 비교해 결과값 제공

- 결과값이 3 스트라이크라면, 정답을 맞췄다는 메시지와 게임 재시작 버튼 제공
  - 게임 재시작 버튼을 눌렀을 경우만, 1로 돌아감(play 난수 생성)
- 결과값이 3 스트라이크가 아니라면, 게임 계속 진행

**2.2 유효하지 않다면**, 유효하지 않은 이유를 alert로 제공 & 게임 계속 진행
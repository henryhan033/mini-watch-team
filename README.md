# Mini Watch Day5 시작 코드

Day4 본문 6교시에서 완성한 코드를 새 Day5 폴더로 받아 사용한다.

- general: Flask/Jinja2 일반 게시판.
- monitor/backend: 계정 확인, 관찰 메모 CRUD, 요청 기록 수집·조회 API.
- monitor/frontend: React/Vite 감시 대시보드와 분리된 컴포넌트·API 모듈.

## 새 Day5 폴더로 받기

VS Code에서 C:\work 같은 상위 폴더를 열고 새 CMD에서 실행한다.

```text
git clone --branch day05-start https://github.com/zeroskill2400/mini-watch.git mini-watch-day05
```

받은 mini-watch-day05 폴더를 VS Code로 열고 새 CMD를 연다. 먼저 시작 브랜치를 확인한다.

```text
git status
```

1~3교시는 짧은 문서로 Git 협업을 연습한다. 공통 기준은 받은 이름 그대로 day05-start를 사용한다.

- 1교시: 내 PC에서 민수·지연 역할을 번갈아 맡는다. 같은 기준에서 feature/minsu와 feature/jiyun을 만들고, 각자 문서를 커밋한다. 브랜치를 오가며 비교한 뒤 day05-start에 두 작업을 병합한다.
- 2교시: 한 PC·한 계정으로 두 역할을 맡는다. 기존 mini-watch-day05는 민수 폴더로 쓰고, 공통 기준을 올린 내 GitHub 저장소를 mini-watch-day05-jiyun에 clone해 지윤 폴더를 먼저 준비한다. 민수가 점검표를 작성·commit·push하고 PR을 제출·보완해 Open 상태로 마친다.
- 3교시: 민수 PR을 확인·병합한 뒤 지윤 폴더의 기준에서 pull한다. 지윤도 최신 기준에서 다음 작업·새 PR을 진행하고 병합 결과를 민수가 받는다. 두 폴더의 day05-start를 맞춰 마치며 같은 줄의 충돌 해결은 추가 실습으로 둔다.

브랜치를 만들기 전에 현재 브랜치를 확인하고, 전환하기 전에 수정 내용을 커밋한다. 병합할 때는 작업을 받을 브랜치로 먼저 이동한다. 명령과 전체 파일 내용은 각 교안의 순서대로 진행한다.

민수 폴더는 내 실습 원격을 team으로 추가하고 강사 origin을 남긴다. 지윤 폴더는 내 실습 저장소에서 clone하므로 origin이 내 실습 주소다. 민수의 team과 지윤의 origin은 같은 주소이며 학생 변경을 강사 저장소로 push하지 않는다. 1~3교시는 서버와 DB를 켜지 않아도 된다. 2교시의 지윤 폴더는 협업을 위한 추가 clone이며, 4교시는 최신 기준을 받은 기존 mini-watch-day05에서 이어간다.

4~6교시는 같은 feature/next-notes 브랜치에서 Next.js를 배우고 메모 CRUD를 완성한다. 기존 React/Vite 앱은 남겨 두고 monitor/next-frontend를 새로 만든다.

- 4교시: Next.js의 뜻과 React와의 관계, 페이지·공통 레이아웃·Link·클라이언트 버튼.
- 5교시: 기존 Flask API와 rewrites로 연결하고 메모 목록 조회·등록.
- 6교시: 선택한 메모 수정·삭제, 취소·오류·DB 결과 확인, lint·build·실행 후 혼자 PR 검토·병합·pull.

Next.js 화면은 3000, Flask API는 5200에서 실행한다. 프로젝트 생성과 단계별 전체 파일 내용은 각 교안의 순서대로 진행한다.

## 다음 교시로 이어갈 상태

감시 로그인은 Flask의 DB 계정 확인 후 React state로 화면을 전환한다. 새로고침하면 로그인 폼으로 돌아오며, 이 로컬 학습판은 서버 API의 세션 접근 보호를 포함하지 않는다.

앱을 실행할 때는 서비스별로 .env·가상환경과 npm 의존성을 준비한다. 기존 general_db·monitor_db는 그대로 사용하며, Git clone은 실제 DB 데이터를 복사하지 않는다. SQL·설정 예시는 각 서버 폴더에 있다.

쿠키·세션 확장 부록 완성본은 별도의 day04-session 브랜치에서 받을 수 있다.

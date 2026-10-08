# Mini Watch Day5 Next.js 시작 코드

4~6교시 Next.js 실습의 출발점인 Day4 본문 완료 코드다.

- general: Flask/Jinja2 일반 게시판.
- monitor/backend: 계정 확인, 관찰 메모 CRUD, 요청 기록 API.
- monitor/frontend: React/Vite 감시 대시보드.

## 새 폴더로 받기

VS Code에서 실습 폴더를 둘 상위 폴더를 열고 새 CMD에서 실행한다. --branch day05-start는 오늘의 앱 시작 브랜치를 고른다.

```text
git clone --branch day05-start https://github.com/zeroskill2400/mini-watch.git mini-watch-day05
```

받은 mini-watch-day05를 VS Code로 열고 새 CMD에서 Next.js 작업 브랜치를 만든다. 같은 이름의 폴더가 이미 있으면 clone 명령의 마지막 폴더 이름을 바꾸고 실제 받은 폴더를 연다.

```text
git status
git switch -c feature/next-notes
```

## 4~6교시 진행

기존 React/Vite 앱 옆에 monitor/next-frontend를 추가하고 같은 feature/next-notes에서 이어간다.

- 4교시: Next.js 정의, React와의 관계, 페이지·공통 틀·Link·버튼.
- 5교시: 기존 Flask API 연결, 메모 조회·등록.
- 6교시: 메모 수정·삭제, 취소·오류·DB 결과 확인, lint·build·실행, 최종 커밋.

Next.js는 3000, Flask API는 5200에서 실행한다. 단계별 전체 파일 내용은 각 교안에 있다.

1~3교시 Git 협업은 별도의 새 git-practice 저장소에서 main과 origin으로 연습한다. 그 문서나 브랜치를 이 앱 폴더로 옮길 필요는 없다.

## 실행 준비

서비스별 .env·가상환경과 npm 의존성을 준비한다. 기존 general_db·monitor_db를 사용하며 Git clone은 실제 DB 데이터를 복사하지 않는다. SQL·설정 예시는 각 서버 폴더에 있다.

감시 로그인은 Flask의 DB 계정 확인 후 React state로 화면을 전환한다. 새로고침하면 로그인 폼으로 돌아오며 이 로컬 학습판은 서버 API의 세션 접근 보호를 포함하지 않는다.

쿠키·세션 확장 부록은 별도의 day04-session 브랜치에서 받을 수 있다.

# 클라이언트

## 개발 개요
OTT 플랫폼(Netflix)을 새롭게 개발한 OTT 플랫폼 서비스입니다.

## 팀원
- **Developer**: 김병찬, 김민서
- **Project Manager**: 김민서
- **Data Collector, QA**: 홍석환

### 업무
- **김민서**: 홈/메인/프로필 페이지, REST API, UI/UX 디자인 및 구현, 프로젝트 가이드라인, 코딩 표준 정의
- **김병찬**: 로그인 페이지, 데이터 유효성, 무결성 처리, 회원가입 처리, UI/UX 구현
- **홍석환**: UI/UX 테스트, 성능 테스트, 버그 리포트 및 기록, 데이터 수집

## 개발 스택
- **디자인**: Figma, Clip Studio
- **개발 환경**: VSCode
- **프로그래밍 언어**: HTML, CSS, TypeScript
- **프레임워크/라이브러리**: React, TailwindCSS, SWR, Axios, React Router DOM
- **버전 관리**: Git, GitHub
- **커뮤니케이션**: Notion, KakaoTalk

## 개발 기간 및 기획

### 개발 기간
- **디자인**: 6/29 ~ 7/1
- **가이드라인 구축**: 7/1 ~ 7/3
- **정적 페이지**: 7/3 ~ 7/14
- **REST API**: 7/14 ~ 7/21
- **UX 구현**: 7/21 ~ 7/29
- **빌드 및 배포**: 7/29 ~ 7/31
- **유지보수**: 7/31 ~ 8/3
- **문서화 및 피드백**: 8/3 ~ 8/6

### 기획
- **페이지**: 홈, 로그인, 메인, 프로필, 에러
- **디렉토리 구조**:
  - `public/`: 정적 파일을 보관하는 폴더
    - `image/`: 이미지 파일을 보관하는 폴더
  - `src/`: 소스 코드를 관리하는 폴더
    - `components/`: 각 구조의 컴포넌트를 관리하는 폴더
    - `pages/`: 각 페이지를 관리하는 폴더
    - `services/`: REST API 함수를 관리하는 폴더
    - `events/`: 모든 이벤트 핸들러를 관리하는 폴더
    - `styles/`: 사용자 정의의 유틸리티 스타일 속성을 관리하는 폴더
    - `types/`: 모든 타입 정의를 관리하는 폴더
    - `utils/`: 모든 유틸리티 함수 및 에러 처리, 데이터 무결성+유효성 등을 관리하는 폴더
    - `data/`: 클라이언트 측 정적 데이터 및 시드 데이터를 정의하고 관리하는 폴더
- **코딩 표준**:
  - `atom`: 재사용 가능한 리프 노드를 정의합니다.
  - `molecule`: 리프 노드의 집합을 정의합니다.
  - `cluster`: 리프 노드의 집합인 `molecule` 집합을 정의하며 페이지 컴포넌트의 하위 노드로 정의됩니다.

## 페이지
- **홈 (Home)**: 웹 서비스의 초기 화면입니다.
- **로그인 (Login)**: 로그인 서비스 및 회원가입 시스템을 제공합니다.
- **메인 (Main)**: 계정 서비스를 통해 OTT 플랫폼의 콘텐츠를 제공합니다.
- **프로필 (Profile)**: 계정 서비스 통해 OTT 플랫폼의 계정 관련 서비스를 제공합니다.
- **에러 (Error)**: 클라이언트 측 에러 발생 시 지원되는 안내 페이지입니다.

## 테스트 (에러 처리, 버전 관리)

| 테스트 케이스 ID | 제목                         | 목표                                                  | 전제 조건                                       | 입력 데이터                                  | 예상 결과                                              | 실제 결과                   | 상태         |
|------------------|------------------------------|-----------------------------------------------------|------------------------------------------------|----------------------------------------------|--------------------------------------------------------|------------------------------|--------------|
| TC001            | 로그인 기능 확인              | 사용자가 올바른 자격 증명을 입력할 때 로그인할 수 있는지 확인 | 사용자 계정이 존재하고 활성화되어 있어야 한다. | 사용자 ID: `testuser`<br>비밀번호: `Test@1234` | 사용자가 성공적으로 로그인되며, 대시보드 페이지로 리다이렉트된다. | (테스트 실행 후 결과 입력) | (테스트 성공/실패) |
| TC002            | 잘못된 비밀번호 입력 시 에러 메시지 확인 | 사용자가 잘못된 비밀번호를 입력할 때 적절한 에러 메시지가 표시되는지 확인 | 사용자 계정이 존재하고 활성화되어 있어야 한다. | 사용자 ID: `testuser`<br>비밀번호: `WrongPassword` | "잘못된 비밀번호입니다."라는 에러 메시지가 표시된다.  | (테스트 실행 후 결과 입력) | (테스트 성공/실패) |
| TC003            | 비어있는 필드로 로그인 시 에러 메시지 확인 | 로그인 필드가 비어 있을 때 적절한 에러 메시지가 표시되는지 확인 | 사용자 계정이 존재하고 활성화되어 있어야 한다. | 사용자 ID: (빈 값)<br>비밀번호: (빈 값) | "사용자 ID와 비밀번호를 입력해 주세요."라는 에러 메시지가 표시된다. | (테스트 실행 후 결과 입력) | (테스트 성공/실패) |



- 홈
- 로그인
- 메인
- 프로필
- 에러

## 참고 자료 및 출처
- **디자인**: 
  - YouTube: [https://www.youtube.com](https://www.youtube.com)
  - Netflix: [https://www.netflix.com/kr/](https://www.netflix.com/kr/)
- **UI/UX**: 
  - Netflix: [https://www.netflix.com/kr/](https://www.netflix.com/kr/)
- **데이터**: 
  - YouTube: [https://www.youtube.com](https://www.youtube.com)
  - Netflix: [https://www.netflix.com/kr/](https://www.netflix.com/kr/)
  - 나무위키: [https://namu.wiki](https://namu.wiki)
  - Pinterest: [https://kr.pinterest.com/](https://kr.pinterest.com/)

## FAQ 및 마무리

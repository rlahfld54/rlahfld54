# Excel Automation Workspace

> Excel/CSV 업무 파일을 열고, 검증하고, 자동화 작업까지 한 화면에서 처리하는 데스크톱형 데이터 작업 공간입니다.

안녕하세요. 사용자에게 안정감 있는 UI와 실무에 가까운 흐름을 제공하는 풀스택 개발자를 목표로 프로젝트를 만들고 있습니다.

이 프로젝트는 단순한 관리자 대시보드가 아니라, 사무 사용자가 매일 반복하는 Excel 정리, 코드 매핑, 중복 검사, 백업, 보고서 생성 작업을 하나의 워크스페이스 안에서 자연스럽게 처리하도록 설계한 React + Electron 기반 앱입니다.

<p>
  <img src="https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react&logoColor=111111" alt="React" />
  <img src="https://img.shields.io/badge/Vite-6-646CFF?style=for-the-badge&logo=vite&logoColor=ffffff" alt="Vite" />
  <img src="https://img.shields.io/badge/Electron-Desktop-47848F?style=for-the-badge&logo=electron&logoColor=ffffff" alt="Electron" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-4-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=ffffff" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/ExcelJS-4.4-217346?style=for-the-badge&logo=microsoftexcel&logoColor=ffffff" alt="ExcelJS" />
  <img src="https://img.shields.io/badge/SQLite-ready-003B57?style=for-the-badge&logo=sqlite&logoColor=ffffff" alt="SQLite" />
</p>

<img width="1904" height="914" alt="기본 초안" src="https://github.com/user-attachments/assets/957035f1-c853-434a-b1b4-55a60bf4f330" />



## Contact

<p>
  <a href="mailto:rlahfld54@naver.com">
    <img src="https://img.shields.io/badge/Email-rlahfld54%40naver.com-EA4335?style=for-the-badge&logo=gmail&logoColor=ffffff" alt="Email" />
  </a>
  <a href="https://normal-gom-jelly.tistory.com">
    <img src="https://img.shields.io/badge/Blog-normal--gom--jelly-FF5A4A?style=for-the-badge&logo=tistory&logoColor=ffffff" alt="Blog" />
  </a>
  <a href="https://github.com/rlahfld54">
    <img src="https://img.shields.io/badge/GitHub-rlahfld54-181717?style=for-the-badge&logo=github&logoColor=ffffff" alt="GitHub" />
  </a>
</p>

## 프로젝트 한 줄 소개

반복적인 엑셀 업무를 줄이기 위해, 파일 탐색, 스프레드시트형 데이터 검토, 자동화 실행, 로그 확인, 백업 상태를 한 화면에서 다루는 업무용 데스크톱 앱입니다.

## 왜 만들었나요?

실무에서 Excel 파일은 여전히 많이 쓰이지만, 데이터 정리 과정은 자주 흩어집니다.

- 파일을 열고
- 누락값과 중복을 찾고
- 거래처 코드나 품목 코드를 맞추고
- 결과를 저장하거나 백업하고
- 문제가 생기면 로그를 다시 확인하는 흐름

이 과정을 여러 도구 사이에서 왔다 갔다 하지 않고, 하나의 작업 공간 안에서 처리할 수 있게 만드는 것이 목표입니다.

## 포트폴리오에서 보여주고 싶은 점

이 프로젝트는 화려한 랜딩 페이지보다, 실제 사용자가 매일 반복하는 업무를 덜 피곤하게 만드는 도구에 가깝습니다.

저는 이 프로젝트를 통해 다음 역량을 보여주고 싶습니다.

- 사용자의 업무 흐름을 화면 구조로 바꾸는 능력
- React 컴포넌트를 재사용 가능한 업무 단위로 정리하는 능력
- 데스크톱 앱, 파일 처리, 로컬 저장소까지 고려하는 제품 설계 감각
- 작은 기능도 실제 서비스처럼 보이게 다듬는 UI 구현 능력

## 주요 기능

| 영역 | 구현 방향 |
| --- | --- |
| Dashboard | 현재 파일, 자동화 상태, 검증 결과를 요약해서 보여주는 첫 화면 |
| Excel-like Grid | 행 번호, 시트 탭, 고정 헤더, 상태 칩을 포함한 스프레드시트형 테이블 |
| Automation Queue | 데이터 정리, 코드 매핑, 중복 검사, 보고서 생성 흐름 표시 |
| Workspace Explorer | 최근 파일, 고정 파일, 백업 버전을 한쪽 패널에서 확인 |
| Logs & Status | 실시간 작업 로그, 오류/경고, 선택 셀, 인코딩, 자동 저장 상태 표시 |
| Module Pages | 파일 관리, 자동화, 데이터 테이블, 백업, 설정, 관리자 메뉴 확장 |

## 화면 구성

현재 첫 화면은 업무자가 바로 사용할 수 있는 도구처럼 보이도록 구성했습니다.

- 왼쪽 사이드바: 프로젝트, 데이터, 백업, 설정, 관리자 메뉴
- 상단 툴바: 업로드, 저장, 실행, 실행 취소, 다시 실행, 자동 저장 상태
- 중앙 영역: Excel 스타일 데이터 그리드
- 오른쪽 패널: 작업 탐색기와 자동화 큐
- 하단 영역: 로그, 상태 바, 파일 메타 정보

## 기술 스택

### Frontend

- React 19
- React Router
- Tailwind CSS 4
- Chart.js
- AG Grid
- Radix UI

### Desktop & Data

- Electron
- Vite
- ExcelJS
- xlsx
- better-sqlite3
- Zustand

### 개발 포인트

- 템플릿형 카드 대시보드를 실제 업무용 워크스페이스 구조로 재설계
- 여러 메뉴가 같은 품질로 보이도록 공통 업무 화면 컴포넌트 구성
- Excel/CSV 자동화 앱에 필요한 탐색기, 큐, 로그, 상태 바 흐름 설계
- 비개발자 사무 사용자가 이해하기 쉬운 정보 구조를 우선 적용



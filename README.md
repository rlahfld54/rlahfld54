# Excel Automation Workspace

> 반복적인 Excel 마감 업무를 데이터 검증부터 보고서 작성과 발송까지 연결한 데스크톱 업무 자동화 앱입니다.

안녕하세요. 사용자의 실제 업무 흐름을 이해하고, 복잡한 과정을 안정적인 UI로 풀어내는 풀스택 개발자를 목표로 하고 있습니다.

이 프로젝트는 단순한 관리자 대시보드가 아닙니다.  
매출 자료 취합, 오류 검증, 코드 매핑, 거래처 확인, 마감장 생성, 보고서 작성처럼 여러 도구에 흩어진 업무를 하나의 워크스페이스에서 처리할 수 있도록 설계한 **React + Electron 기반 데스크톱 애플리케이션**입니다.

<img width="1920" height="1040" alt="포트폴리오 화면" src="https://github.com/user-attachments/assets/96576302-50ab-46b6-bbaf-bd0a5297a514" />


## 다운로드

Windows 설치 파일은 아래 GitHub Releases에서 받을 수 있습니다.

[Excel Automation Workspace 다운로드](https://github.com/rlahfld54/excel-desktop-app/releases/tag/v1.0.1)

## 기술 스택

<p>
  <img src="https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react&logoColor=111111" alt="React" />
  <img src="https://img.shields.io/badge/Vite-6-646CFF?style=for-the-badge&logo=vite&logoColor=ffffff" alt="Vite" />
  <img src="https://img.shields.io/badge/Electron-37-47848F?style=for-the-badge&logo=electron&logoColor=ffffff" alt="Electron" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-4-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=ffffff" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/ExcelJS-4.4-217346?style=for-the-badge&logo=microsoftexcel&logoColor=ffffff" alt="ExcelJS" />
  <img src="https://img.shields.io/badge/SQLite-Local_DB-003B57?style=for-the-badge&logo=sqlite&logoColor=ffffff" alt="SQLite" />
</p>

## 프로젝트 한 줄 소개

Excel 파일 업로드부터 데이터 검증, 마감 진행 관리, 거래처 발송, 보고서 작성과 백업까지 하나의 흐름으로 연결한 로컬 우선 업무 자동화 앱입니다.

## 왜 만들었나요?

실무에서 매출 마감 업무를 진행할 때는 여러 담당자가 작성한 Excel 파일을 취합하고 검수해야 합니다.

하지만 사람마다 입력 방식이 달라 다음과 같은 문제가 반복됩니다.

- 거래처명과 품목명의 표기 불일치
- 필수 데이터 누락
- 중복 데이터 입력
- 수량·단가·금액 불일치
- 담당자 및 거래처 확인 상태 누락
- 보고 직전까지 이어지는 수정 파일 관리
- 업체별 마감장과 확인 요청 자료의 반복 생성

이 과정에서는 데이터를 분석하는 시간보다 오류가 발생한 위치와 확인 담당자를 찾는 데 더 많은 시간이 들기도 합니다.

그래서 사람이 모든 데이터를 반복해서 검사하는 대신, 시스템이 오류 후보와 확인 대상을 정리하고 사용자는 최종 판단에 집중할 수 있는 **마감 업무 전용 작업 공간**을 만들었습니다.

## 주요 기능

- Excel/XLSX 파일 업로드 및 표준 양식 검증
- 누락값, 중복, 금액 및 단가 불일치 탐지
- 제품·거래처 코드 매핑
- 원본 데이터 조회 및 SQLite 저장
- 업체별 마감 진행 상태 관리
- 거래처 및 내부 담당자 연락처 관리
- 업체별 마감 요청 Excel·PDF 생성
- 메일 제목과 요청 문구 미리보기
- Gmail 테스트 메일 발송
- 보고서 작성 및 템플릿 관리
- 경영진용 보고 대시보드
- 작업 이력과 활동 로그 관리
- 로컬 백업 및 복구
- 관리자와 일반 사용자 권한별 화면 분리

## 업무 흐름

1. Excel 파일 업로드
2. 업로드 전 데이터 검증
3. 제품·거래처 코드 매핑
4. 원본 데이터 저장
5. 업체별 마감 진행 관리
6. 마감장 Excel·PDF 생성
7. 확인 요청 및 발송 이력 저장
8. 보고서 작성 및 백업


## 상세 기술

### Frontend

- React 19
- React Router
- Tailwind CSS 4
- AG Grid
- Chart.js
- Radix UI
- Zustand

### Desktop & Data

- Electron
- Vite
- ExcelJS
- SheetJS
- better-sqlite3
- PDF-Lib
- Nodemailer
- electron-builder

## 개발 포인트

- 템플릿형 카드 대시보드를 실제 마감 업무 중심의 워크스페이스로 재설계
- Excel 업로드부터 검증, 저장, 보고, 발송까지 이어지는 업무 흐름 구성
- 비개발자 사무 사용자가 이해하기 쉬운 메뉴와 상태 표현 적용
- Electron IPC를 활용한 파일 저장, PDF 생성 및 이메일 발송 구현
- SQLite 기반 로컬 우선 구조로 오프라인 업무 환경 지원
- 사용자 권한에 따라 메뉴와 페이지 기능 분리
- 반복되는 업무 화면을 재사용 가능한 React 컴포넌트로 구성
- 작업 기록과 발송 이력을 로컬 데이터베이스에 저장

## 이 프로젝트를 통해 보여주고 싶은 점

이 프로젝트는 화려한 화면보다 사용자가 매일 겪는 불편을 줄이는 제품을 만드는 데 초점을 두고 있습니다.

- 실제 업무를 분석해 화면과 기능으로 바꾸는 능력
- 복잡한 작업을 단계적인 사용자 경험으로 정리하는 능력
- React와 Electron을 활용한 데스크톱 앱 개발
- Excel, SQLite, PDF, 이메일을 연결하는 실무형 기능 구현
- 사용자 관점에서 오류 상황과 작업 흐름을 계속 개선하는 태도

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



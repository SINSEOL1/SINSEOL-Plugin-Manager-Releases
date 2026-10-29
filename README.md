# SINSEOL Plugin Manager

Windows에서 로컬 Minecraft 서버의 플러그인 버전을 확인하고 JAR을 검증·백업·교체·복원합니다.

## 시작하기

Windows 10 1809 이상 / Windows 11 x64용입니다.

**[설치 EXE 다운로드](https://github.com/SINSEOL1/SINSEOL-Plugin-Manager-Releases/releases/latest/download/SINSEOL-Plugin-Manager-Setup.exe)**

`SINSEOL-Plugin-Manager-Setup.exe` 하나를 받아 실행하고 `설치`를 누르세요. Python 설치·ZIP 압축 해제 없이 바탕화면 또는 시작 메뉴에서 실행합니다. 관리자 권한은 필요하지 않습니다. 설치 EXE에는 필요한 파일이 모두 포함되어 있습니다.

1. `서버 폴더 추가`에서 `plugins`가 들어 있는 서버 최상위 폴더를 고릅니다.
2. 현재 서버 종류와 정확한 Minecraft 버전을 입력합니다.
3. 자동 배포처 탐색 후 `업데이트 확인`을 누릅니다.
4. `다운로드·교체 검토` 또는 `배포처에서 다운로드`로 진행합니다.

파일명이 달라도 JAR 내부 정보로 식별합니다. 설치 버전은 파일명에 적힌 숫자 대신 실제 JAR에서 읽습니다.

서버 연결을 해제하려면 `내 서버` 옆 `목록에서 제거`를 누르세요. 서버 폴더와 JAR·설정·월드·백업은 유지하며, 같은 폴더를 다시 추가하면 기존 배포처 연결을 재사용합니다.

프로그램 소개: https://sinseol.xyz/plugin-manager/

## 다운로드와 업데이트

- Modrinth·Hangar·Spigot·공개 GitHub Releases를 지원합니다. ProtocolLib·LoneLibs의 알려진 공식 외부 배포를 GitHub로 연결합니다.
- 유료·자동 다운로드 미지원 항목은 구매처에서 JAR을 받습니다. `다운로드 폴더 연결`을 켜면 이후 새로 받은 JAR을 감지하고 `감지한 파일 검토`에 보여줍니다. 기존에 있던 파일은 `내려받은 JAR 등록`으로 고를 수 있습니다.
- 폴더 감지와 파일 준비 단계에서는 서버 JAR을 변경하지 않습니다. 교체 검토에서 서버 정상 종료를 확인해야 적용됩니다.
- 프로그램 시작 시 새 정식 버전을 확인합니다. 새 버전은 왼쪽 버튼에서 다운로드·검증하고 재시작해 설치합니다. 서버 목록과 플러그인 백업은 유지됩니다.
- 베타·개발 릴리스는 기본 자동 업데이트 대상에서 제외합니다.

## 상태 읽기

초록: 교체 완료·파일/버전 일치 / 파랑: 새 버전 / 보라: 시험 버전 / 회색: 일반 안내 / 노랑: 조회 오류 / 빨강: 중복·의존성 등 교체 차단.

현재 파일의 내부 버전·해시가 완료 이력과 일치할 때 `업데이트 완료`가 표시됩니다. 파일명을 유지하므로 예전 버전 숫자가 파일명에 남을 수 있습니다. 이 표시는 서버 실행이나 모든 플러그인 간 호환성을 보증하지 않습니다.

## 백업·설정

- 프로그램: `%LOCALAPPDATA%\Programs\SINSEOL\PluginManager`
- 설정: `%LOCALAPPDATA%\SINSEOL\PluginManager`
- JAR 백업·교체 기록: `서버폴더/.sinseol-plugin-manager`
- 프로그램 자체 업데이트 작업·이전 프로그램: `프로그램폴더/.sinseol-app-updates`
- 백업은 JAR만 포함합니다. 설정·월드·외부 DB는 별도로 백업하세요.
- 프로그램 시작 오류는 설정 폴더의 `startup.log`, 프로그램 업데이트 실패는 작업 폴더의 `result.json`을 확인하세요.

JAR을 실행하거나 서버 경로·설정·월드·JAR 내용을 업로드하지 않습니다. 출처·버전 조회 시 파일 해시, 플러그인 이름, 프로젝트 ID, Minecraft 버전·로더를 해당 배포처에 전달합니다. 프로그램 릴리스 확인에는 공개 GitHub API를 사용합니다. 판매처 비밀번호나 GitHub 토큰은 요구하지 않습니다.

Windows 설정의 `설치된 앱`에서 제거할 수 있습니다. 제거 후에도 서버 목록·출처 연결·다운로드 폴더 설정·플러그인 백업은 유지합니다. 재설치하면 그대로 사용할 수 있습니다.

다운로드: https://github.com/SINSEOL1/SINSEOL-Plugin-Manager-Releases/releases/latest
문의·오류 신고: https://sinseol.xyz/contact/?project=plugin-manager&topic=bug

소스 저장소는 비공개로 관리합니다. 공개 배포에는 원본 앱 소스·개발 문서를 포함하지 않습니다. 라이선스와 타사 라이브러리 정보는 `THIRD_PARTY_NOTICES.md` 및 `licenses`를 참조하세요.

릴리스의 `windows-x64.zip`은 프로그램 자동 업데이트용입니다. 처음 설치할 때는 위의 설치 EXE만 받으면 됩니다.

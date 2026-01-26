# 설치 가이드

## 빠른 시작

1. **파일 다운로드**
   - `Gamma.exe` 파일 다운로드
   - 원하는 위치에 저장 (예: `C:\Program Files\Gamma Controller\` 또는 `D:\Tools\`)

2. **실행**
   - `Gamma.exe` 더블클릭
   - 설치 프로그램 불필요

3. **첫 실행**
   - 프로그램이 자동으로 `SETTING.JSON` 파일 생성
   - 기본 설정으로 시작

## 상세 설치 방법

### 방법 1: 포터블 설치 (권장)

1. 폴더 생성 (예: `C:\Gamma Controller\`)
2. `Gamma.exe` 파일을 해당 폴더에 복사
3. 바로가기 생성 (선택):
   - `Gamma.exe` 우클릭 → "바로가기 만들기"
   - 바로가기를 바탕화면 또는 시작 메뉴로 이동

### 방법 2: Program Files 설치

1. `C:\Program Files\Gamma Controller\` 폴더 생성
2. `Gamma.exe` 파일 복사
3. 관리자 권한으로 실행하여 자동 실행 설정 (선택)

## .NET Framework 확인

### Windows 10/11
- .NET Framework 4.7.2 이상이 기본 포함되어 있음
- 추가 설치 불필요

### Windows 7/8/8.1
1. .NET Framework 버전 확인:
   - 제어판 → 프로그램 → 프로그램 및 기능
   - ".NET Framework" 검색
   
2. 4.7.2 미설치 시:
   - [.NET Framework 4.7.2 다운로드](https://dotnet.microsoft.com/download/dotnet-framework/net472)
   - 다운로드 후 설치
   - 컴퓨터 재시작

## 자동 실행 설정

1. 프로그램 실행
2. **설정** 탭 이동
3. **"컴퓨터 시작 시 자동 실행"** 체크박스 선택
4. Windows 시작 시 자동으로 실행됨

## 관리자 권한 설정 (선택)

일부 시스템에서 감마 조정이 작동하지 않는 경우:

1. `Gamma.exe` 우클릭
2. **속성** 선택
3. **호환성** 탭
4. **"관리자 권한으로 이 프로그램 실행"** 체크
5. **확인** 클릭

## 제거 방법

1. 프로그램 종료 (시스템 트레이 아이콘 우클릭 → 종료)
2. `Gamma.exe` 파일 삭제
3. (선택) `SETTING.JSON` 파일 삭제 (설정 초기화)
4. (선택) 자동 실행 해제:
   - 설정 탭에서 "컴퓨터 시작 시 자동 실행" 체크 해제
   - 또는 레지스트리에서 수동 삭제:
     - `Win + R` → `regedit`
     - `HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run`
     - `Gamma_Controller` 항목 삭제

## 문제 해결

### "애플리케이션을 시작할 수 없습니다" 오류
- **원인**: .NET Framework 미설치
- **해결**: .NET Framework 4.7.2 설치

### "액세스가 거부되었습니다" 오류
- **원인**: 파일 권한 문제
- **해결**: 
  - 다른 위치에 복사 (예: 사용자 폴더)
  - 또는 관리자 권한으로 실행

### 바이러스 백신 경고
- **원인**: 신뢰할 수 없는 출처의 실행 파일
- **해결**: 
  - 바이러스 백신 예외 목록에 추가
  - 또는 신뢰할 수 있는 출처에서 다운로드 확인

## 다음 단계

설치가 완료되면 [README.md](README.md)를 참고하여 사용 방법을 확인하세요.


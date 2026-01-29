# RPAapp

C# .NET Framework 4.7.2 기반의 WPF 애플리케이션입니다.

## 프로젝트 개요

이 프로젝트는 RPA (Robotic Process Automation) 애플리케이션으로, 다음과 같은 기능을 제공합니다:

- Excel 데이터 처리 및 조회
- 홈택스 관련 기능
- 데이터베이스 연결 (MongoDB)
- MVVM 패턴 기반의 구조화된 코드

## 필수 요구사항

- Visual Studio 2017 이상
- .NET Framework 4.7.2
- Windows 운영체제

## 프로젝트 구조

```
RPAapp/
├── Model/          # 데이터 모델 클래스
├── View/           # XAML 뷰 파일들
├── ViewModel/      # 뷰모델 클래스들 (MVVM 패턴)
├── Tools/          # 유틸리티 클래스들
└── Properties/     # 애플리케이션 속성 및 리소스
```

## 빌드 방법

### Visual Studio 사용

1. `RPAapp.sln` 파일을 Visual Studio에서 엽니다.
2. NuGet 패키지 복원:
   - 솔루션 탐색기에서 솔루션을 우클릭하고 "Restore NuGet Packages" 선택
   - 또는 빌드 시 자동으로 복원됩니다.
3. 빌드:
   - `Ctrl + Shift + B` 또는 메뉴에서 `Build > Build Solution`

### 명령줄 사용

```powershell
# NuGet 패키지 복원
nuget restore RPAapp.sln

# MSBuild로 빌드
msbuild RPAapp.sln /p:Configuration=Debug /p:Platform="Any CPU"
```

## 주요 NuGet 패키지

- **ClosedXML** (0.95.4) - Excel 파일 처리
- **MongoDB.Driver** (3.4.2) - MongoDB 데이터베이스 연결
- **Newtonsoft.Json** (13.0.3) - JSON 처리
- **DocumentFormat.OpenXml** (2.12.3) - OpenXML 문서 처리

전체 패키지 목록은 `RPAapp/packages.config` 파일을 참조하세요.

## 실행 방법

### Visual Studio에서 실행

1. `RPAapp.sln` 파일을 Visual Studio에서 엽니다.
2. `F5` 키를 누르거나 메뉴에서 `Debug > Start Debugging` 선택
3. 또는 `Ctrl + F5`로 디버깅 없이 실행

### 명령줄에서 실행

```powershell
# PowerShell 사용
.\run-wpf.ps1

# 또는 배치 파일 사용
run-wpf.bat

# 또는 직접 실행 파일 실행
.\RPAapp\bin\Debug\RPAapp.exe
```

### XAML 디자이너에서 미리보기

Visual Studio에서 XAML 파일을 열면 디자이너 뷰에서 UI를 미리 볼 수 있습니다:
- `MainWindow.xaml` - 메인 윈도우
- `View/*.xaml` - 각 뷰 파일들

## 개발 환경 설정

1. 이 저장소를 클론합니다.
2. Visual Studio에서 솔루션을 엽니다.
3. NuGet 패키지가 자동으로 복원됩니다.
4. 프로젝트를 빌드하고 실행합니다.

## 코드 스타일

이 프로젝트는 `.editorconfig` 파일을 사용하여 코드 스타일을 일관되게 유지합니다. Visual Studio는 이 파일을 자동으로 인식하여 코드 포맷팅을 적용합니다.

## 테스트

이 프로젝트는 MSTest를 사용한 단위 테스트를 포함하고 있습니다.

### Visual Studio에서 테스트 실행

1. **Test Explorer 사용**:
   - `Test > Test Explorer` 메뉴를 엽니다
   - `Ctrl + R, A`로 모든 테스트 실행
   - 또는 `Ctrl + R, T`로 현재 컨텍스트의 테스트 실행

2. **명령줄에서 테스트 실행**:
   ```powershell
   # PowerShell 사용
   .\run-tests.ps1
   
   # 또는 배치 파일 사용
   run-tests.bat
   ```

### 테스트 프로젝트 구조

```
RPAapp.Tests/
├── Model/              # 모델 클래스 테스트
├── ViewModel/          # ViewModel 클래스 테스트
└── Tools/              # 유틸리티 클래스 테스트
```

### 테스트 작성 가이드

- 각 프로덕션 클래스에 대해 해당하는 테스트 클래스를 작성합니다
- 테스트 메서드는 `[TestMethod]` 특성으로 표시합니다
- 테스트 클래스는 `[TestClass]` 특성으로 표시합니다

## 라이선스

이 프로젝트의 라이선스 정보는 각 NuGet 패키지의 라이선스를 참조하세요.


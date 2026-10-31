# Hyfeast

**Hyfeast**는 한국건설기술연구원(KICT)에서 개발한 고성능 유한요소해석(FEA) 프레임워크입니다.  구조 해석 및 설계 응용을 위해 누구나 자유롭게 사용할 수 있습니다.

Hyfeast는 셸, 보, 솔리드 요소를 지원하며, 빠른 병렬 해석, 3D 시각화, 배치 모드 해석 기능을 제공합니다. 구조역학 및 설계 자동화를 연구하는 연구자, 엔지니어, 개발자를 위해 설계되었습니다.

- 다운로드: [최신 릴리스](https://github.com/jrcho/Hyfeast/releases/latest)  
- 도움말: [온라인 문서](https://jrcho.github.io/Hyfeast/index.html)  
- 오프라인 도움말: `Bin\help\index.html`  
- English version: [README.md](./README.md)

## 시스템 요구사항

- 64비트 Windows 10 이상

## 설치 및 사용법

Hyfeast는 압축을 풀면 바로 쓸 수 있습니다. `install.bat`을 한 번 실행하면 시작 메뉴와 명령이 등록되어 더 편하게 쓸 수 있습니다.

### 1. 압축 해제

1. [Releases](https://github.com/jrcho/Hyfeast/releases/latest) 페이지에서 최신 릴리스를 다운로드합니다.
2. ZIP 파일을 원하는 위치(예: `D:\Apps\Hyfeast-v1.0.0`)에 압축 해제합니다. 아래에서는 이 폴더를 **배포 폴더**라고 부릅니다.

### 2. 설치 (권장)

배포 폴더의 `install.bat`을 더블 클릭합니다. 관리자 권한은 필요 없고, 파일을 다른 곳으로 복사하지도 않습니다.

- 시작 메뉴에 배포 폴더 이름(예: `Hyfeast-v1.0.0`)으로 폴더가 생기고 hfStudio, hf2DStudio, Hyfeast Command Prompt, Hyfeast Help, Examples, Uninstall이 등록됩니다.
- 바탕화면 바로가기는 설치 중에 만들지 묻습니다.
- `hfAnalyzer`, `hfSectAnalyzer`, `hfStudio`, `hf2DStudio` 명령이 등록되어, 설치 후 **새로 연** 명령 프롬프트나 PowerShell 창이면 어느 폴더에서나 바로 실행됩니다.

```
D:\Work\proj> hfAnalyzer frame.inp
D:\Work\proj> hfStudio
```

배포 폴더를 다른 곳으로 옮기면 바로가기가 끊어지므로 옮긴 위치에서 `install.bat`을 다시 실행합니다.

### 3. 설치하지 않고 쓰기

배포 폴더의 `HyfeastCmd.bat`을 더블 클릭하면 Hyfeast 실행 환경이 설정된 명령 프롬프트가 열립니다. 이미 열어 둔 명령 프롬프트에서 환경만 설정하려면 다음과 같이 입력합니다.

```
D:\Work\proj> D:\Apps\Hyfeast-v1.0.0\HyfeastCmd.bat --no-shell
D:\Work\proj> hfAnalyzer frame.inp
```

### 4. 여러 버전을 함께 쓸 때

- 버전마다 `install.bat`을 실행하면 시작 메뉴에는 버전별 폴더가 따로 생깁니다.
- `hfAnalyzer` 같은 명령은 **마지막에 설치한 버전**을 실행합니다.
- 어떤 창에서만 다른 버전을 쓰려면 그 버전의 `HyfeastCmd.bat --no-shell`을 실행합니다. 그 창에서는 그 버전이 먼저 실행됩니다.
- 어느 프로그램이 실행되는지는 `where hfAnalyzer`로 확인합니다.

### 5. 제거

시작 메뉴의 **Uninstall** 또는 배포 폴더의 `uninstall.bat`을 실행하면 바로가기와 명령이 제거되고, hfStudio·hf2DStudio 설정(`Bin`의 `*.ini`)이 초기화되며, 배포 폴더와 `Bin`에 생긴 작업 폴더 `.hyfeast`(자동 저장 백업 등)도 지워집니다. 명령은 이 버전을 가리키고 있을 때만 제거됩니다. DigitalTwin 활성화는 모든 버전이 함께 쓰므로 유지됩니다. 설정을 초기화하려면 실행 전에 hfStudio와 hf2DStudio를 닫습니다. 그다음 배포 폴더를 지우면 됩니다.

자세한 사용법은 도움말이나 예제 파일을 참고하세요.

## Hyfeast에 사용된 외부 라이브러리

Hyfeast는 다음과 같은 오픈소스 및 서드파티 라이브러리를 포함하고 있습니다:

### 수치 커널 및 해석기

- Intel OneAPI MKL – BLAS, LAPACK, 벡터 연산  
- PARDISO – 직접 해법을 위한 희소 행렬 해석기 (MKL 포함)  
- ARPACK – 희소 행렬의 고유값 해석기  
- Eigen – C++ 선형대수 라이브러리  
- HDF5 – 과학 데이터 저장용 포맷

### GUI 및 시각화

- Qt – 그래픽 사용자 인터페이스 프레임워크  
- VTK – 3D 시각화 엔진  
- NETGEN – 2차원 메시 생성기

### 유틸리티

- xlnt – C++용 Excel `.xlsx` 입출력 라이브러리  
- RapidJSON – C++용 고속 JSON 파서  
- JKQtPlotter – Qt 기반 과학 플로팅 위젯

### 외부 도구 (선택 사항)

- Python - Digital Twin/OMA 분석 스크립트 실행에 사용
- Pandoc – 문서 변환기

자세한 라이선스 및 출처 정보는 `LICENSE.txt`를 참고하세요.

## 라이선스

본 소프트웨어는 커스텀 라이선스로 제공됩니다.  
전체 조건은 `LICENSE.txt` 파일을 참고하십시오.

## 문의처

기술 문의 및 지원: jrcho2012@gmail.com

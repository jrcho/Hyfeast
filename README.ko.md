# Hyfeast

**Hyfeast**는 한국건설기술연구원(KICT)에서 개발한 고성능 유한요소해석(FEA) 프레임워크입니다.  
구조 해석 및 설계 응용을 위해 누구나 자유롭게 사용할 수 있습니다.

- 다운로드: [최신 릴리스](https://github.com/jrcho/Hyfeast/releases/latest)  
- 도움말: [온라인 문서](https://jrcho.github.io/Hyfeast/index.html)  
- English version: [README.md](./README.md)

## 시스템 요구사항

- Windows 10 이상
- 64비트 시스템
- (선택 사항) Python 3.8 이상 (DXF 내보내기 기능에 필요)

## 설치 및 사용법

1. [Releases](https://github.com/jrcho/Hyfeast/releases/latest) 페이지에서 최신 릴리스를 다운로드합니다.
2. ZIP 파일을 원하는 위치(예: `Hyfeast/`)에 압축 해제합니다.
3. `Hyfeast` 폴더를 열고 `setpath.bat`을 더블 클릭하면 환경 변수가 설정되고 명령 프롬프트가 열립니다.
4. 명령 프롬프트에서 다음과 같이 실행할 수 있습니다:

```
Hyfeast> hfVisualizer
Hyfeast> hfAnalyzer input.inp
Hyfeast> hfSectionVisualizer
Hyfeast> hfSectionAnalyzer input.sec
```

자세한 사용법은 매뉴얼이나 예제 파일을 참고하세요.

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

- Python – ezdxf 및 모드 해석 스크립트 실행에 사용
- ezdxf (Python) – `hfVisualizer`의 DXF 내보내기 기능에 사용됨
- Pandoc – 문서 변환기

자세한 라이선스 및 출처 정보는 `LICENSE.txt`를 참고하세요.

## 라이선스

본 소프트웨어는 커스텀 라이선스로 제공됩니다.  
전체 조건은 `LICENSE.txt` 파일을 참고하십시오.

## 문의처

기술 문의 및 지원: jrcho2012@gmail.com

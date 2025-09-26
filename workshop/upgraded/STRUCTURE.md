# upgraded 폴더 구조 설명

`upgraded` 폴더는 레거시 Python 프로젝트의 전체 구조를 최신화 및 포팅 작업을 위해 복사한 디렉터리입니다. 아래는 주요 폴더 및 파일 구조와 각 역할에 대한 설명입니다.

```
upgraded/
├── MANIFEST.in                # 패키징을 위한 매니페스트 파일
├── README.rst                 # 프로젝트 설명 파일
├── distribute-0.6.10.tar.gz   # 레거시 의존성 패키지(압축 파일)
├── distribute_setup.py        # distribute 설치 스크립트
├── setup.py                   # 패키지 설치/설정 스크립트
├── docs/                      # Sphinx 기반 문서 폴더
│   ├── Makefile               # 문서 빌드용 Makefile
│   ├── build/                 # Sphinx 빌드 산출물
│   │   ├── doctrees/          # Sphinx 중간 파일
│   │   └── html/              # HTML 문서 결과물
│   │       ├── _sources/      # 원본 rst 텍스트
│   │       └── _static/       # 정적 리소스(css, js, 이미지 등)
│   └── source/                # 문서 원본(rst, conf.py 등)
│       └── _static/           # 커스텀 스타일 등
├── guachi/                    # 실제 Python 패키지 소스
│   ├── __init__.py
│   ├── config.py
│   ├── database.py
│   └── tests/                 # 단위 테스트 코드
│       ├── test_configmapper.py
│       ├── test_configurations.py
│       ├── test_database.py
│       └── test_integration.py
└── guachi.egg-info/           # 패키지 메타데이터
    ├── PKG-INFO
    ├── SOURCES.txt
    ├── dependency_links.txt
    └── top_level.txt
```

## 주요 폴더/파일 설명
- **MANIFEST.in, setup.py**: 패키징 및 설치 관련 메타 파일
- **README.rst**: 프로젝트 설명서
- **distribute-0.6.10.tar.gz, distribute_setup.py**: 레거시 Python 패키지 관리 도구
- **docs/**: Sphinx 기반 문서 소스 및 빌드 결과
- **guachi/**: 실제 소스 코드와 테스트 코드
- **guachi.egg-info/**: 패키지화 시 생성되는 메타데이터

이 구조는 레거시 프로젝트를 최신 Python 환경으로 포팅하거나, 테스트 및 문서화 작업을 진행할 때 그대로 활용할 수 있습니다.

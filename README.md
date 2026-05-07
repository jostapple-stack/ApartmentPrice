# ApartmentPrice
공공데이터 API를 활용한 아파트 매매가격 조회

# ApartmentPrice

공공데이터 API와 Gemini AI를 활용한 아파트 실거래가 자동 보고서 생성 프로그램입니다.

---

## 프로젝트 소개

RPA 없이 Python만으로 아파트 실거래가 데이터를 수집하고, AI 분석 코멘트가 포함된 Excel 보고서를 자동으로 생성합니다.
기업에서 고비용 RPA 라이센스 없이도 동일한 자동화 프로세스를 구축할 수 있음을 보여주는 포트폴리오 프로젝트입니다.

---

## 주요 기능

- 국토교통부 공공데이터 API를 활용한 아파트 실거래가 데이터 수집
- 서울 4개 구(영등포구, 관악구, 구로구, 강서구) 조회 지원 / 추가 가능
- 조회 년월 유효성 검사 (미래 날짜 및 10년 초과 날짜 차단)
- 구별 시트로 구성된 Excel 보고서 자동 생성
- 중복 데이터 감지 및 기존 파일 자동 열기 기능
- Gemini AI를 활용한 시세 흐름 분석 코멘트 자동 생성

---

## 사용 기술

| 항목 | 내용 |
|------|------|
| Language | Python 3.x |
| 데이터 수집 | 국토교통부 공공데이터 API |
| AI 분석 | Google Gemini API |
| 보고서 생성 | openpyxl |
| 데이터 처리 | pandas |
| 환경 변수 관리 | python-dotenv |

---

## 프로젝트 구조
ApartmentPrice/
├── main.py            # 메인 실행 파일
├── .env               # API 키 저장 (Git 제외)
├── .env.example       # API 키 템플릿
├── .gitignore         # Git 제외 파일 설정
├── requirements.txt   # 라이브러리 목록
└── output/            # 생성된 Excel 보고서 저장 폴더

---

## 실행 방법

**1. 레포지토리 클론**
```bash
git clone https://github.com/jostapple-stack/ApartmentPrice.git
```

**2. 라이브러리 설치**
```bash
pip install -r requirements.txt
```

**3. 환경 변수 설정**

`.env.example` 파일을 복사해서 `.env` 파일을 만들고 API 키를 입력해주세요.

---

## 🚀 실행 방법

**1. 레포지토리 클론**
```bash
git clone https://github.com/jostapple-stack/ApartmentPrice.git
```

**2. 라이브러리 설치**
```bash
pip install -r requirements.txt
```

**3. 환경 변수 설정**

`.env.example` 파일을 복사해서 `.env` 파일을 만들고 API 키를 입력해주세요.

PUBLIC_DATA_API_KEY=공공데이터_Decoding_키
GEMINI_API_KEY=Gemini_API_키

**4. 실행**
```bash
python main.py
```

---

## 🏢 전사 배포 방안

| 방법 | 설명 | 특징 |
|------|------|------|
| 실행 파일(.exe) | PyInstaller로 변환 후 배포 | Python 설치 없이 실행 가능 |
| 웹 서버 호스팅 | 클라우드 서버에 배포 | 브라우저로 접근 가능 |
| 스케줄러 자동 실행 | 서버에 등록 후 자동 실행 | RPA 대체에 가장 적합 |

---

## 📊 실행 예시

=== 조회할 지역을 선택하세요 ===

영등포구
관악구
구로구
강서구
전체

번호를 입력하세요: 1
조회할 년월을 입력하세요 (예: 202403): 202403
영등포구 데이터 추가 완료!
영등포구 AI 분석 중...
Excel 파일 저장 완료: output/202403.xlsx

---

## 📝 라이센스

MIT License
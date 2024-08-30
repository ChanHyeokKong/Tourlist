# 투어리스트 (TourList)

## 1. 프로젝트 목표

### 주요 목표

- **AI를 통한 맞춤형 여행지 추천**: 사용자의 요구와 선호에 기반하여 최적의 여행지를 추천
- **리뷰 기반의 정확한 정보 제공**: Google Maps에서 제공하는 실제 사용자 리뷰를 활용하여, RAG 모델을 통해 여행지에 대한 정확하고 신뢰할 수 있는 정보를 제공

### 세부 목표

- **Google Maps의 리뷰 데이터 활용**: 다양한 관광지에 대한 사용자 리뷰를 수집하여, 사용자가 더 신뢰할 수 있는 여행지 추천을 받을 수 있도록 함
- **RAG 모델 통합**: 검색 기반의 문서 검색과 생성 모델을 결합하여, 사용자 맞춤형 여행 계획을 지원

## 2. 개발 과정

### 1. 시스템 설계 및 구성

- **LangChain을 통한 RAG 모델 사용**: LangChain을 이용하여 Retrieval-Augmented Generation (RAG) 모델을 구성하고, 문서 검색과 응답 생성의 두 가지 주요 단계를 통합
- **OpenAI API를 통한 GPT-3.5 LLM 모델 사용**: OpenAI의 GPT-3.5를 사용하여 자연어 생성 기능을 구현하고, 사용자 질의에 대한 적절한 응답을 생성

### 2. 데이터 수집 및 처리

- **사용자 입력**: 사용자가 원하는 도시와 여행 요구사항을 입력
- **데이터 수집**: Google Maps API를 활용하여 입력된 도시 주변의 관광지와 관련된 리뷰 데이터를 수집
- **문서화**: 수집된 리뷰 데이터를 문서 형식으로 변환하고, 이를 RAG 모델의 검색 가능한 데이터베이스에 저장

### 3. 검색 및 생성

- **데이터 검색**: 사용자 요구에 맞는 데이터를 검색하여 관련 정보를 추출
- **RAG와 LLM을 통한 응답 생성**: 검색된 정보를 기반으로 RAG와 LLM을 사용하여 사용자 요구에 적합한 여행지 추천 결과를 생성

## 3. 개선 사항

### 1. 기능 확장

- **다양한 장소 추가**: 현재 시스템은 관광지에 한정된 리뷰만을 다루고 있으므로, 향후 식당, 호텔 등 다양한 장소의 리뷰를 수집하고 관련 추천 기능을 추가

### 2. 사용자 인터페이스 개선

- **웹 기반의 사용자 인터페이스 개발**: 현재는 명령어 기반의 접근 방식이므로, 사용자 친화적인 웹 기반 인터페이스를 개발

### 3. 데이터 정확성 및 다양성

- **리뷰 데이터의 품질 개선**: 더 많은 사용자 리뷰와 최신 정보를 반영하여 추천의 정확성과 신뢰성을 상승

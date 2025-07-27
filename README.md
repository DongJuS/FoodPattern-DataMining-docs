# FoodPattern-DataMining-docs
AI meal recommendation system using association rule mining and deep learning on Gyeonggi high school meal data | 경기도 고등학교 급식 데이터 기반 연관규칙 마이닝 식단 추천 시스템

# FoodPattern-DataMining

AI meal recommendation system using association rule mining and deep learning on Gyeonggi high school meal data | 경기도 고등학교 급식 데이터 기반 연관규칙 마이닝 식단 추천 시스템

## 프로젝트 소개
경기도 고등학교 5년치 급식 데이터를 활용하여 연관규칙 마이닝과 딥러닝 기술을 통해 월별 식단 생성 및 특정 음식에 어울리는 음식을 추천하는 AI 시스템입니다. 222,375개의 트랜잭션과 3,000여 개의 음식 데이터를 분석하여 실용적인 식단 추천 서비스를 제공합니다.

## 주요 기능
- 월별 식단 자동 생성: 계절성과 식단 패턴을 고려한 월별 맞춤 식단 추천
- 음식 조합 추천: 특정 음식과 잘 어울리는 음식 조합 제안
- 다단계 FP-Growth 알고리즘: 대용량 데이터 처리를 위한 최적화된 연관규칙 분석
- 카테고리 기반 분석: 주식, 국류, 반찬, 김치류 등 음식 카테고리별 체계적 분석

## 사용 기술
- Python: 주요 개발 언어 및 데이터 처리
- R, RStudio: 통계 분석 및 데이터 시각화
- Deep Learning: 음식 분류 및 패턴 학습
- Data Mining:
  - Clustering (계층적 군집화)
  - Association Rules (Apriori, FP-Growth)
  - Multi-level FP-Growth (성능 최적화)


## 시스템 아키텍처
데이터 전처리

원시 데이터 수집: 경기도 고등학교 5년치 급식식단정보 데이터
데이터 정제:

<br/> 태그 기준 음식명 분리
알레르기 정보 및 특수문자 제거
동일 음식의 다양한 표기 통합


카테고리 분류: 음식을 7가지 대분류로 체계화

## 핵심 알고리즘
데이터 전처리 → 카테고리별 분석 → 카테고리 간 연관규칙 분석 → 통합 식단 생성 → 결과 저장
성능 최적화: 다단계 FP-Growth

문제: 단일 FP-Growth에서 메모리 폭발 및 조합 폭발 (9,000,000회 계산 필요)
해결: 카테고리별 소형 FP-Tree 구성으로 분할 정복
결과: 단일 FP-Growth 대비 1000배 이상 성능 향상

## 주요 성과
품질 개선

기존: "김치와 사과", "밥과 우유" 등 무작위적 조합
개선: "현미밥 → 된장국 → 제육볶음 → 콩나물무침 → 배추김치" 등 자연스러운 식단 구성
결과: 생성된 연관규칙의 95% 이상이 실제 활용 가능한 의미있는 조합

## 결과
<img width="407" height="269" alt="식단 결과 스크린샷" src="https://github.com/user-attachments/assets/416acc8e-628b-4580-9a9e-388d7aa10bfd" />

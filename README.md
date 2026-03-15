# 📱 Kor-Smishing Dataset & Benchmark
> **스미싱(Smishing) 탐지 AI 모델 학습을 위한 한국어 데이터셋 및 성능 평가 지표**

[![Hugging Face Dataset](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Datasets-yellow)](https://huggingface.co/datasets/jmjmjm3/kor-smishing-message)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

---

## 1. 🚨 프로젝트 배경 및 위험성
**스미싱(Smishing)**은 SMS와 피싱(Phishing)의 합성어로, 문자 메시지를 통해 악성 링크 클릭이나 개인정보 입력을 유도하는 지능형 사이버 범죄입니다.

* **정교한 사칭:** 택배 배송, 공공기관, 금융 인증 절차 등을 완벽히 모방합니다.
* **지능적 진화:** 일상적인 문구를 교묘하게 활용하여 단순 필터링을 우회합니다.
* **사회적 문제:** 개인정보 유출을 넘어 심각한 금전적 피해와 2차 범죄로 이어집니다.

---

## 2. 🧠 AI 기반 탐지의 필요성
기존의 **규칙 기반(Rule-based)** 방식은 변칙적인 문구와 신종 패턴 대응에 한계가 있습니다.

| 구분 | 기존 규칙 기반 방식 | AI 기반 NLP 모델 |
| :--- | :--- | :--- |
| **대응 방식** | 특정 키워드 매칭 | 문맥 및 의도 파악 |
| **유연성** | 문구 변형에 취약함 | 신종 패턴에 유연하게 대응 |
| **정확도** | 오탐(False Positive) 발생 높음 | 정밀한 탐지 가능 |

---

## 3. 📊 데이터셋 구축 개요 (Dataset)
본 프로젝트는 한국어 환경에 최적화된 스미싱 탐지 AI 학습을 위해 고품질 데이터셋을 구축하였습니다.

### 📌 데이터셋 주요 특징
* **분류:** 스미싱 문자(Smishing) / 정상 문자(Ham) 이진 분류
* **도메인:** 금융, 택배, 공공기관, 지인 사칭 등 실제 사례 중심 구성
* **활용도:** 모델 학습 및 공정한 성능 비교를 위한 벤치마크 데이터로 활용 가능

<p align="center">
  <img src="https://github.com/user-attachments/assets/407e4e51-0bc5-45be-aeb8-96caa646ffc9" width="400" />
</p>

> **Hugging Face 주소:** [jmjmjm3/kor-smishing-message](https://huggingface.co/datasets/jmjmjm3/kor-smishing-message)

---

## 4. 📈 벤치마크 및 모델 평가 (Benchmark)
다양한 AI 모델을 활용해 스미싱 탐지 성능을 실험하고 분석하였습니다.

### 📉 실험 결과 요약
본 벤치마크 결과는 향후 스미싱 대응 시스템 개발 시 최적의 모델을 선택하는 기초 자료로 활용될 수 있습니다.

<p align="center">
  <img src="https://github.com/user-attachments/assets/83fe273c-4a6e-4bb2-828a-1538071698bf" width="80%" />
  <br>
  <img src="https://github.com/user-attachments/assets/518bdb2e-6822-4165-a91c-0de8547c33ee" width="80%" />
</p>

---

## 5. ✨ 기대 효과
* **표준화:** 스미싱 탐지 연구를 위한 한국어 표준 데이터셋 제공
* **객관성:** 모델 간 성능 비교를 위한 명확한 벤치마크 기준 제시
* **실용성:** 실제 서비스 적용이 가능한 수준의 정교한 데이터 구성

---

## 🛠️ Quick Start
데이터셋을 프로젝트에 바로 적용해 보세요.

```python
from datasets import load_dataset

# 데이터셋 불러오기
dataset = load_dataset("jmjmjm3/kor-smishing-message")

# 예시 데이터 출력
print(dataset['train'][0])

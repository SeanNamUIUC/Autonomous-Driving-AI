# 🛰️ Autonomous-Driving-AI
> **Sequential Attention 기반 자율주행 차폐(Occlusion) 극복 BEV 경로 예측 시스템**

본 프로젝트는 주행 중 가로수, 대형 차량 등에 의해 주변 객체가 가려지는 **차폐(Occlusion) 시나리오**를 극복하기 위해, **Transformer의 Multi-Head Attention 메커니즘을 밑바닥부터 백지 구현**하고 이를 KITTI 데이터셋의 시계열 워크로드에 도킹하는 자율주행 인지 프로젝트입니다.

---

## 🏗️ Repository Architecture
- **`attention_mechanism/1_model/`**: PyTorch 로우 레벨 연산자 기반 딥러닝 코어 아키텍처 (MHA, Transformer Block) 구현 구역
- **`2_data_pipeline/`**: KITTI Tracking Dataset 시계열 좌표 파싱 및 BEV(Bird's-Eye View) 궤적 복원 구역
- **`attention_mechanism/3_hardware_profile/`**: 모델 구동 시 발생하는 연산 비용(VRAM, Latency) 분석 및 하드웨어 친화적 최적화 검증 구역

---

## 📊 Hardware Target
- **구동 환경**: Google Colab GPU 인프라 기반 테스트 및 최적화 진행 예정
- **목표**: 모델 코드 구현 완료 후, 실제 연산량(FLOPs), 메모리 점유율(Peak VRAM), 추론 속도(Latency)를 정밀 측정하여 하드웨어 자원 효율성을 증명할 계획입니다.
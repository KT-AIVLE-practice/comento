
# 📦 Image Preprocessing Pipeline

이 프로젝트는 HuggingFace `food101` 데이터셋에서 샘플 이미지를 가져와, 딥러닝 학습을 위한 전처리를 수행하는 예제입니다.

## ✅ 전처리 단계

1. **크기 조정 (Resize)**  
   - 모든 이미지를 224x224 픽셀로 조정

2. **그레이스케일 변환 및 정규화 (Grayscale & Normalize)**  
   - RGB → Grayscale 변환 후, [0,1]로 정규화

3. **노이즈 제거 (Blur)**  
   - 가우시안 블러 적용

4. **데이터 증강 (Augmentation)**  
   - 좌우 반전 적용

5. **이상치 제거 (Outlier Filtering)**  
   - 밝기 평균이 너무 어두운 이미지 제거  
   - 주요 객체(윤곽선 면적)가 너무 작은 이미지 제거

## ✅ 저장 경로
- 전처리된 샘플은 `preprocessed_samples/` 폴더에 저장됩니다.

## ✅ 사용한 데이터셋
- HuggingFace: [`food101`](https://huggingface.co/datasets/food101)

## ✅ 전처리 예시 결과
- torch_0.jpg ✅
- torch_1.jpg ❌ (객체 작음)
- torch_2.jpg ❌ (객체 작음)
- torch_3.jpg ❌ (객체 작음)
- torch_4.jpg ✅

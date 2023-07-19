# Image_Processing_for_Cervix

자궁경부 데이터에 대하여 여러 영상처리 알고리즘을 적용 후, 딥러닝 분류 모델의 정확도를 비교하였습니다.
영상처리 알고리즘 리스트는 다음과 같습니다.

1. CLAHE
2. Histogram Equalization
3. Sharpening

또한, 알고리즘을 처리한 영상에 대하여 영상의 품질을 비교하여 아래의 두 가지 점수를 계산하였습니다.

1. PSNR(Peak Signal-to-Noise Ratio)
    - 생성 혹은 압축된 영상의 화질에 대한 손실 정보를 평가
    - 손실이 적을 수록 (품질이 좋을수록) 높은 점수를 보임

2. SSIM(Structural Similarity Index Map)
    - 휘도, 대조, 구조를 기준으로 영상의 화질을 평가
    - 품질이 좋을수록 높은 점수를 보임

3. Brisque(Blind/Referenceless Image Spatial Quality Evaluator)
    - 영상 A의 무참조(No-Reference) 영상 품질 점수를 계산
    - brisque는 A를 유사 왜곡이 있는 자연 장면 영상에서 계산된 디폴트 모델과 비교
    - 품질이 좋을수록 높은 점수를 보임
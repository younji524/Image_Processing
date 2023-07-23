# Image_Processing_for_Cervix

자궁경부 데이터에 대하여 여러 영상처리 알고리즘을 적용 후, 딥러닝 분류 모델의 정확도를 비교하였습니다.
영상처리 알고리즘 리스트는 다음과 같습니다.
<br/>
1. Histogram Equalization <br/>
    - 좁은 범위에 집중되어 있는 픽셀 값들을 0 ~ 255 범위에 골고루 분포하도록 변화하는 영상처리 기법
<br/><br/>
2. CLAHE(Contrast Limited Adaptive Histogram Eqaulization) <br/>
    - 영상을 일정한 크기의 작은 블록으로 구분하고, 블록 별로 히스토그램 균일화를 시행함
<br/><br/>
3. Sharpening <br/>
    - 주변 픽셀과의 차이를 극대화시켜 명암 비를 증가시킴으로써 이미지의 구조적 정보 및 경계를 강조시켜 선명한 이미지를 얻는 영상처리 기법
<br/><br/>

또한, 알고리즘을 처리한 영상에 대하여 영상의 품질을 비교하여 아래의 두 가지 점수를 계산하였습니다. <br/>
<br/>
1. PSNR(Peak Signal-to-Noise Ratio)
    - 생성 혹은 압축된 영상의 화질에 대한 손실 정보를 평가 <br/>
    - 손실이 적을 수록 (품질이 좋을수록) 높은 점수를 보임 <br/>
<br/>
3. SSIM(Structural Similarity Index Map)
    - 휘도, 대조, 구조를 기준으로 영상의 화질을 평가 <br/>
    - 품질이 좋을수록 높은 점수를 보임 <br/>
<br/>
4. Brisque(Blind/Referenceless Image Spatial Quality Evaluator)
    - 영상 A의 무참조(No-Reference) 영상 품질 점수를 계산 <br/>
    - brisque는 A를 유사 왜곡이 있는 자연 장면 영상에서 계산된 디폴트 모델과 비교 <br/>
    - 품질이 좋을수록 높은 점수를 보임 <br/>
<br/>

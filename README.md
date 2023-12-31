# Image_Processing_for_Cervix

자궁경부 데이터에 대하여 여러 영상처리 기법을 적용 후, 딥러닝 분류 모델의 정확도를 비교하였습니다.
사용한 영상처리 기법은 다음과 같습니다.
<br/>
1. Histogram Equalization <br/><br/>
    - 좁은 범위에 집중되어 있는 픽셀 값들을 0 ~ 255 범위에 골고루 분포하도록 변화하는 영상처리 기법
<br/><br/>
2. CLAHE(Contrast Limited Adaptive Histogram Eqaulization) <br/><br/>
    - 영상을 일정한 크기의 작은 블록으로 구분하고, 블록 별로 히스토그램 균일화를 시행함
<br/><br/>
3. Sharpening <br/><br/>
    - 주변 픽셀과의 차이를 극대화시켜 명암 비를 증가시킴으로써 이미지의 구조적 정보 및 경계를 강조시켜 선명한 이미지를 얻는 영상처리 기법
<br/><br/>

**[원본 영상과 영상처리 알고리즘 적용 결과]** <br/>
(왼쪽부터 차례로 원본, sharpening, Histogram Equalization, CLAHE가 적용되었다.) <br/><br/>
![그림1](https://github.com/younji524/Image_Processing/assets/76142194/b72537f0-bfb9-4ad5-a8ce-54aa7736995e)

<br/><br/>
또한, 각 영상처리 기법을 적용한 영상에 대하여 영상의 품질을 비교하여 아래의 두 가지 점수를 계산하였습니다. <br/><br/>

1. PSNR(Peak Signal-to-Noise Ratio) <br/><br/>
    - 생성 혹은 압축된 영상의 화질에 대한 손실 정보를 평가 <br/>
    - 손실이 적을 수록 (품질이 좋을수록) 높은 점수를 보임 <br/>
<br/>

2. SSIM(Structural Similarity Index Map) <br/><br/>
    - 휘도, 대조, 구조를 기준으로 영상의 화질을 평가 <br/>
    - 품질이 좋을수록 높은 점수를 보임 <br/>
<br/>

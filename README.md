# 객체 탐지 딥러닝 모델을 활용한 영상 속 개인정보 보호 프로그램
<p align="center">
<img src="https://user-images.githubusercontent.com/86579242/218716573-39a4ba7d-37ec-4cac-9c88-346514da9ce6.gif" width="500" />
<img src="https://user-images.githubusercontent.com/86579242/218729754-c0739d69-b965-4641-8473-feb0952174ac.gif" width="500" />
</p>

YOLOv5와 DeepSort 알고리즘을 이용하여 영상 속 개인정보를 자동으로 탐지하여 모자이크 처리를 하는 프로그램입니다.

## Requirements

- Python>=3.7.0
- PyTorch>=1.7.
- YOLOv5 release v6.

## Run Project
### installation
```sh
git clone https://github.com/Euron-CV-3TH/YOLOv5_Project.git

pip install -r requirements.txt
pip install pyyaml==5.4.1
```

for gpu

```sh
pip install torch==1.10.1+cu111 torchvision==0.11.2+cu111 torchaudio==0.10.1 -f https://download.pytorch.org/whl/torch_stable.html
```

### run main process

```sh
python main.py --weights 'yolov5/weights/best.pt' --classes 0 1 2 3 --input_path 'vid.mp4'

```

`main.py`를 통해 다양한 객체를 탐지하여 자동으로 모자이크 된 영상을 얻을 수 있습니다.  모자이크 결과물은 `output/results.mp4`에 저장됩니다.

- `--weight`: yolov5의 가중치 파일
- `--input_path`: 모자이크하고자 하는 영상의 Path
- `--classes`: 모자이크 대상 객체


### Classes
|class|class number|
|------|---|
|human|0|
|face|1|
|license plate|2|
|cell phone|3|


## Reference

- [yolov5](https://github.com/ultralytics/yolov5)
- [deepsort_yolov5_pytorch](https://github.com/HowieMa/DeepSORT_YOLOv5_Pytorch)

## Member

`백승민` : YOLOv5+DeepSort 모델 훈련  
`고주은` : YOLOv5+DeepSort 모델 훈련  
`조수빈` : 객체 모자이크 알고리즘 개발   
`송여진` : 객체 모자이크 알고리즘 개발  

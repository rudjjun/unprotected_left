# unprotected_left

biboho/
train , test, val 로 나눠둔 데이터셋 파일 포함

detect_exp7_augmentation/
train2.py로 추론시킨 detect 결과 파일

train_exp3_augmentaion/
train2.py로 추론한 train 결과 파일

best_augementation.pt
- train2.py 학습 결과인 pytorch weight 파일

intall python3.7
  sudo apt install python3.7-dev
  sudo apt install python3.7-venv

prepare source and dataset
  tar xjvf datasets.tar.bz2
  tar xjvf yolov5.tar.bz2

setup environment
  cd yolov5
  python3.7 -m venv yolov5
  source yolov5/bin/activate
  pip install --upgrade pip wheel setuptools
  pip install -r requirments.txt

train model
  python train2.py --cfg --data --weights yolov5s.pt --img 640 --epochs 300

test model
  python detect.py --weights best_augmentation.pt --source biboho/test


  

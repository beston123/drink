# Introduction 
Use YOLOv8 to train a model that can recognize drink bottles

## Training on PC

### 1.Install YOLOv8
```bash
pip install ultralytics
```

### 2.Train model
```bash
# GPU
yolo train data=drink.yaml model=yolov8n-seg.pt epochs=300 imgsz=640 batch=8 workers=0 device=0

# CPU
yolo train data=drink.yaml model=yolov8n-seg.pt epochs=300 imgsz=640 batch=8 workers=0 device=cpu

# Apple silicon chip (M1/M2/M3/M4...)
yolo train data=drink.yaml model=yolov8n-seg.pt epochs=300 imgsz=640 batch=8 workers=0 device=mps
```

### 3.Predict
```bash
yolo predict model=runs/segment/train/weights/best.pt source=IMG_20230418_200057.jpg
```

## Training on Google Colab
https://colab.research.google.com/drive/1lTjH8SVk5DwxxYbkdQwWt7NjnGfgAlwj?usp=sharing

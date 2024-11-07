# Intro 
Use YOLOv8 to train a model that can recognize drink bottles

### 1.Install dependencies 
```bash
pip install ultralytics
```

### 2.Train YOLOv8 model
```bash
# GPU
yolo train data=drink.yaml model=yolov8n-seg.pt epochs=300 imgsz=640 batch=8 workers=0 device=0

# CPU
yolo train data=drink.yaml model=yolov8n-seg.pt epochs=300 imgsz=640 batch=8 workers=0 device=cpu
```

### 3.Predict
```bash
yolo predict model=runs/segment/train/weights/best.pt source=IMG_20230418_200057.jpg
```

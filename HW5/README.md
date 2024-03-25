# HW5

# Train the yolov5 model on coco128 ds and check the performance of model.

### Setup:

Create virtual environment in python
clone the repository from yolov5
install the necessary dependencies

```
git clone https://github.com/ultralytics/yolov5
pip3 install -U -r yolov5/requirements.txt
```

## Model fitting:

Train yolov5 version:
set 100 epochs
set data coco128.yaml
caching images in RAM or to disk

```
python train.py --img 640 --epochs 100 --data coco128.yaml --weights yolov5s.pt --cache
```

Test model on previously downloaded Youtube video. 

```
python detect.py --weights runs/train/exp3/weights/best.pt --img 640 --conf 0.25 --source ../testvideo.mp4
```

## Results

The video is in this in this folder(testvideo_res.mp4)

![](/HW5/testvideo_res.gif)


![](/HW5/results.png)

### F1-confidence curve:  
![](/HW5/F1_curve.png)

### Labels
![](/HW5/labels.jpg)

### Labels correlogram
![](/HW5/labels_correlogram.jpg)

### Confusion matrix:
![](/HW5/confusion_matrix.png)

#### Precision-Recall Curve:
![](/HW5/PR_curve.png)

### Precision-confidance Curve
![](/HW5/P_curve.png)

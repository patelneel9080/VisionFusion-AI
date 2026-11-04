# VisionFusion-AI

### Integrated Face Detection, Object Detection & Image Processing System

VisionFusion-AI is a computer vision project that combines **OpenCV, YuNet, and YOLOv8** to perform image processing, real-time face detection, and object detection. The project also evaluates model performance using FPS measurements and compares edge-based computer vision techniques.

---


## Project Overview

This project demonstrates practical computer vision techniques through five major modules:

1. **Image Processing:** Image loading, thresholding, morphological operations, and noise removal.
2. **Bitwise Operations & Histograms:** Image masking, ROI extraction, watermarking, and histogram analysis.
3. **Face Detection:** Face detection using the YuNet ONNX model, facial landmarks, confidence thresholds, and face blurring.
4. **Object Detection:** Object detection using YOLOv8 Nano, confidence and IoU comparisons, and COCO class analysis.
5. **Integrated Pipeline:** Combined YuNet and YOLO detection, morphological denoising, FPS comparison, and edge-versus-cloud analysis.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| OpenCV | Image processing and computer vision |
| YuNet | Face detection |
| YOLOv8 Nano | Object detection |
| NumPy | Numerical operations |
| Matplotlib | Image and graph visualization |
| Pandas | Data handling and comparison tables |
| Jupyter Notebook | Project implementation |

## Project Structure

```text
VisionFusion-AI/
│
├── data/
│   └── images/
│       ├── apple.jpg
│       ├── Blender_Suzanne1.jpg
│       ├── box.png
│       ├── chessboard.png
│       ├── fruits.jpg
│       ├── HappyFish.jpg
│       ├── lena.jpg
│       ├── messi5.jpg
│
├── models/
│   └── face_detection_yunet_2026may.onnx
│
├── CV_PR3.ipynb
├── yolov8n.pt
└── README.md
```

*Note: The four face images are additional inputs required for the multiple-image YuNet experiments. Add them to `data/images/` before running those notebook sections.*

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/patelneel9080/VisionFusion-AI.git
```

### 2. Navigate to the Project Directory

```bash
cd VisionFusion-AI
```

### 3. Create a Virtual Environment (Optional)

```bash
python -m venv venv
```

Activate it:

**Windows:**
```bash
venv\Scripts\activate
```

**Linux / macOS:**
```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install opencv-python ultralytics matplotlib numpy pandas jupyter
```

### 5. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `CV_PR3.ipynb` and execute the notebook cells in order.

## Models Used

### 1. YuNet Face Detection

YuNet is a lightweight face detection model used to identify human faces in images and video frames.

**Model file:**
`models/face_detection_yunet_2026may.onnx`

**Features:**
- Face bounding box detection.
- Five facial landmark detection.
- Confidence score evaluation.
- Real-time webcam face detection.
- Face privacy protection using Gaussian blur.

Model source: [OpenCV Zoo](https://github.com/opencv/opencv_zoo)

### 2. YOLOv8 Nano Object Detection

YOLOv8 Nano is used for real-time object detection and classification.

**Model file:** `yolov8n.pt`

**Features:**
- Multiple object detection.
- Bounding box visualization.
- Object classification.
- Confidence threshold comparison.
- IoU and Non-Maximum Suppression analysis.
- COCO class detection and counting.

Model documentation: [Ultralytics YOLO](https://docs.ultralytics.com/)

## Project Modules

### Module 1: Image Processing and Morphological Operations

- Load grayscale and colour images.
- Apply binary thresholding.
- Perform erosion and dilation.
- Perform morphological opening and closing.
- Compare RECT, ELLIPSE, and CROSS structuring elements.

### Module 2: Bitwise Operations and Histograms

- Bitwise AND, OR, XOR, and NOT.
- Circular Region of Interest (ROI).
- Watermark creation using bitwise OR.
- Grayscale histogram analysis.
- Blue, Green, and Red channel histograms.
- Image brightness and contrast adjustment.

### Module 3: YuNet Face Detection

- Load the YuNet ONNX model.
- Detect faces in multiple images.
- Display facial landmarks and confidence scores.
- Perform real-time webcam detection.
- Compare confidence thresholds: 0.5, 0.7, and 0.9.
- Apply Gaussian blur to detected faces.

### Module 4: YOLO Object Detection

- Load the YOLOv8 Nano model.
- Detect objects in multiple images.
- Perform real-time webcam detection.
- Compare confidence thresholds: 0.25, 0.50, and 0.75.
- Compare IoU thresholds: 0.3, 0.5, and 0.7.
- Count detected COCO classes and visualize results.

### Module 5: Integrated Computer Vision Pipeline

- Combine YuNet and YOLO detection.
- Display face detections using green bounding boxes.
- Display object detections using red bounding boxes.
- Apply morphological opening for denoising.
- Compare detection results before and after denoising.
- Compare FPS over the same 100 webcam frames.
- Evaluate edge computing and cloud computing.

## Running Real-Time Detection

The notebook includes webcam-based detection using:

- YuNet for face detection.
- YOLOv8 Nano for object detection.
- Combined YuNet + YOLO for integrated detection.

**Instructions:**

1. Connect a webcam.
2. Run the required notebook cell.
3. Allow webcam access.
4. Observe the detection results and FPS.
5. Press `Q` to close the webcam window.

## Performance Evaluation

The project compares three detection configurations:

| Technique | Detection Type |
|---|---|
| YuNet | Face Detection |
| YOLOv8 Nano | Object Detection |
| Combined Pipeline | Face + Object Detection |

FPS is calculated using the same 100 captured webcam frames for each technique. Actual performance depends on hardware, image resolution, and processing resources.

## Applications

- Smart surveillance systems.
- Face detection and attendance systems.
- Real-time object recognition.
- Privacy protection through face blurring.
- Intelligent camera applications.
- Computer vision research and experimentation.

## Future Improvements

- Add face recognition capabilities.
- Integrate object tracking.
- Build a graphical user interface.
- Add more YOLO model variants.
- Optimize detection performance for edge devices.
- Deploy the system using a cloud-based API.

## Learning Outcomes

Through this project, I explored:

- Fundamental image processing techniques.
- Morphological image operations.
- Bitwise image manipulation.
- Histogram analysis.
- Deep learning-based face detection.
- YOLO-based object detection.
- Real-time webcam processing.
- Non-Maximum Suppression and IoU.
- Model performance evaluation using FPS.
- Edge computing versus cloud computing.

## Author

**Neel Patel**

GitHub: [patelneel9080](https://github.com/patelneel9080)

---

## License

This project is intended for educational and learning purposes. Refer to the respective licenses of OpenCV, Ultralytics, and the pretrained model files before redistribution or commercial use.

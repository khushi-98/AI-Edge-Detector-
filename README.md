# 🔍 AI Edge Detector | Python, OpenCV & Gradio

An interactive Computer Vision project that detects object boundaries in images using Python and OpenCV. The application converts an uploaded image into a clean edge-detected representation using the Canny Edge Detection algorithm.

Built as a beginner-friendly AI project to demonstrate how computers process images and identify object outlines.

## 🚀 Project Overview

Computers process images as pixel values rather than understanding objects the way humans do. Edge detection helps identify boundaries by detecting changes in image intensity.

This project allows users to upload an image and instantly visualize its edges through a simple web interface powered by Gradio.

## ✨ Features

- 📤 Upload images through a web interface.
- 🎨 Convert color images into grayscale.
- 🔍 Detect edges using the Canny algorithm.
- 🖥️ View the processed image instantly.
- ⚙️ Experiment with different edge-detection thresholds.
- 🌐 Interactive interface built with Gradio.
- 🎓 Beginner-friendly computer vision project.

## 🛠️ Technologies Used

- Python
- OpenCV
- Gradio
- NumPy

## ⚙️ How It Works

The application follows four main steps:

1. **Image Upload:** The user uploads an image.
2. **Grayscale Conversion:** The color image is converted into grayscale.
3. **Edge Detection:** OpenCV's Canny algorithm identifies significant intensity changes.
4. **Output Display:** The application displays the detected edges.

```text
Input Image
    ↓
Grayscale Conversion
    ↓
Canny Edge Detection
    ↓
Edge-Detected Image
```

## 📂 Project Structure

```text
ai-edge-detector/
│
├── app.py              # Main application
├── requirements.txt    # Project dependencies
├── README.md           # Project documentation
└── screenshots/        # Optional project screenshots
```

## 📦 Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/ai-edge-detector.git
```

### 2. Navigate to the Project Directory

```bash
cd ai-edge-detector
```

### 3. Create a Virtual Environment (Optional)

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Run the Application

```bash
python app.py
```

Open the local URL displayed in your terminal to use the application.

## 📋 Requirements

Add the following dependencies to `requirements.txt`:

```text
opencv-python
gradio
numpy
```

## 💻 Example Implementation

The following is the core edge-detection function:

```python
import cv2
import gradio as gr
import numpy as np

def detect_edges(image):
    if image is None:
        return None

    # Convert RGB image to grayscale
    gray = cv2.cvtColor(image, cv2.COLOR_RGB2GRAY)

    # Apply Canny edge detection
    edges = cv2.Canny(gray, 100, 200)

    return edges

demo = gr.Interface(
    fn=detect_edges,
    inputs=gr.Image(type="numpy"),
    outputs=gr.Image(type="numpy"),
    title="AI Edge Detector",
    description="Upload an image to detect its edges."
)

if __name__ == "__main__":
    demo.launch()
```

## 🌍 Real-World Applications

Edge detection is a fundamental image-processing technique used in:

- 🚗 Autonomous driving and road-scene analysis
- 🤖 Robotics and computer vision
- 🏥 Medical image processing
- 📹 Security and surveillance systems
- 🏭 Industrial inspection and quality control
- 📷 Image analysis and object recognition

*Note: This project demonstrates classical computer vision, not a trained deep-learning model. Edge detection alone does not recognize or classify objects.*

## 🎯 Learning Outcomes

By building this project, you will learn:

- How digital images are represented as pixels.
- Why grayscale conversion is useful in image processing.
- How the Canny Edge Detection algorithm works.
- How to use OpenCV for practical computer vision tasks.
- How to create an interactive Python application with Gradio.

## 🔮 Future Improvements

- Add adjustable Canny threshold controls.
- Support image downloads.
- Add side-by-side original and processed image comparisons.
- Explore contour detection and object segmentation.
- Integrate a trained object-detection model.

## 👩‍💻 Author

**LearnPy — Learn Python, AI & Machine Learning step by step.**

📺 YouTube: https://www.youtube.com/@LearnPy-t4q

📸 Instagram: https://www.instagram.com/learnpy_with_ques/

💬 Telegram: https://t.me/learnpywithradhe

## ⭐ Support

If you find this project helpful, give the repository a ⭐ and share it with other learners!

**Keep learning. Keep building. Grow daily.**

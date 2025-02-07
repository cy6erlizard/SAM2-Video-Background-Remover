# SAM2 Video Background Removal in Google Colab

This project demonstrates live background removal using the Segment Anything 2 (SAM2) model along with a pre-trained Faster R-CNN for body detection—all in Google Colab. Webcam frames are captured, key body points are detected, and the background is replaced with a custom color.

## Requirements

- Python (Colab environment)
- PyTorch 2.0.1+cu118, TorchVision 0.15.2+cu118
- Segment Anything 2 (SAM2)
- OpenCV 4.7.0.72, NumPy 1.23.5, Pillow 9.3.0, Matplotlib 3.7.1, pycocotools 2.0.6, SciPy 1.10.1, timm 0.6.13, onnxruntime-gpu 1.15.0, onnx 1.14.0

## Setup & Usage

1. **Install Dependencies:**  
   Run the provided cell to install required libraries.

2. **Download Model Weights:**  
   The SAM2 model weight (`sam2_hiera_large.pt`) is downloaded via a `wget` command.

3. **Run the Notebook:**  
   - The notebook defines a `Predictor` class that initializes the SAM2 predictor and a Faster R-CNN body detector.
   - Use the provided `take_photo` function to capture frames from your webcam.
   - The predictor processes each frame (detects keypoints, segments the person, and removes the background) and displays the output inline.

4. **Change Background Color:**  
   Pass a different hex code (e.g., `"#FF0000"` for red) to the `process_camera_stream(bg_color=...)` function to change the background color.

## License

This project is for educational purposes. Please comply with the licenses of the underlying models and libraries.

---

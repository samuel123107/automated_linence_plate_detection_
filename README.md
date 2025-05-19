# 🚘 License Plate Detection & OCR using OpenCV and EasyOCR

This project performs automatic **license plate detection and text recognition** from an image using:
- 📷 OpenCV (image processing & contour detection)
- 📖 EasyOCR (optical character recognition)

---

## 📸 Demo

| Step | Output |
|------|--------|
| Original Image | ![](examples/original.jpg) |
| Plate Masked   | ![](examples/masked.jpg) |
| Cropped Plate  | ![](examples/cropped.jpg) |
| Final Result   | ![](examples/final.jpg) |

---

## 🧠 How It Works

1. **Image Preprocessing**
   - Convert to grayscale
   - Apply bilateral filtering (to reduce noise)
   - Detect edges using Canny

2. **Contour Detection**
   - Find contours that are likely rectangles (license plates)
   - Select the contour with 4 edges (assuming the plate is rectangular)

3. **Masking & Cropping**
   - Mask the detected license plate area
   - Crop the plate region for OCR

4. **OCR with EasyOCR**
   - Recognize text from the cropped region
   - Display the detected number plate on the image

---

## 🛠️ Requirements

- Python 3.x
- OpenCV
- imutils
- easyocr
- matplotlib
- numpy

### 🔧 Install with pip:

```bash
pip install opencv-python matplotlib numpy imutils easyocr

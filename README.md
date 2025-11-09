# Data-collection-by-python
# 📸 Face Data Collection Script (Raw, Variable Size)

---

## 🌟 1. Project Overview

This script is a simple, command-line tool designed for **efficient data collection of cropped human faces** using a webcam. It utilizes OpenCV's Haar Cascade classifier to detect a face, crops the bounding box (plus a margin), and saves the resulting image to a specified directory **without resizing or normalization**.

This method is ideal for creating datasets where the images need to preserve their **original scale and aspect ratio** relative to the detection frame. The resulting images will have **variable dimensions**.

---

## ⚙️ 2. Necessary Dependencies

The following Python libraries are required to run this script.

| Library | Purpose | Installation Command |
| :--- | :--- | :--- |
| **OpenCV** (`cv2`) | Core library for video capture, face detection (Haar Cascade), image processing, and file I/O. | `pip install opencv-python` |
| **NumPy** | Used internally by OpenCV for handling image data as numerical arrays. | `pip install numpy` |

---

## 🚀 3. Installation and Setup

1.  **Install Dependencies:**
    ```bash
    pip install opencv-python numpy
    ```
2.  **Haar Cascade File:** Ensure the **`haarcascade_frontalface_default.xml`** file is accessible by OpenCV (it's typically included with the `opencv-python` installation).
3.  **Directory Structure:** The script automatically creates the necessary data folder (e.g., `Data/Face_Raw_Variable`) in the same directory where the script is executed.

---

## 👨‍💻 4. How to Use

1.  **Modify Settings (Optional):** Open the Python file and adjust the following parameters near the top as needed:
    * `cap = cv2.VideoCapture(0)`: Change `0` to `1` or higher if you are using a different webcam.
    * `offset = 40`: Adjust the pixel margin around the detected face.
    * `folder = "Data/Your_Custom_Label"`: **CRITICAL**: Change the folder name to define the label for the data you are collecting (e.g., `Data/Subject_A`).

2.  **Run the Script:**
    ```bash
    python your_script_name.py
    ```
    *Replace `your_script_name.py` with the actual name of your Python file.*

3.  **Collection Controls:**
    * Press **`s`** (save) to capture and save the current cropped face image.
    * Saved files include the dimensions in the name (e.g., `Image_0001_450x512.jpg`).
    * Press **`q`** (quit) to close the application windows and stop the script.

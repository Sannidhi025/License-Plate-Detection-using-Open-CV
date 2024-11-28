# License-Plate-Detection-using-Open-CV

**Overview:**
This project is a Python-based License Plate Recognition system leveraging OpenCV for image processing. It aims to detect and extract license plates from images or video feeds, followed by optical character recognition (OCR) to read the license numbers.

**Features:**
License Plate Detection:
Preprocessing using grayscale conversion, Gaussian blurring, and edge detection.
Contour detection to identify potential license plate regions.
Optical Character Recognition (OCR):
Extracts license plate characters using Tesseract OCR.
Video and Image Support:
Processes both static images and real-time video feeds.
Output:
Annotated images/videos with detected license plate and recognized characters.

**Dependencies:**
Python Libraries:
opencv-python
pytesseract
numpy
matplotlib (optional, for visualization)
Setup
Install Dependencies:
bash
Copy code
pip install opencv-python pytesseract numpy matplotlib
Install Tesseract:
Download and install Tesseract OCR from here.
Configure the tesseract_cmd in the script to point to the Tesseract executable path. Example:
python
Copy code
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
Clone or Download the Repository:
bash
Copy code
git clone https://github.com/your-repository/license-plate-recognition.git
cd license-plate-recognition

**Usage**
Detect License Plate from an Image:

Place your input image in the project directory.
Run the script:
bash
Copy code
python license_plate_recognition.py --image <image_path>
Output: The script displays and saves the image with annotated license plates.
Detect License Plate from a Video Feed:

Run the script:
bash
Copy code
python license_plate_recognition.py --video <video_path>
Output: The script annotates the video in real time and displays the recognized plates.
Real-time Detection with a Camera:

Run the script without specifying a file:
bash
Copy code
python license_plate_recognition.py
Customization
Adjust Detection Parameters:
Modify edge detection and contour filtering thresholds to optimize for different lighting or license plate styles.
OCR Tuning:
Train Tesseract on custom data for improved accuracy on non-standard license plate fonts.
Output
Annotated images/videos with highlighted license plates.
Recognized license numbers printed to the console and optionally saved to a text file.
Limitations
Performance may vary with:
Poor lighting conditions.
Non-standard or damaged license plates.
OCR may require fine-tuning for specific regions or languages.
Future Enhancements
Integrate a deep learning model (e.g., YOLO, TensorFlow) for robust plate detection.
Support multilingual license plate recognition.
Deploy as a real-time system using Flask or FastAPI.

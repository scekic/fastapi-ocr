# OCR Application with FastAPI

This is a simple OCR (Optical Character Recognition) application built using FastAPI. It provides a single endpoint `/ocr` that allows you to upload an image containing text. The application extracts the text from the image and returns it as a string, also saving it to a file.

## Prerequisites

### 1. Install Tesseract on your machine:

- **Ubuntu:**
  ```bash
  sudo apt install tesseract-ocr
- **macOS:**
  ```bash
  brew install tesseract
- **Windows:**

  Download and install Tesseract from [here](https://github.com/UB-Mannheim/tesseract/wiki).

### 2. If using a Windows machine:
Place the correct path to your `tesseract.exe` file in the code. For example:
```python
pytesseract.pytesseract.tesseract_cmd = r'C:\Users\USER\AppData\Local\Programs\Tesseract-OCR\tesseract.exe'
```

## Installation
### 1. Clone the repository:
```bash
git clone https://github.com/scekic/fastapi-ocr.git
cd fastapi-ocr
```
### 2. Create a virtual environment and activate it:
```bash
python -m venv env
source env/bin/activate  # On Windows use `env\Scripts\activate`
```
### 3. Install the required packages:
```bash
pip install -r requirements.txt
```

## Running the Application
### 1. Run the application:
```bash
uvicorn main:app --reload
```
### 2. Open your browser and navigate to:
```bash
http://localhost:8000/docs
```
### 3. Use the `/ocr` endpoint:

- Select the `/ocr` POST endpoint.
- Upload an image file that contains text.
- Execute the request to see the extracted text.

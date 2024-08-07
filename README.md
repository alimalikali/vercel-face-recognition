﻿

# Face Recognition API

## Overview

This project provides a RESTful API for face recognition using Flask and Python. It supports two main functionalities:

1. **Face Recognition**: Recognize faces in an image by comparing them with known faces stored in a MongoDB database.
2. **Upload Known Face**: Upload new faces to the database with associated names.

The API is designed to be hosted on Vercel and uses MongoDB with GridFS for storing images.

## Project Structure

```
/api
    recognize.py  # Endpoint for face recognition
    upload.py     # Endpoint for uploading known faces

vercel.json      # Vercel configuration file
requirements.txt # Python dependencies
```

## Setup

### Prerequisites

- Python 3.7+
- MongoDB instance running locally or remotely
- `pip` for Python package management

### Installation

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/your-username/face-recognition-api.git
    cd face-recognition-api
    ```

2. **Create and Activate a Virtual Environment**:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

4. **Configure MongoDB**:
   - Ensure MongoDB is running on `mongodb://localhost:27017` or update the `MONGO_URI` in the code to point to your MongoDB instance.

## Usage

### Running Locally

1. **Start the Flask Application**:
    ```bash
    python api/recognize.py  # Or use your preferred method to start the Flask app
    ```

2. **Access the Endpoints**:
   - **Face Recognition**: `POST /api/recognize`
   - **Upload Known Face**: `POST /api/upload`

### API Endpoints

- **POST /api/recognize**:
    - **Description**: Recognizes faces in the provided image URL.
    - **Parameters**:
      - `image_url` (form data): URL of the image to be recognized.
    - **Response**: JSON object with recognized face names and IDs.

- **POST /api/upload**:
    - **Description**: Uploads a new face with a name to the database.
    - **Parameters**:
      - `name` (form data): Name associated with the face.
      - `image_url` (form data): URL of the image to be uploaded.
    - **Response**: JSON object with status message and face ID.

## Contact

For any questions or issues, contact [alimalikali1928@gmail.com](mailto:your-email@example.com).


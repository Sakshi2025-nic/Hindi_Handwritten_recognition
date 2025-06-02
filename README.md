# Hindi OCR Web Application

## Description

This project is a web application that provides Hindi Optical Character Recognition (OCR) capabilities. It features a backend API built with FastAPI for processing images, performing word detection, and predicting Hindi text using a pre-trained model. The application also includes user authentication and a feedback system.

## Features

*   **Hindi OCR:** Process images to extract Hindi text.
*   **Word Detection:** Identify and highlight words in the uploaded images.
*   **Text Prediction:** Utilize a machine learning model to predict Hindi characters or words.
*   **User Authentication:** Secure API endpoints with user signup and login.
*   **Feedback System:** Allow users to submit feedback.
*   **Admin Panel:** (Requires admin privileges) View users and feedback.

## Technologies Used

**Backend:**

*   FastAPI (Python)
*   SQLAlchemy (for database interaction)
*   SQLite (database)
*   TensorFlow (for the OCR model)
*   OpenCV (for image processing)
*   py_text_scan (for additional text scanning)
*   Passlib (for password hashing)
*   Uvicorn (ASGI server)

**Frontend:**

*   HTML, CSS (based on the presence of HTML files)

**Machine Learning Model:**

*   Pre-trained Hindi OCR model from Hugging Face.

## Setup and Installation

1.  **Clone the repository:**

    ```bash
    git clone <repository_url>
    cd Web[Frontend]
    ```

2.  **Create a virtual environment (recommended):**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3.  **Install dependencies:**

    ```bash
    pip install -r requirements.txt
    ```
    *(Note: A `requirements.txt` file is needed with the project's dependencies listed.)*

4.  **Download the necessary model files:** The application will attempt to download the model, label encoder, and font file on startup from the specified Hugging Face URLs.

## How to Run the Application

1.  **Start the FastAPI server:**

    ```bash
    uvicorn app:app --reload
    ```

2.  **Access the application:** Open your web browser and go to `http://127.0.0.1:8000`.

## API Endpoints

*   `/token`: User login to get an access token.
*   `/signup`: Register a new user.
*   `/process/`: Process an uploaded image for OCR, word detection, and prediction (requires authentication).
*   `/word-detection/`: Get the word detection image (requires authentication).
*   `/prediction/`: Get the prediction image (requires authentication).
*   `/feedback/`: Submit feedback.
*   `/admin/users/`: Get a list of users (admin only).
*   `/admin/users/{user_id}`: Delete a user (admin only).
*   `/admin/feedback/`: Get a list of feedback entries (admin only).

## Frontend Pages

*   `index.html`: Main page.
*   `about.html`: About page.
*   `contact.html`: Contact page.
*   `examples.html`: Examples page.
*   `feedback.html`: Feedback submission page.
*   `admin.html`: Admin panel page.
*   `recognizer.html`: Page for the OCR functionality.
*   `technology.html`: Technology details page.

## Credits

*   Hindi OCR model: [sameernotes/hindi-ocr](https://huggingface.co/sameernotes/hindi-ocr) on Hugging Face.
*   `py_text_scan` library.

## License

Under the licence of slimshadow org
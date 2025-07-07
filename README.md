# ✍️ Handwritten Digit Recognition Web App 🤖

This is a simple web application built with Python and Flask that uses a trained TensorFlow/Keras model to recognize and classify handwritten digits from an uploaded image. The application provides a web interface where a user can upload an image file, and it will return the predicted digit.

## ⚙️ How It Works

1.  **Upload**: The user uploads an image of a digit through the web interface (`index.html`). 🖼️
2.  **Receive**: The Flask backend receives the uploaded image file. 📥
3.  **Process**: A custom function `prepare_image` processes the image:
    * Converts it to grayscale.
    * Inverts the colors (to match the MNIST dataset format of white digits on a black background).
    * Resizes the image to 28x28 pixels.
    * Normalizes the pixel values to a range between 0 and 1.
    * Reshapes the data to match the input shape required by the model. 🎨
4.  **Predict**: The pre-trained Keras model (`model.hdf5`) predicts the class (a digit from 0-9) based on the processed image data. 🧠
5.  **Display**: The application renders a results page (`result.html`) to display the final prediction to the user. 📊

## 📁 Project Structure

For the application to work correctly, your project should have the following file structure:

## 📋 Prerequisites

* Python 3.7+
* pip (Python package installer)

## 🚀 Setup and Installation

1.  **Clone the repository or download the files.**

2.  **Create a virtual environment (recommended):**
    Open your terminal or command prompt and navigate to the project directory.
    ```bash
    # Create a virtual environment
    python -m venv venv

    # Activate the virtual environment
    # On Windows:
    .\venv\Scripts\activate
    # On macOS/Linux:
    source venv/bin/activate
    ```

3.  **Create the `requirements.txt` file** with the following content:
    ```
    Flask
    tensorflow
    numpy
    Pillow
    ```

4.  **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```

## ▶️ Running the Application

1.  Make sure you are in the project's root directory and your virtual environment is activated.

2.  Run the Flask application from your terminal:
    ```bash
    python app.py
    ```

3.  You should see output indicating that the server is running, similar to this:
    ```
     * Serving Flask app 'app'
     * Running on [http://127.0.0.1:5000](http://127.0.0.1:5000) (Press CTRL+C to quit)
    ```

4.  Open your web browser and navigate to the following URL: 🌐
    [http://127.0.0.1:5000/](http://127.0.0.1:5000/)

5.  Upload an image of a handwritten digit and click "Submit" to see the prediction!

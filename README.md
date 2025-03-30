# Calorie Estimator API

This repository contains a Flask application that estimates the calories of a given food image using the `meta-llama/llama-3-2-90b-vision-instruct` model from IBM Watsonx.

## Installation

### Prerequisites
Ensure you have Python installed (Python 3.8 or later is recommended).

### Setup
Clone this repository and navigate to its directory:
```bash
git clone https://github.com/talebsidelmoktar/calories_calculator_uisng_llama3_vision_model
cd calories_calculator_uisng_llama3_vision_model
```

Install the required dependencies:
```bash
pip install ibm-watsonx-ai==1.1.20 image==1.5.33 flask requests==2.32.0
```

## Running the Application

To start the Flask server, run:
```bash
python app.py
```
The server will start on `http://127.0.0.1:5000/` by default.

## API Usage

### Endpoint: `/predict`
**Method:** POST

**Request:** Send an image file as a `multipart/form-data` request.

**Example using cURL:**
```bash
curl -X POST "http://127.0.0.1:5000/predict" -F "image=@path/to/food_image.jpg"
```

**Response:**
```json
{
  "calories": "Estimated calories value"
}
```

## Contributing
Feel free to fork this repository and make improvements. Pull requests are welcome!

## License
This project is licensed under the MIT License.


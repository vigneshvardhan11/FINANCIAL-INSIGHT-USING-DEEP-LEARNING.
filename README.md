
# Stock Price Prediction Django Application

This project is a Django-based web application that predicts and compares stock prices using machine learning models. The application fetches stock data from Yahoo Finance and uses TensorFlow and Keras for prediction models.

## Table of Contents
- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Technologies Used](#technologies-used)
- [File Paths](#file-paths)
- [License](#license)

## Features
- Fetch stock data from Yahoo Finance using `yfinance`.
- Perform stock price predictions using LSTM models from TensorFlow/Keras.
- Compare multiple stocks based on open, high, low, close, and volume metrics.
- Download stock data and predictions in CSV format.
- Pagination and filtering for stock data.

## Project Structure
```
StockPricePrediction/
│
├── StockPricePrediction/          # Main Django app configuration
├── StockPricePredictionApp/       # Core app for stock prediction
├── static/                        # Static files (CSS, JS, images)
├── templates/                     # HTML templates
├── db.sqlite3                     # SQLite database
├── manage.py                      # Django management script
├── all_stocks.csv                 # CSV file containing stock data
└── README.md                      # Project documentation
```

## Installation

### Prerequisites
- Python 3.x
- pip (Python package manager)
- Git (optional for cloning the repository)

### Steps

1. **Clone the Repository** (optional, if you haven't already downloaded the project):

    ```bash
    git clone https://github.com/your-username/your-repo.git
    cd your-repo
    ```

2. **Create a Virtual Environment** (recommended):

    ```bash
    python -m venv venv
    ```

    Activate the virtual environment:
    - For Windows:
      ```bash
      venv\Scripts\activate
      ```
    - For macOS/Linux:
      ```bash
      source venv/bin/activate
      ```

3. **Install Required Dependencies**:

    Make sure you are inside your project directory and run:

    ```bash
    pip install -r requirements.txt
    ```

    If you don't have a `requirements.txt` file, you can manually install the dependencies:

    ```bash
    pip install django pandas yfinance scikit-learn tensorflow keras
    ```

4. **Apply Database Migrations**:

    Run the following command to apply migrations to your SQLite database:

    ```bash
    python manage.py migrate
    ```

5. **Start the Development Server**:

    ```bash
    python manage.py runserver
    ```

6. **Access the Application**:

    Open your browser and navigate to `http://127.0.0.1:8000/`.

## Usage

### Home Page
- Enter a stock symbol (e.g., `AAPL` for Apple) and select a date range to view stock price history.
- You can also view detailed metrics such as open, high, low, close prices, and volume.

### Stock Prediction
- Input a stock symbol and the number of days for future predictions. The model will generate future stock price predictions based on historical data.

### Compare Stocks
- Input two stock symbols and a date range to compare metrics between the two stocks.

### CSV Download
- You can download the stock data and predictions as CSV files by clicking the "Download" button on the respective pages.

## Technologies Used
- **Backend**: Django, Python
- **Machine Learning**: TensorFlow, Keras, scikit-learn
- **Data**: yfinance for fetching stock data
- **Frontend**: HTML, CSS (via static files)
- **Database**: SQLite (default Django DB)

## File Paths

- **all_stocks.csv**: The CSV file containing the list of stocks and their details.
    - If the file is located in a different folder, ensure the file path in the code is updated accordingly using `os.path.join()` for portability.

- **Static and Template Files**: 
    - HTML files are stored in the `templates/` directory.
    - CSS and JS files are stored in the `static/` directory.

- **Database**: The default database is `db.sqlite3`, which is included in the root directory.

## License
This project is open-source and available for modification and distribution. 

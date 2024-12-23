# Compute Platform

## Overview
Compute Platform is a web application that enables users to upload CSV or Excel files and perform common data operations such as sum, average, mean, max, and min on specific columns. The application provides an intuitive interface for processing data and retrieves accurate results by leveraging AI-powered Python function generation.

## Features
- **File Upload**: Support for CSV and Excel files.
- **Data Operations**: Perform sum, average, mean, max, and min on selected columns.
- **AI-Driven Function Generation**: Backend integrates with Gemini 1.5 Flash to dynamically generate Python functions for requested operations.
- **Database Logging**: Tracks user activity including:
  - User ID
  - File name
  - Operation performed
  - Result obtained
  - Timestamp (date and time)
- **Result Fetching**: Users can retrieve previously performed operation results.

## Technologies Used
- **Framework**: Streamlit
- **Backend**: Python
- **AI Integration**: Gemini 1.5 Flash
- **Database**: SQLite3
- **File Handling**: Pandas


## Installation

### Steps
1. Clone the repository:
   ```bash
   git clone 
   cd compute-platform
   ```
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Change the API key:
   In the .env file type your Gemini Key.
4. Start the development server:
   ```bash
   streamlit run app.py
   ```
5. Open the web application in your browser:
   The webpage will run by default. If it did not, copy
   the link in your terminal and run on your browser.
   ```bash
      You can now view your Streamlit app in your browser.

      Local URL: http://localhost:8501
      Network URL: http://192.168.1.3:8501
   ```
   

## Usage
1. Upload a CSV or Excel file via the web interface.
2. Select a column and choose an operation (sum, average, mean, max, or min).
3. Submit the request.
4. View the result displayed on the web application.
5. Retrieve previously processed results by selecting "Fetch Results" option in-place of "Compute Results".

## API Workflow
1. **Operation Request**:
   - The backend sends a prompt to Gemini 1.5 Flash specifying the operation
   - Receives the generated Python function as a response.
2. **Function Execution**:
   - The function is executed with the selected column data passed as input.
3. **Database Logging**:
   - Logs details such as User ID, file name, operation, result, and timestamp in SQLite3.

## Project Structure
```plaintext
compute-platform/
├── app.py           # Main application file
├── funtions.py      # Helper functions
├── database.py      # Handles database
├── requirements.txt # Dependencies
└── README.md        # Project documentation
```


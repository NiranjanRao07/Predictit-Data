# Raw PredictIt ETL Pipeline

## About

This project demonstrates the creation of an ETL pipeline using Apache Airflow to scrape JSON data from the PredictIt API and upload it to Amazon S3. The pipeline is designed to automate the extraction and storage of market data, showcasing the capabilities of cloud orchestration with Airflow.

## Project Structure

The project consists of two main files:

1. **`raw_predict.py`**: This file contains the Airflow DAG (Directed Acyclic Graph) that orchestrates the data extraction and uploading process.
2. **`test_raw_predictit.py`**: This file serves as a testing script to verify the functionality of the JSON scraper without the Airflow context.

## Technologies Used

- **Apache Airflow**: A platform to programmatically author, schedule, and monitor workflows.
- **Boto3**: The Amazon Web Services (AWS) SDK for Python, which allows Python developers to write software that makes use of Amazon services.
- **Requests**: A simple and elegant HTTP library for Python, used to make API requests.

## Setup Instructions

### Prerequisites

- Python 3.x
- Airflow installed and set up
- Boto3 library for AWS interactions
- Access to Amazon S3 (Note: This project currently requires access to S3. The free trial for AWS has expired, so S3 functionality is not currently available.)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/repository-name.git
   cd repository-name
   ```

2. Install required packages:
   ```bash
   pip install apache-airflow boto3 requests
   ```

## Usage

### Running the Airflow DAG

1. Ensure your Airflow environment is running.
2. Place the `raw_predict.py` file in the `dags` folder of your Airflow installation.
3. Access the Airflow UI (usually at `http://localhost:8080`).
4. Enable the `raw_predictit` DAG.
5. Trigger the DAG to run the data extraction process.

### Testing the JSON Scraper

You can run the `test_raw_predictit.py` script directly to test the JSON scraper without using Airflow:

```bash
python test_raw_predictit.py
```

### Note

As I no longer have access to Amazon S3 due to the expiration of my free trial, the upload functionality is commented out in the code. However, the core functionality of scraping the JSON data from the PredictIt API is intact and can be tested locally.

## Conclusion

This project serves as a foundational example of building an ETL pipeline using Airflow, highlighting how to automate data extraction from an API and store it in cloud storage. Future enhancements could include re-enabling the S3 integration and adding additional data transformation steps.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

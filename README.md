# ML-Powered Network Security Platform

This project is designed to provide a comprehensive solution for network security using machine learning models. It includes data ingestion, validation, transformation, model training, and prediction functionalities. The project is built using Python and leverages various libraries and tools such as FastAPI, scikit-learn, MLflow, and Docker.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Endpoints](#endpoints)
- [Model Training](#model-training)
- [Docker Deployment](#docker-deployment)
- [Continuous Integration and Deployment](#continuous-integration-and-deployment)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Installation

### Prerequisites

- Python 3.10
- Docker
- AWS CLI (for deployment)

### Steps

* Clone the repository:
    ```sh
    git clone https://github.com/yourusername/networksecurity.git
    cd networksecurity
    ```
* Create and activate a virtual environment:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

* Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

## Usage

* Start the FastAPI application:
    ```sh
    python app.py
    ```

* Access the API documentation at `http://localhost:8000/docs`.

## Project Structure

```bash
NETWORK_SECURITY
├── .github/
│   └── workflows/
│       └── main.yml
├── data_schema/
│   └── schema.yaml
├── final_model/
│   ├── model.pkl
│   └── preprocessor.pkl
├── network_data/
│   └── phisingData.csv
├── networksecurity/
│   ├── cloud/
│   ├── components/
│   ├── constants/
│   ├── entity/
│   ├── exception/
│   ├── logging/
│   ├── pipeline/
│   └── utils/
├── notebooks/
├── prediction_output/
│   └── output.csv
├── templates/
│   └── table.html
└── valid_data/
    └── test.csv

```


## Endpoints

- `GET /`: Root endpoint
- `GET /train`: Train the model
- `POST /predict`: Make predictions

## Model Training

To train the model, you can use the `/train` endpoint:
```sh
curl -X GET "http://localhost:8000/train"
```
## Docker Deployment

* Build the Docker image:
```sh
docker build -t networksecurity:latest .
```

* Run the Docker container:
```sh
docker run -d -p 8000:8000 networksecurity:latest
```


## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## License
This project is licensed under the MIT License.


Contact
Author: Hetav Raval
Email: raval.hetav@gmail.com


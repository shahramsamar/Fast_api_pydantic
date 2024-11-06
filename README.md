# FastAPI Pydantic

A Python project that demonstrates the use of **Pydantic** models with **FastAPI** to handle data validation, serialization, and deserialization in web applications. This project showcases how Pydantic integrates with FastAPI to ensure data integrity and type safety.

## Features

- **Pydantic Integration**: Uses Pydantic models to validate and parse incoming request data.
- **Data Validation**: Ensures the correctness of input data with type-checking and custom validation rules.
- **Request and Response Models**: Defines models for handling requests and responses, ensuring data consistency.
- **Easy Serialization**: Automatically converts Python objects to JSON responses using Pydantic's `jsonable_encoder` method.
- **Error Handling**: Provides detailed error messages when invalid data is received.

## Requirements

- **Python 3.x**
- **FastAPI**
- **Pydantic** (for data validation)

### Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/shahramsamar/Fast_api_pydantic.git
    cd Fast_api_pydantic
    ```

2. **Install Dependencies:**

    If you're using `pip`, run:

    ```bash
    pip install -r requirements.txt
    ```

3. **Run the Application**:

    To run the FastAPI app:

    ```bash
    uvicorn main:app --reload
    ```

### How to Use

1. **Create Request Data**:
   - Define your Pydantic models in `schemas.py` to describe the data structure.
   - Use these models in your FastAPI routes to validate incoming requests.

2. **Response Handling**:
   - Use Pydantic models to structure the response data returned from your routes.

3. **Test the Endpoints**:
   - Use FastAPI’s auto-generated Swagger UI or API documentation to interact with your endpoints and test them in real-time:
     ```bash
     http://127.0.0.1:8000/docs
     ```

4. **Example Request**:
   - Send a POST request to `/items` with the following JSON data:
     ```json
     {
       "name": "Sample Item",
       "description": "This is a sample item",
       "price": 10.5
     }
     ```

5. **Example Response**:
   - The response will return the same data with validation applied:
     ```json
     {
       "name": "Sample Item",
       "description": "This is a sample item",
       "price": 10.5
     }
     ```

### Project Structure

- `main.py`: Contains the FastAPI application, routes, and logic for handling Pydantic models.
- `schemas.py`: Defines the Pydantic models used for request and response validation.
- `requirements.txt`: Lists necessary libraries like `FastAPI`, `Pydantic`, etc.

## Contributing

Feel free to fork the project and submit pull requests for new features, improvements, or bug fixes.

## License

This project is open-source and available for educational purposes.

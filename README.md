# Flask Web Calculator🧮

This is a simple web calculator application built using Flask, a lightweight Python web framework. The calculator allows users to perform basic arithmetic operations such as addition, subtraction, multiplication, and division.

## Features

- Perform arithmetic operations: addition, subtraction, multiplication, and division.
- Accepts input via JSON format for easy testing with tools like Postman.

## Usage

### Installation

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/your-username/flask-web-calculator.git
   ```

2. Navigate to the project directory:

   ```bash
   cd flask-web-calculator
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

### Running the Application

1. Start the Flask server:

   ```bash
   python app.py
   ```

2. The server will start running on `http://localhost:5000/`.

### Using the Calculator

You can use the calculator by sending POST requests to the `/calculate` endpoint with the following JSON payload:

```json
{
  "operation": "add",
  "number1": 5,
  "number2": 3
}
```

- `"operation"`: The arithmetic operation to perform (`add`, `subtract`, `multiply`, `divide`).
- `"number1"`: The first number.
- `"number2"`: The second number.

The server will respond with the result of the calculation in JSON format.

### Example

#### Request

```http
POST /calculate HTTP/1.1
Host: localhost:5000
Content-Type: application/json

{
  "operation": "add",
  "number1": 5,
  "number2": 3
}
```

#### Response

```json
{
  "result": 8
}
```

## Contributing

Contributions are welcome! If you'd like to contribute to this project, please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

# Simple Go Web Server

This is a basic web server implemented in Go. It serves static files and handles basic GET and POST requests.

## Features

- **Static File Server**: Serves files from the `./static` directory.
- **Hello Handler**: Responds to GET requests at `/hello` with a simple greeting.
- **Form Handler**: Accepts POST requests at `/form` and responds with the submitted form data.

## Project Structure

├── main.go 
└── static 
    └── (your static files here)


- **`main.go`**: Contains the main server code.
- **`static/`**: Directory for static files like HTML, CSS, JS, etc.

## Endpoints

- `GET /hello`: Returns a simple "Hello!" message.
- `POST /form`: Processes form data and returns the submitted `name` and `address`.

## Running the Server

To run the server, execute the following command:

```bash
go run main.go

The server will start on port 8080. You can access it in your browser at http://localhost:8080.

Example Usage
1. Serving Static Files
Place your static files (e.g., index.html, style.css) in the static directory. They will be accessible from the root path (/).

2. Hello Handler
Send a GET request to /hello:

`curl http://localhost:8080/hello`

Response:
`Hello!`

3. Form Handler
Send a POST request to /form with form data:
`curl -X POST -d "name=John Doe&address=123 Main St" http://localhost:8080/form`

Response:
```POST request Successfully
Name = John Doe
Address = 123 Main St```

Error Handling
- 404 Not Found: Returned if the requested URL path is not /hello or /form.
- 405 Method Not Allowed: Returned if the request method is not supported (e.g., POST on /hello).

Dependencies
- This project uses only the standard Go library.

License
This project is licensed under the MIT License.

This README provides a comprehensive overview of your project, including how to run it, its structure, endpoints, and example usage.

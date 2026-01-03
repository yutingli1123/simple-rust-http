# Simple Rust HTTP Server

This is a simple, multi-threaded HTTP server implementation in Rust. It demonstrates how to build a basic web server from scratch using the standard library, including a custom thread pool for handling concurrent connections.

This project is based on the final project from [The Rust Programming Language](https://doc.rust-lang.org/book/ch20-00-final-project-a-web-server.html) book.

## Features

- **Multi-threaded**: Uses a custom `ThreadPool` to handle multiple requests concurrently.
- **Basic Routing**:
  - `GET /`: Returns `hello.html`.
  - `GET /sleep`: Simulates a slow request (5 seconds delay) and returns `hello.html`.
  - Other paths: Returns `404.html`.
- **Graceful Shutdown**: The server is configured to shut down gracefully (currently set to shut down after 2 requests for demonstration purposes).

## Project Structure

- `src/main.rs`: The entry point of the application, containing the server setup and request handling logic.
- `src/lib.rs`: Contains the `ThreadPool` implementation.
- `hello.html`: The default HTML page served.
- `404.html`: The error page served for unknown routes.

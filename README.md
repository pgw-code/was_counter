# Rust + WebAssembly Counter Example

This is a simple counter web application built with Rust and WebAssembly (Wasm). The application allows users to increment and decrement a counter displayed on a web page. The core logic is implemented in Rust, while a minimal amount of JavaScript is used to interact with the DOM.

## Features

- Written in Rust, compiled to WebAssembly.
- Minimal JavaScript for DOM manipulation.
- Simple user interface with increment and decrement buttons.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Rust](https://www.rust-lang.org/tools/install)
- [wasm-pack](https://rustwasm.github.io/wasm-pack/installer/)
- Python (for serving the application locally)

## Installation

1. **Clone the repository:**

   ```sh
   git clone https://github.com/yourusername/wasm_counter.git
   cd wasm_counter
   ```
2. **Build the WebAssembly package:**
  
  ```sh
  wasm-pack build --target web
  ```

3. **Running the Application:**
   To run the application locally, you can use a simple HTTP server. Here’s how to do it with Python:
  
    ```sh
    python3 -m http.server 8080
   ```
 
   Open your browser and navigate to http://localhost:8080

## Project Structure

**src/lib.rs:** The main Rust code that defines the Counter struct and its methods.

**Cargo.toml**: Configuration file specifying the project dependencies and crate type.

**index.html**: The HTML file that includes the user interface and JavaScript to interact with the Rust WebAssembly module.

**pkg/:** The output directory where the WebAssembly and JavaScript files are generated after running wasm-pack build.

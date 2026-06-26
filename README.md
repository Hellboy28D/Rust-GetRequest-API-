🦀 Rust GET Request API

A simple Rust project demonstrating how to make HTTP GET requests, retrieve API responses, and process response data using reqwest.

This project was built as part of my Rust learning journey to understand networking, APIs, and error handling in Rust.

⸻

✨ Features

* Send HTTP GET requests
* Fetch data from external APIs
* Read response bodies
* Display HTTP status codes
* View response headers
* Handle errors cleanly
* Learn Rust networking basics

⸻

📸 Project Overview

This project sends a GET request to an API endpoint and retrieves:

✅ Response status
✅ Headers
✅ Response body

Example flow:

Application
     ↓
Send GET Request
     ↓
API Server
     ↓
Receive Response
     ↓
Parse & Display Data

⸻

🛠 Tech Stack

* Rust 🦀
* Reqwest
* Anyhow (Error handling)

⸻

📦 Dependencies

[dependencies]
reqwest = { version = "0.12", features = ["blocking", "json"] }
anyhow = "1.0"

⸻

💻 Example Code

use anyhow::Result;
use std::io::Read;
fn main() -> Result<()> {
    let mut res = reqwest::blocking::get(
        "http://httpbin.org/get"
    )?;
    let mut body = String::new();
    res.read_to_string(&mut body)?;
    println!("Status: {}", res.status());
    println!("Headers:\n{:#?}", res.headers());
    println!("Body:\n{}", body);
    Ok(())
}

⸻

▶ Getting Started

Clone the repository:

git clone https://github.com/Hellboy28D/Rust-GetRequest-API-.git

Move into the project:

cd Rust-GetRequest

Run the application:

cargo run

⸻

📂 Project Structure

Rust-GetRequest
│
├── src
│   └── main.rs
│
├── Cargo.toml
├── Cargo.lock
├── README.md
└── .gitignore

⸻

🎯 Learning Goals

This project helped me understand:

✅ HTTP requests in Rust
✅ API communication
✅ External crate usage
✅ Error handling
✅ Reading server responses
✅ Rust project structure

⸻

🚀 Future Improvements

* Support POST requests
* Add async API requests
* Parse JSON responses automatically
* Build a command-line interface
* Add multiple API endpoints

⸻

Made with 🦀 + ☕ + curiosity

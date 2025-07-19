# Timestamp Microservice

A simple and reliable API that returns Unix and UTC timestamps for any valid date string or Unix timestamp.  
Perfect for quick date conversions and timestamp lookups.

## Features

- Get the current time in Unix and UTC formats.
- Convert a date string or Unix timestamp to both Unix and UTC time.
- Gracefully handles invalid date inputs with clear error messages.

## Usage

- **GET /**  
  Home page.

- **GET /api/:date?**  
  - If `:date` is empty, returns the current time.  
  - If `:date` is a valid date string or Unix timestamp, returns the corresponding time.  
  - If `:date` is invalid, returns `{ "error": "Invalid Date" }`.

## Examples

- `/api/2015-12-25`  
  `{ "unix": 1451001600000, "utc": "Fri, 25 Dec 2015 00:00:00 GMT" }`

- `/api/1451001600000`  
  `{ "unix": 1451001600000, "utc": "Fri, 25 Dec 2015 00:00:00 GMT" }`

- `/api/invalid-date`  
  `{ "error": "Invalid Date" }`

## Getting Started

Follow these steps to run the project locally:

1. **Clone the repository**
   ```sh
   git clone https://github.com/sabbas-ctrl/Timestamp-Microservice.git
   cd Timestamp-Microservice
   ```

2. **Install dependencies**
   ```sh
   npm run dev
   ```

3. **Start the server**
   ```sh
   npm start
   ```
   The API will be running at `http://localhost:3000/`.

---

Inspired by a microservice challenge from freeCodeCamp.

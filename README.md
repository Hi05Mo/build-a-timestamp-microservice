# Timestamp Microservice

A simple timestamp microservice built with Node.js and Express.js.

## Description

This project provides an API that converts dates into Unix timestamps and UTC date strings.

It accepts a Unix timestamp or a date string, returns the current date and time when no date is provided, and handles invalid dates with an error response.

## Technologies

* JavaScript
* Node.js
* Express.js
* CORS
* ES Modules

## Usage

Install the dependencies:

```bash
npm install
```

Start the server with:

```bash
npm start
```

The server runs on:

`http://localhost:8000`

Available routes:

```http
GET /
GET /api
GET /api/:date
```

### Timestamp API

The `/api/:date` endpoint accepts a Unix timestamp in milliseconds or a date string and returns the timestamp and UTC date.

Example request:

```http
GET /api/1451001600000
```

Example response:

```json
{
  "unix": 1451001600000,
  "utc": "Fri, 25 Dec 2015 00:00:00 GMT"
}
```

### Current Timestamp

The `/api` endpoint returns the current date and time.

### Invalid Date

If the provided date is invalid, the API returns:

```json
{
  "error": "Invalid Date"
}
```

## Project Structure

```text
build-a-timestamp-microservice/
├── public/
│   └── style.css
├── views/
│   └── index.html
├── server.js
├── package.json
├── package-lock.json
├── .gitignore
└── README.md
```

## License

MIT

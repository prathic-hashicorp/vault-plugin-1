# Echo API Server

A simple Go API server that echoes back user input.

## Running the Server

```bash
go run main.go
```

The server will start on `http://localhost:8080`

## Endpoints

### POST /echo
Accepts JSON input and returns it back.

**Request:**
```json
{
  "message": "Hello, World!"
}
```

**Response:**
```json
{
  "echo": "Hello, World!"
}
```

### GET /health
Health check endpoint that returns "OK".

## Example Usage

```bash
curl -X POST http://localhost:8080/echo \
  -H "Content-Type: application/json" \
  -d '{"message": "Hello from the API!"}'
```

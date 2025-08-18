# ngrok Python SDK Quickstart

A minimal Python app demonstrating the ngrok Python SDK.

## What you'll need

- An [ngrok account](https://dashboard.ngrok.com/signup).
- Your [ngrok auth token](https://dashboard.ngrok.com/get-started/your-authtoken).
- [Python installed](https://www.python.org/downloads/) on your machine.

## Setup

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Create a `.env` file from the example:
   ```bash
   cp .env.example .env
   ```

3. Add your ngrok auth token to the `.env` file:
   ```txt
   NGROK_AUTHTOKEN=your_actual_authtoken_here
   ```

4. Reserve a domain in the [ngrok dashboard](https://dashboard.ngrok.com/domains) and add it to the `.env` file:
   ```txt
   NGROK_RESERVED_DOMAIN=your_actual_authtoken_here
   ```

## Running the app

1. Start the Python service:
   ```bash
   python service.py
   ```

2. In another terminal, start the ngrok agent endpoint:
   ```bash
   python endpoint.py
   ```

The ngrok agent endpoint will output a URL that forwards traffic to your local app.

## Files

- `service.py` - Basic Python HTTP server
- `endpoint.py` - ngrok agent endpoint configuration with OAuth
- `.env.example` - Environment variable template
- `requirements.txt` - Python dependencies

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

4. (Optional) Reserve a domain in the [ngrok dashboard](https://dashboard.ngrok.com/domains) and update the `domain` parameter in `example.py`.

## Running the app

1. Start the Python service:
   ```bash
   python service.py
   ```

2. In another terminal, start the ngrok agent endpoint:
   ```bash
   python example.py
   ```

The ngrok agent endpoint will output a URL that forwards traffic to your local app. If you configured OAuth, visitors will need to log in with Google to access it.

## Files

- `service.py` - Basic Python HTTP server
- `example.py` - ngrok agent endpoint configuration with OAuth
- `.env.example` - Environment variable template
- `requirements.txt` - Python dependencies

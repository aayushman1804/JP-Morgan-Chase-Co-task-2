<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Task 1: Stock Price Data Feed</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #333;
            color: #fff;
            padding: 10px 0;
            text-align: center;
        }
        .container {
            padding: 20px;
            max-width: 1000px;
            margin: 0 auto;
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            color: #333;
        }
        h2 {
            color: #555;
        }
        code {
            background-color: #f4f4f4;
            padding: 2px 4px;
            font-size: 1.1rem;
            border-radius: 4px;
        }
        .code-block {
            background-color: #eee;
            padding: 10px;
            border-radius: 5px;
            margin-top: 10px;
            font-family: monospace;
        }
        footer {
            margin-top: 20px;
            text-align: center;
            color: #888;
        }
    </style>
</head>
<body>
    <header>
        <h1>J.P. Morgan Virtual Experience Program</h1>
        <p><strong>Task 1: Interface with a Stock Price Data Feed</strong></p>
    </header>
    <div class="container">
        <h2>Overview</h2>
        <p>
            This project simulates interfacing with a stock price data feed to retrieve and process real-time stock prices. The feed provides live data from J.P. Morgan’s financial systems, and the objective is to monitor and calculate changes in stock prices in real time.
        </p>

        <h2>Objective</h2>
        <p>
            The goal of this task is to develop a Python client that can:
        </p>
        <ul>
            <li>Connect to a simulated stock price data feed API.</li>
            <li>Receive and process real-time stock price data.</li>
            <li>Calculate the price change for each stock in the feed.</li>
        </ul>

        <h2>Technologies Used</h2>
        <ul>
            <li><strong>Python:</strong> Backend programming to handle data feed and calculations.</li>
            <li><strong>Websockets:</strong> Used for real-time data exchange.</li>
        </ul>

        <h2>Code Snippets</h2>
        <p>Below is a simplified version of the main Python code that connects to the stock data feed and calculates stock price changes:</p>
        <div class="code-block">
            <code>
# client3.py
import websocket
import json

def on_message(ws, message):
    data = json.loads(message)
    stock_symbol = data['stock_symbol']
    price = data['price']
    print(f"Received data for {stock_symbol}: {price}")

def on_error(ws, error):
    print(f"Error: {error}")

def on_close(ws):
    print("Connection closed")

def on_open(ws):
    print("Connection opened")

if __name__ == "__main__":
    ws = websocket.WebSocketApp("ws://stock-data-feed-url",
                                on_message=on_message,
                                on_error=on_error,
                                on_close=on_close)
    ws.on_open = on_open
    ws.run_forever()
            </code>
        </div>

        <h2>Steps to Run the Application</h2>
        <ol>
            <li>Clone the repository to your local machine:</li>
            <div class="code-block">
                <code>git clone https://github.com/yourusername/forage-jpmc-swe-task-1.git</code>
            </div>
            <li>Navigate to the project directory:</li>
            <div class="code-block">
                <code>cd forage-jpmc-swe-task-1</code>
            </div>
            <li>Install the necessary dependencies using <strong>pip</strong>:</li>
            <div class="code-block">
                <code>pip install -r requirements.txt</code>
            </div>
            <li>Run the Python client:</li>
            <div class="code-block">
                <code>python client3.py</code>
            </div>
            <li>Observe the stock price changes printed in the console.</li>
        </ol>

        <h2>Expected Output</h2>
        <p>
            After running the program, you should see real-time stock price data similar to the example below:
        </p>
        <div class="code-block">
            <code>
Received data for AAPL: 145.32
Received data for TSLA: 653.22
Received data for MSFT: 300.10
            </code>
        </div>

        <footer>
            <p>&copy; 2024 J.P. Morgan Virtual Experience | Task 1: Interface with Stock Price Data Feed</p>
        </footer>
    </div>
</body>
</html>

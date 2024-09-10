<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Task 1: Stock Price Data Feed</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f0f0f0;
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #0056b3;
            color: white;
            padding: 20px;
            text-align: center;
            font-size: 24px;
        }
        .container {
            max-width: 900px;
            margin: 20px auto;
            background-color: white;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }
        h1, h2 {
            color: #0056b3;
        }
        p {
            font-size: 14px;
            line-height: 1.6;
        }
        code, .code-block {
            background-color: #f4f4f4;
            padding: 10px;
            border-radius: 5px;
            font-family: 'Courier New', Courier, monospace;
            font-size: 14px;
        }
        .code-block {
            display: block;
            margin: 10px 0;
        }
        footer {
            text-align: center;
            margin-top: 20px;
            font-size: 12px;
            color: #777;
        }
    </style>
</head>
<body>

<header>
    J.P. Morgan Virtual Experience <br> Task 1: Stock Price Data Feed
</header>

<div class="container">
    <h1>Overview</h1>
    <p>
        A Python client connecting to a stock price data feed, processing real-time prices, and calculating changes.
    </p>
    <h2>Tech Stack</h2>
    <p>
        <strong>Python</strong>, WebSockets, JSON.
    </p>
    <h2>Quick Start</h2>
    <p>Clone the repo and run the client:</p>
    <pre class="code-block">git clone https://github.com/yourusername/forage-jpmc-swe-task-1.git</pre>
    <pre class="code-block">cd forage-jpmc-swe-task-1</pre>
    <pre class="code-block">pip install -r requirements.txt</pre>
    <pre class="code-block">python client3.py</pre>
    <h2>Sample Output</h2>
    <pre class="code-block">
Received data for AAPL: 145.32
Received data for TSLA: 653.22
Received data for MSFT: 300.10
    </pre>
    <footer>
        &copy; 2024 J.P. Morgan Virtual Experience - Task 1
    </footer>
</div>

</body>
</html>

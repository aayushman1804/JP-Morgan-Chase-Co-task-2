<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <h1>Task 2: Perspective Framework</h1>
   
</head>
<body>

<div class="container">
    <h1>Overview</h1>
    <p>
        Implementing the Perspective framework to create interactive financial data visualizations for stock prices in a real-time web application.
    </p>
    <h2>Tech Stack</h2>
    <p>
        <strong>HTML</strong>, <strong>JavaScript</strong>, <strong>Perspective.js</strong>.
    </p>
    <h2>Quick Start</h2>
    <p>Clone the repo and run the app:</p>
    <pre class="code-block">git clone https://github.com/yourusername/forage-jpmc-swe-task-2.git</pre>
    <pre class="code-block">cd forage-jpmc-swe-task-2</pre>
    <pre class="code-block">npm install</pre>
    <pre class="code-block">npm start</pre>
    <h2>Sample Code</h2>
    <p>Example of integrating Perspective into the web app:</p>
    <pre class="code-block">
const elem = document.getElementById("perspective-viewer");
const worker = perspective.worker();
const table = worker.table(stockData);
elem.load(table);
    </pre>
    <footer>
        &copy; 2024 J.P. Morgan Virtual Experience - Task 2
    </footer>
</div>

</body>
</html>

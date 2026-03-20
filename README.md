<html>
<head>
    <title>Calculator</title>
    <link rel="stylesheet" href="../css folder/Practical17.css">

    <style>
        body {
            text-align: center;
            background-color: #1e1e2f;
            color: white;
            font-family: Arial;
        }

        .calculator {
            margin-top: 30px;
            display: inline-block;
            background: #2c2c3c;
            padding: 20px;
            border-radius: 10px;
        }

        input {
            width: 200px;
            height: 40px;
            font-size: 20px;
            text-align: right;
            margin-bottom: 10px;
        }

        button {
            width: 45px;
            height: 45px;
            margin: 5px;
            font-size: 18px;
            cursor: pointer;
        }
    </style>
</head>

<body>

<center><h3>Santanu Das</h3></center>

<!-- Header -->
<div class="header">
    <h1>Calculator</h1>
</div>

<!-- Main Calculator -->
<div class="calculator">

    <input type="text" id="display" disabled><br>

    <button onclick="append('7')">7</button>
    <button onclick="append('8')">8</button>
    <button onclick="append('9')">9</button>
    <button onclick="append('/')">/</button><br>

    <button onclick="append('4')">4</button>
    <button onclick="append('5')">5</button>
    <button onclick="append('6')">6</button>
    <button onclick="append('*')">*</button><br>

    <button onclick="append('1')">1</button>
    <button onclick="append('2')">2</button>
    <button onclick="append('3')">3</button>
    <button onclick="append('-')">-</button><br>

    <button onclick="append('0')">0</button>
    <button onclick="append('.')">.</button>
    <button onclick="calculate()">=</button>
    <button onclick="append('+')">+</button><br>

    <button onclick="clearDisplay()">C</button>

</div>

<!-- Footer -->
<div class="footer">
    <p>Contact: santanudas5567@gmail.com</p>
    <p>&copy; santanu</p>
</div>

<script>
    let display = document.getElementById("display");

    function append(value) {
        display.value += value;
    }

    function clearDisplay() {
        display.value = "";
    }

    function calculate() {
        try {
            display.value = eval(display.value);
        } catch {
            display.value = "Error";
        }
    }
</script>

</body>
</html>

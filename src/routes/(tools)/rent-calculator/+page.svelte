<head>
	<title>Rent Calculator</title>
	<link rel="stylesheet" href="style.css" />
	<style type="text/css">
		body {
			background-color: #f3f3f3;
			font-family: Arial, sans-serif;
		}

		#about {
			text-align: center;
			font-size: 16px;
			margin: 20px;
		}

		.container {
			background-color: #fff;
			border-radius: 10px;
			box-shadow: 0px 0px 10px 1px #7b7272;
			padding: 20px;
		}

		.heading {
			text-align: center;
			font-size: 24px;
			font-weight: bold;
			color: #333;
		}

		.input-container {
			display: flex;
			justify-content: space-between;
			align-items: center;
			margin: 10px 0;
		}

		.input-container label {
			font-size: 18px;
			color: #333;
			font-weight: bold;
		}

		.input-container input {
			font-size: 18px;
			border: none;
			box-shadow: 0px 0px 2px 1px #989191;
			padding: 8px 12px;
			border-radius: 5px;
			font-family: 'Cambria', 'Cochin', 'Georgia', 'Times', 'Times New Roman', serif;
			outline: none;
			width: 50%;
		}

		.input-container input:hover {
			box-shadow: 0px 0px 2px 1px #252222;
		}

		.submit-container {
			display: flex;
			justify-content: center;
		}

		#calculate {
			padding: 8px 16px;
			font-size: 18px;
			background-color: #b63535;
			border-radius: 3px;
			color: #fff;
			border: none;
			outline: none;
			box-shadow: 2px 3px 4px #373434;
			transition: 0.4s;
			cursor: pointer;
		}

		#calculate:active {
			box-shadow: none;
			font-size: 18px;
		}

		.output {
			margin: 20px 0;
		}

		.output p {
			font-size: 18px;
			border-radius: 4px;
			padding: 8px;
			margin: 8px 0;
			box-shadow: 0px 0px 5px #33302e;
			color: #3e3a3a;
			font-weight: bold;
			display: flex;
			justify-content: space-between;
		}

		.output p span {
			color: #651129;
			font-size: 18px;
		}
		#rentCalculator2 {
			background-color: #fff;
			border-radius: 10px;
			box-shadow: 0px 0px 10px 1px #7b7272;
			padding: 20px;
			margin-top: 20px;
		}

		#rentCalculator2 h2 {
			text-align: center;
			font-size: 24px;
			font-weight: bold;
			color: #333;
		}

		#rentCalculator2 .input-container {
			display: flex;
			justify-content: space-between;
			align-items: center;
			margin: 10px 0;
		}

		#rentCalculator2 .input-container label {
			font-size: 18px;
			color: #333;
			font-weight: bold;
		}

		#rentCalculator2 .input-container input {
			font-size: 18px;
			border: none;
			box-shadow: 0px 0px 2px 1px #989191;
			padding: 8px 12px;
			border-radius: 5px;
			font-family: 'Cambria', 'Cochin', 'Georgia', 'Times', 'Times New Roman', serif;
			outline: none;
			width: 50%;
		}

		#rentCalculator2 .input-container input:hover {
			box-shadow: 0px 0px 2px 1px #252222;
		}

		#rentCalculator2 .submit-container {
			display: flex;
			justify-content: center;
		}

		#calculate2 {
			padding: 8px 16px;
			font-size: 18px;
			background-color: #b63535;
			border-radius: 3px;
			color: #fff;
			border: none;
			outline: none;
			box-shadow: 2px 3px 4px #373434;
			transition: 0.4s;
			cursor: pointer;
		}

		#calculate2:active {
			box-shadow: none;
			font-size: 18px;
		}

		#rentCalculator2 .output {
			margin: 20px 0;
		}

		#rentCalculator2 .output p {
			font-size: 18px;
			border-radius: 4px;
			padding: 8px;
			margin: 8px 0;
			box-shadow: 0px 0px 5px #33302e;
			color: #3e3a3a;
			font-weight: bold;
			display: flex;
			justify-content: space-between;
		}

		#rentCalculator2 .output p span {
			color: #651129;
			font-size: 18px;
		}
	</style>
</head>
<body>
    <center>
        <div id="rentCalculator2">
            <h2>Rent Calculator For Many Persons</h2>
            <p>
                Calculate your yearly rent expense based on the number of months and persons (Max 12 months)
            </p>
            <div class="input-container">
                <label for="rentAmount">Monthly Rent Amount</label>
                <input type="number" id="rentAmount" min="0" step="0.01" />
            </div>
            <div class="input-container">
                <label for="numberOfMonths">Number of Months (Max 12)</label>
                <input type="number" id="numberOfMonths" min="1" max="12" />
            </div>
            <div class="input-container">
                <label for="numberOfPersons">Number of Persons (Min 1)</label>
                <input type="number" id="numberOfPersons" min="1" />
            </div>
            <div class="submit-container">
                <button type="button" id="calculate2" onclick="calculateRent2()">Calculate Rent</button>
            </div>
            <div class="output">
                <p>
                    Total Rent for <span id="monthsResult">1</span> Months and
                    <span id="personsResult">1</span> Person:
                </p>
                <p>₹<span id="result">0</span></p>
            </div>
        </div>
        <div id="about">
            A rent calculator is a tool that helps you estimate how much rent you can afford to pay based
            on your income and expenses. It is useful for renters to plan their budget and find suitable
            housing options. To use a calculator, enter your monthly income, expenses, and desired
            savings. The calculator will show you how much rent you can afford and how much you will have
            left after paying rent.
        </div>
        <div id="box">
            <div class="container">
                <p class="heading">Rent Calculator</p>
                <div class="input-container">
                    <label for="income">Monthly Income(₹)</label>
                    <input type="number" id="income" min="0" step="0.01" required />
                </div>
                <div class="input-container">
                    <label for="expenses">Monthly Expenses(₹)</label>
                    <input type="number" id="expenses" min="0" step="0.01" required />
                </div>
                <div class="input-container">
                    <label for="savings">Desired Savings(₹)</label>
                    <input type="number" id="savings" min="0" step="0.01" required />
                </div>
                <div class="submit-container">
                    <button type="button" id="calculate" onclick="calculateRent()">Calculate Rent</button>
                </div>
                <div class="output">
                    <p>Affordable Rent Per Month (₹) <span id="rent">0.00</span></p>
                    <p>Remaining Income (₹) <span id="remaining">0.00</span></p>
                </div>
            </div>
        </div>
    </center>

    <script>
        function calculateRent() {
            const income = parseFloat(document.getElementById('income').value);
            const expenses = parseFloat(document.getElementById('expenses').value);
            const savings = parseFloat(document.getElementById('savings').value);

            // Calculate the affordable rent as 30% of the income minus expenses and savings
            const rent = 0.3 * (income - expenses - savings);

            // Calculate the remaining income after paying rent
            const remaining = income - expenses - savings - rent;

            // Update the content of the spans with the results
            document.getElementById('rent').textContent = '₹' + rent.toFixed(2);
            document.getElementById('remaining').textContent = '₹' + remaining.toFixed(2);
        }
        function calculateRent2() {
            const rentAmount = parseFloat(document.getElementById('rentAmount').value);
            const numberOfMonths = parseInt(document.getElementById('numberOfMonths').value);
            const numberOfPersons = parseInt(document.getElementById('numberOfPersons').value);

            if (rentAmount < 0 || numberOfMonths < 1 || numberOfPersons < 1) {
                alert('Please enter valid positive values.');
                return;
            }

            // Calculate the total rent
            const result2 = rentAmount * numberOfMonths * numberOfPersons;

            // Update the content of the spans with the results
            document.getElementById('monthsResult').textContent = numberOfMonths;
            document.getElementById('personsResult').textContent = numberOfPersons;
            document.getElementById('result').textContent = result2.toFixed(2);
        }

        function validatePersons2() {
            const numberOfPersons = parseInt(document.getElementById('numberOfPersons').value);
            if (numberOfPersons < 1) {
                document.getElementById('numberOfPersons').value = 1; // Ensure a minimum of 1 person
            }
        }

        function validateMonths2() {
            const numberOfMonths = parseInt(document.getElementById('numberOfMonths').value);
            if (numberOfMonths < 1) {
                document.getElementById('numberOfMonths').value = 1; // Ensure a minimum of 1 month
            } else if (numberOfMonths > 12) {
                document.getElementById('numberOfMonths').value = 12; // Limit to a maximum of 12 months
            }
        }
    </script>
</body>

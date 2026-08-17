<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Chicken Business System</title>

<style>
* {
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 15px;
    background: #f2f2f2;
}

.container {
    max-width: 750px;
    margin: auto;
    background: white;
    padding: 20px;
    border-radius: 12px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.15);
}

h1 {
    text-align: center;
}

h2 {
    margin-top: 25px;
    border-bottom: 2px solid #ddd;
    padding-bottom: 8px;
}

input, select, button {
    width: 100%;
    padding: 12px;
    margin: 6px 0;
    font-size: 16px;
    border-radius: 6px;
    border: 1px solid #ccc;
}

button {
    background: #333;
    color: white;
    border: none;
}

.add {
    background: #1976d2;
}

.sell {
    background: #2e7d32;
}

.expense {
    background: #ef6c00;
}

.delete {
    background: #c62828;
    padding: 6px;
    font-size: 12px;
}

.clear {
    background: #b71c1c;
}

.cards {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
    margin-top: 15px;
}

.card {
    padding: 15px;
    text-align: center;
    border-radius: 8px;
    background: #eee;
}

.card h3 {
    margin: 5px;
}

.card p {
    font-size: 20px;
    font-weight: bold;
    margin: 5px;
}

.profit {
    background: #e8f5e9;
}

.stock {
    background: #fff3cd;
}

table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 15px;
    font-size: 13px;
}

th, td {
    border: 1px solid #ccc;
    padding: 7px;
    text-align: center;
}

th {
    background: #eee;
}

@media (max-width: 600px) {
    table {
        font-size: 11px;
    }

    th, td {
        padding: 5px;
    }
}
</style>
</head>

<body>

<div class="container">

<h1>🐔 Chicken Business System</h1>


<!-- STOCK -->

<h2>🐣 Add Chicken Stock</h2>

<input
    type="text"
    id="chickenType"
    placeholder="Chicken type e.g. Broiler, Layer, Kenbro">

<input
    type="number"
    id="buyPrice"
    placeholder="Buying price per chicken (KSh)"
    min="0">

<input
    type="number"
    id="sellPrice"
    placeholder="Selling price per chicken (KSh)"
    min="0">

<input
    type="number"
    id="chickenQuantity"
    placeholder="Number of chickens"
    min="1">

<button class="add" onclick="addStock()">
    Add Chicken Stock
</button>


<table>

<thead>
<tr>
<th>Type</th>
<th>Buy</th>
<th>Sell</th>
<th>Stock</th>
<th>Action</th>
</tr>
</thead>

<tbody id="stockTable"></tbody>

</table>


<!-- SALES -->

<h2>💰 Sell Chickens</h2>

<select id="saleChicken" onchange="showChickenDetails()">
<option value="">Select chicken</option>
</select>

<input
    type="number"
    id="saleQuantity"
    placeholder="Number sold"
    min="1">

<div class="card stock">
Stock available:
<strong>
<span id="available">0</span>
</strong>
</div>

<button class="sell" onclick="sellChicken()">
    Record Chicken Sale
</button>


<!-- EXPENSES -->

<h2>💸 Business Expenses</h2>

<input
    type="text"
    id="expenseName"
    placeholder="Expense name e.g. Feed, Medicine, Transport">

<input
    type="number"
    id="expenseAmount"
    placeholder="Amount (KSh)"
    min="0">

<button class="expense" onclick="addExpense()">
    Add Expense
</button>


<!-- SUMMARY -->

<h2>📊 Business Summary</h2>

<div class="cards">

<div class="card stock">
<h3>🐔 Chickens</h3>
<p id="totalChickens">0</p>
</div>

<div class="card">
<h3>💰 Sales</h3>
<p>KSh <span id="totalSales">0</span></p>
</div>

<div class="card">
<h3>💸 Expenses</h3>
<p>KSh <span id="totalExpenses">0</span></p>
</div>

<div class="card profit">
<h3>📈 Profit</h3>
<p>KSh <span id="totalProfit">0</span></p>
</div>

</div>


<!-- SALES RECORD -->

<h2>🧾 Chicken Sales</h2>

<table>

<thead>
<tr>
<th>Type</th>
<th>Qty</th>
<th>Sales</th>
<th>Profit</th>
<th>Action</th>
</tr>
</thead>

<tbody id="salesTable"></tbody>

</table>


<!-- EXPENSE RECORD -->

<h2>💸 Expenses</h2>

<table>

<thead>
<tr>
<th>Expense</th>
<th>Amount</th>
<th>Action</th>
</tr>
</thead>

<tbody id="expenseTable"></tbody>

</table>


<button class="clear" onclick="clearAll()">
Clear All Business Records
</button>

</div>


<script>

let chickens =
JSON.parse(localStorage.getItem("chickens")) || [];

let sales =
JSON.parse(localStorage.getItem("chickenSales")) || [];

let expenses =
JSON.parse(localStorage.getItem("chickenExpenses")) || [];


/* SAVE */

function saveData() {

localStorage.setItem(
"chickens",
JSON.stringify(chickens)
);

localStorage.setItem(
"chickenSales",
JSON.stringify(sales)
);

localStorage.setItem(
"chickenExpenses",
JSON.stringify(expenses)
);

}


/* ADD STOCK */

function addStock() {

let type =
document.getElementById("chickenType").value.trim();

let buy =
Number(document.getElementById("buyPrice").value);

let sell =
Number(document.getElementById("sellPrice").value);

let quantity =
Number(document.getElementById("chickenQuantity").value);


if (
type === "" ||
buy <= 0 ||
sell <= 0 ||
quantity <= 0
) {

alert("Please enter all chicken details.");

return;

}


let existing =
chickens.find(
c => c.type.toLowerCase() === type.toLowerCase()
);


if (existing) {

existing.buy = buy;
existing.sell = sell;
existing.stock += quantity;

} else {

chickens.push({

type: type,
buy: buy,
sell: sell,
stock: quantity

});

}


saveData();

document.getElementById("chickenType").value = "";
document.getElementById("buyPrice").value = "";
document.getElementById("sellPrice").value = "";
document.getElementById("chickenQuantity").value = "";

displayAll();

alert("Chicken stock added successfully!");

}


/* DISPLAY STOCK */

function displayStock() {

let table =
document.getElementById("stockTable");

table.innerHTML = "";

chickens.forEach((chicken,index) => {

table.innerHTML += `

<tr>

<td>${chicken.type}</td>

<td>KSh ${chicken.buy}</td>

<td>KSh ${chicken.sell}</td>

<td>${chicken.stock}</td>

<td>

<button
class="delete"
onclick="deleteChicken(${index})">

Delete

</button>

</td>

</tr>

`;

});


let total = 0;

chickens.forEach(c => {

total += c.stock;

});

document.getElementById(
"totalChickens"
).textContent = total;

}


/* DELETE CHICKEN TYPE */

function deleteChicken(index) {

if (
confirm(
"Delete this chicken stock?"
)
) {

chickens.splice(index,1);

saveData();

displayAll();

}

}


/* SELECT CHICKEN */

function updateChickenSelect() {

let select =
document.getElementById("saleChicken");

select.innerHTML =
'<option value="">Select chicken</option>';


chickens.forEach((chicken,index) => {

select.innerHTML += `

<option value="${index}">

${chicken.type}
- KSh ${chicken.sell}
(${chicken.stock} available)

</option>

`;

});

showChickenDetails();

}


/* SHOW STOCK */

function showChickenDetails() {

let index =
document.getElementById("saleChicken").value;

if(index === "") {

document.getElementById(
"available"
).textContent = 0;

return;

}

document.getElementById(
"available"
).textContent =
chickens[index].stock;

}


/* SELL CHICKEN */

function sellChicken() {

let index =
document.getElementById("saleChicken").value;

let quantity =
Number(
document.getElementById("saleQuantity").value
);


if(index === "") {

alert("Select chicken type.");

return;

}


if(quantity <= 0) {

alert("Enter quantity sold.");

return;

}


let chicken =
chickens[index];


if(quantity > chicken.stock) {

alert(
"Not enough chickens in stock.\n\n" +
"Available: " +
chicken.stock
);

return;

}


chicken.stock -= quantity;


let salesAmount =
chicken.sell * quantity;

let cost =
chicken.buy * quantity;

let profit =
salesAmount - cost;


sales.push({

type: chicken.type,

buy: chicken.buy,

sell: chicken.sell,

quantity: quantity,

sales: salesAmount,

profit: profit

});


saveData();

document.getElementById(
"saleQuantity"
).value = "";

displayAll();

alert("Chicken sale recorded!");

}


/* ADD EXPENSE */

function addExpense() {

let name =
document.getElementById("expenseName").value.trim();

let amount =
Number(
document.getElementById("expenseAmount").value
);


if(name === "" || amount <= 0) {

alert("Enter expense name and amount.");

return;

}


expenses.push({

name: name,

amount: amount

});


saveData();


document.getElementById(
"expenseName"
).value = "";

document.getElementById(
"expenseAmount"
).value = "";


displayAll();

}


/* DISPLAY SALES */

function displaySales() {

let table =
document.getElementById("salesTable");

table.innerHTML = "";


sales.forEach((sale,index) => {

table.innerHTML += `

<tr>

<td>${sale.type}</td>

<td>${sale.quantity}</td>

<td>KSh ${sale.sales}</td>

<td>KSh ${sale.profit}</td>

<td>

<button
class="delete"
onclick="deleteSale(${index})">

Delete

</button>

</td>

</tr>

`;

});

}


/* DELETE SALE */

function deleteSale(index) {

let sale = sales[index];


if(
confirm(
"Delete this sale and return chickens to stock?"
)
) {

let chicken =
chickens.find(
c => c.type === sale.type
);


if(chicken) {

chicken.stock += sale.quantity;

}


sales.splice(index,1);

saveData();

displayAll();

}

}


/* DISPLAY EXPENSES */

function displayExpenses() {

let table =
document.getElementById("expenseTable");

table.innerHTML = "";


expenses.forEach((expense,index) => {

table.innerHTML += `

<tr>

<td>${expense.name}</td>

<td>KSh ${expense.amount}</td>

<td>

<button
class="delete"
onclick="deleteExpense(${index})">

Delete

</button>

</td>

</tr>

`;

});

}


/* DELETE EXPENSE */

function deleteExpense(index) {

if(
confirm("Delete this expense?")
) {

expenses.splice(index,1);

saveData();

displayAll();

}

}


/* SUMMARY */

function calculateSummary() {

let totalSales = 0;

let chickenProfit = 0;

let totalExpenses = 0;


sales.forEach(sale => {

totalSales += sale.sales;

chickenProfit += sale.profit;

});


expenses.forEach(expense => {

totalExpenses += expense.amount;

});


let finalProfit =
chickenProfit - totalExpenses;


document.getElementById(
"totalSales"
).textContent = totalSales;


document.getElementById(
"totalExpenses"
).textContent = totalExpenses;


document.getElementById(
"totalProfit"
).textContent = finalProfit;

}


/* CLEAR EVERYTHING */

function clearAll() {

if(
confirm(
"WARNING!\n\n" +
"This will delete all chickens, sales and expenses.\n\n" +
"Continue?"
)
) {

chickens = [];
sales = [];
expenses = [];

localStorage.removeItem("chickens");
localStorage.removeItem("chickenSales");
localStorage.removeItem("chickenExpenses");

displayAll();

}

}


/* DISPLAY EVERYTHING */

function displayAll() {

displayStock();

updateChickenSelect();

displaySales();

displayExpenses();

calculateSummary();

}


displayAll();

</script>

</body>
</html>

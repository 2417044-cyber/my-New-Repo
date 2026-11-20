**// 1.Cal operations**



/\*

<html>

<head>

&#x20;   <title>Simple Calculator</title>

&#x20;   <link rel="stylesheet" href="style.css">

</head>

<body>



<h2>Simple Calculator</h2>



<input type="number" id="num1" placeholder="Enter First Number"><br><br>



<input type="number" id="num2" placeholder="Enter Second Number"><br><br>



<button onclick="add()">Addition (+)</button>

<button onclick="sub()">Subtraction (-)</button><br><br>



<button onclick="mul()">Multiplication (\*)</button>

<button onclick="div()">Division (/)</button>



<h3 id="result">Result:</h3>



<script src="script.js"></script>



</body>

</html>





//css

body {

&#x20;   text-align: center;

&#x20;   background-color: lightblue;

&#x20;   font-family: Arial;

}



input {

&#x20;   padding: 8px;

}



button {

&#x20;   padding: 8px;

&#x20;   margin: 5px;

&#x20;   background-color: green;

&#x20;   color: white;

}



//Js



function add() {

&#x20;   var a = Number(document.getElementById("num1").value);

&#x20;   var b = Number(document.getElementById("num2").value);



&#x20;   document.getElementById("result").innerHTML = "Result: " + (a + b);

}



function sub() {

&#x20;   var a = Number(document.getElementById("num1").value);

&#x20;   var b = Number(document.getElementById("num2").value);



&#x20;   document.getElementById("result").innerHTML = "Result: " + (a - b);

}



function mul() {

&#x20;   var a = Number(document.getElementById("num1").value);

&#x20;   var b = Number(document.getElementById("num2").value);



&#x20;   document.getElementById("result").innerHTML = "Result: " + (a \* b);

}



function div() {

&#x20;   var a = Number(document.getElementById("num1").value);

&#x20;   var b = Number(document.getElementById("num2").value);



&#x20;   if (b == 0) {

&#x20;       alert("Cannot divide by zero");

&#x20;   }

&#x20;   else {

&#x20;       document.getElementById("result").innerHTML = "Result: " + (a / b);

&#x20;   }

}





**// 2.To-do task**



<html>

<head>

&#x20;   <title>To Do List</title>

&#x20;   <link rel="stylesheet" href="style.css">

</head>

<body>



<h2>My To Do List</h2>



<input type="text" id="task" placeholder="Enter Task">



<button onclick="addTask()">Add</button>



<ul id="list"></ul>



<script src="script.js"></script>



</body>

</html>



// css

body {

&#x20;   text-align: center;

&#x20;   background-color: lightblue;

&#x20;   font-family: Arial;

}



input {

&#x20;   padding: 8px;

}



button {

&#x20;   padding: 8px;

&#x20;   background-color: green;

&#x20;   color: white;

}



li {

&#x20;   margin: 10px;

}



//js



function addTask() {



&#x20;   var task = document.getElementById("task").value;



&#x20;   if (task == "") {

&#x20;       alert("Enter a task");

&#x20;   }

&#x20;   else {

&#x20;       var li = document.createElement("li");



&#x20;       li.innerHTML = task + 

&#x20;       " <button onclick='completeTask(this)'>Complete</button>" +

&#x20;       " <button onclick='deleteTask(this)'>Delete</button>";



&#x20;       document.getElementById("list").appendChild(li);



&#x20;       document.getElementById("task").value = "";

&#x20;   }

}



function completeTask(btn) {

&#x20;   btn.parentElement.style.textDecoration = "line-through";

}



function deleteTask(btn) {

&#x20;   btn.parentElement.remove();

}


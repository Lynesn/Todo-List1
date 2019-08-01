<!DOCTYPE html>
<html>
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1">
<style>
  
  
* {
  box-sizing: border-box;
}
/*Remove margins/padding*/
ul {
  margin: 0;
  padding: 0;
}
body {
  font-family:
 -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans,
  Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;
  width: 30%;
  position: relative;
  
}
/* List Items */
ul li {
  cursor: pointer;
  position: relative;
  padding: 12px 20px 12px 40px;
  list-style-type: none;
  background: skyblue;
  font-size: 20px;
  transition: 0.5s;
  margin: 5px 0px;
  
  /* make them unselectable */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
#myInput{
  color: black;
}
/* Set items to a different color (light blue) */
ul li:nth-child(odd) {
  background: skyblue;
}

/* Add a "checked" mark when clicked on */
ul li.checked::before {
  content: '';
  position:absolute;
  border-style: solid;
  border-width: 0 2px 2px 0;
  top: 10px;
  left: 16px;
  transform: rotate(45deg);
  height: 15px;
  width: 7px;
}
/* Style the close button */
.close {
  position: absolute;
  right: 0;
  top: 0;
  padding: 12px 16px 12px 16px;
}

.close:hover {
  background-color: #f44336;
  color: red;
  
}
/* Style the header */
.header {
  padding: 20px 0px;
  color: black;
  text-align: left;
  width: 70%;
  }

/* Clear floats */
.header:after {
  content: "";
  display: table;
  clear: both;
}

/* input */
input {
  margin: 0;
  border: none;
  border-radius: 0;
  width: 80%;
  padding: 10px;
  float: left;
  font-size: 16px;
  background-color: skyblue;
  color: black;
}


.addBtn {
  padding: 8.5px;
  width: 20%;
  background: #d9d9d9;
  color: #555;
  float: left;
  text-align: center;
  font-size: 16px;
  cursor: pointer;
  transition: 0.3s;
  border-radius: 0;
}

.addBtn:hover {
  background-color: #bbb;
}
</style>
</head>
<body>
  <div id="myDIV" class="header">
    <h2 style="margin:5px">ToDo App</h2>
    <input type="text" id="myInput" placeholder="Enter To Do...">
    <span onclick="newElement()" class="addBtn">Add</span>
  </div>

<ul id="myUL">
  <li>Exercise</li>
  <li class="checked">Reading</li>
  <li>Meet Cosy</li>
  <li>Shopping</li>
  <li>University</li>
  <li>House Work</li>
</ul>
<script>
  // Adding a close button to items
var myNodelist = document.getElementsByTagName("LI");
var i;
for (i = 0; i < myNodelist.length; i++) {
  var span = document.createElement("SPAN");
  var txt = document.createTextNode("\u00D7");
  span.className = "close";
  span.appendChild(txt);
  myNodelist[i].appendChild(span);
}
// To delet items.
var close = document.getElementsByClassName("close");
var i;
for (i = 0; i < close.length; i++) {
  close[i].onclick = function() {
    var div = this.parentElement;
    div.style.display = "none";
  }
}


// check when clicked.
var list = document.querySelector('ul');
list.addEventListener('click', function(ev) {
  if (ev.target.tagName === 'LI') {
    ev.target.classList.toggle('checked');
  }
}, false);

// Click Add to create
function newElement() {
  var li = document.createElement("li");
  var inputValue = document.getElementById("myInput").value;
  console.log(inputValue);
  var t = document.createTextNode(inputValue);
  li.appendChild(t);
  if (inputValue === '') {
    alert("You must write something!");
  } else {
    document.getElementById("myUL").appendChild(li);
  }
  document.getElementById("myInput").value = "";

  var span = document.createElement("SPAN");
  var txt = document.createTextNode("\u00D7");
  span.className = "close";
  span.appendChild(txt);
  li.appendChild(span);

  for (i = 0; i < close.length; i++) {
    close[i].onclick = function() {
      var div = this.parentElement;
      div.style.display = "none";
    }
  }
}
</script>  
</body>
</html>

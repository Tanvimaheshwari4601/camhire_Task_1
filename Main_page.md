<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MAIN PAGE</title>
    
</head>
<head>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

<style>
  .w3-button {width:230px;
  height: 50px;
border: black;}
* {box-sizing: border-box;}

body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}

.topnav {
  overflow: hidden;
  background-color: #e9e9e9;
}

.topnav a {
  float: left;
  display: block;
  color: black;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

.topnav a:hover {
  background-color: #ddd;
  color: black;
}

.topnav a.active {
  background-color: #2196F3;
  color: white;
}

.topnav .search-container {
 
  float: right;
}

.topnav input[type=text] {
  padding: 6px;
  margin-top: 8px;
  font-size: 17px;
  border: none;
}

.topnav .search-container button {
  background-color: #2196F3;
  float: right;
  padding: 6px 10px;
  margin-top: 8px;
  margin-right: 16px;
  background: #ddd;
  font-size: 17px;
  border: none;
  cursor: pointer;
}

}

.btn {
  background-color: DodgerBlue; /* Blue background */
  border: none; /* Remove borders */
  color: white; /* White text */
  padding: 35px 50px; /* Some padding */
  font-size: 50px; /* Set a font size */
  cursor: pointer; /* Mouse pointer on hover */
}

/* Darker background on mouse-over */
.btn:hover {
  background-color: RoyalBlue;
}





.show {display: block;}
#myTable {
  border-collapse: collapse; /* Collapse borders */
  width: 100%; /* Full-width */
  border: 1px solid rgb(247, 243, 243); /* Add a grey border */
  font-size: 25px; /* Increase font-size */
}

#myTable th, #myTable td {
  text-align: left; /* Left-align text */
  padding: 12px; /* Add padding */
}
.row_style {
display: flex;
flex-direction: row row-reverse;
}

#myTable tr {
  /* Add a bottom border to all table rows */
  border-bottom: 1px solid #ddd;
}

#myTable tr.header, #myTable tr:hover {
  /* Add a grey background color to the table header and on hover */
  background-color: #ac6e6e;
}
}
.topnav .search-container button:hover {
  background: #ccc;
}

@media screen and (max-width: 600px) {
  .topnav .search-container {
    float: none;
  }
  .topnav a, .topnav input[type=text], .topnav .search-container button {
    float: none;
    display: block;
    text-align: left;
    width: 100%;
    margin: 0;
    padding: 14px;
  }
  
  .topnav input[type=text] {
    border: 1px solid #ccc;  
  }
}
</style>
</head>
<body>

<div class="topnav">
  
 <a class='active' href="#home">Home</a>
 <a  href="#About">About</a>
 <a  href="#contact">Contact</a>
  <div>
    
  </div>
  
  <div class="search-container">
    <div class="row_style" >
    <form action="/action_page.php">
      <input type="text" id="myInput" onkeyup="myFunction()" placeholder="Search by Category...">
     
    </form>
    <button onclick="sortTable()" >sort by charges</button>
      <button onclick="logout()" type="submit">Log out </button> 
  
    
  </div>
    <ol id='list'>
    </ol>
  </div>
  
  </div>
</div>

<div>
  <table id="myTable">
    <tr class="header">
      <th style="width:20px;">ID</th>
      <th style="width:250px;">Name of Photographer</th>
      <th style="width:200px;">Category</th>
      <th style="width:200px;">Location</th>
      <th style="width:100px;">Charges per day</th>
    </tr>
    <tr>
      <td>110</td>
      <td>Mr. Smith johnson</td>
      <td>Wedding Photographer</td>
      <td>123 Street no. 25,udaipur</td>
      <td> 5000</td>
        </tr>
    <tr>
      <td>125</td>
      <td>Mr. kevin day</td>
      <td>Wildlife Photographer</td>
      <td>450 abc nagar 25,udaipur</td>
      <td>3500</td>
    </tr>
    <tr>
      <td>565</td>
      <td>Mr. Camera king</td>
      <td>Fashion Photographer</td>
      <td>sector-4 ,udaipur</td>
      <td> 4000</td>
    </tr>
    <tr>
      <td>455</td>
      <td>Mr. Crimson son</td>
      <td>Travel Photographer</td>
      <td>xyz near abc temple,udaipur</td>
      <td> 7000</td>
    </tr>
    <tr>
      <td>289</td>
      <td>Mr. Christian </td>
      <td>Portrait Photographer</td>
      <td>chain street,udaipur</td>
      <td> 5500</td>
    </tr>
    <tr>
      <td>355</td>
      <td>Mr. Sem </td>
      <td>Travel Photographer</td>
      <td>industrial area,udaipur</td>
      <td> 8000</td>
    </tr>
    <tr>
      <td>485</td>
      <td>Mr. Giovanni</td>
      <td>Wedding Photographer</td>
      <td>near street,udaipur</td>
      <td> 6000</td>
    </tr>
    <tr>
      <td>115</td>
      <td>Mr. peter Gray</td>
      <td>Wildlife Photographer</td>
      <td>12345 colony,udaipur</td>
      <td> 4700</td>
    </tr>

  </table>
  <script>
    function myFunction() {
      var input, filter, table, tr, td, i, txtValue;
      input = document.getElementById("myInput");
      filter = input.value.toUpperCase();
      table = document.getElementById("myTable");
      tr = table.getElementsByTagName("tr");
      for (i = 0; i < tr.length; i++) {
        td = tr[i].getElementsByTagName("td")[2];
        if (td) {
          txtValue = td.textContent || td.innerText;
          if (txtValue.toUpperCase().indexOf(filter) > -1) {
            tr[i].style.display = "";
          } else {
            tr[i].style.display = "none";
          }
        }       
      }
    }
    </script>
    <script>
      
      function logout()
      {    
        window.location = "box.html";
      }
        
    </script>
    
    <script>
      function sortTable() {
  var table, rows, switching, i, x, y, shouldSwitch;
  table = document.getElementById("myTable");
  switching = true;
  while (switching) {
    switching = false;
    rows = table.rows;
    for (i = 1; i < (rows.length - 1); i++) {
      shouldSwitch = false;
      x = rows[i].getElementsByTagName("TD")[4];
      y = rows[i + 1].getElementsByTagName("TD")[4];
      if (Number(x.innerHTML) > Number(y.innerHTML)) {
        shouldSwitch = true;
        break;
      }
    }
    if (shouldSwitch) {
    
      rows[i].parentNode.insertBefore(rows[i + 1], rows[i]);
      switching = true;
    }
  }
}

    </script>
    
    <script>
      function logout(){
    wwindow.location.href = "box.html";
}
    </script>
    <script>
      (function() {
        const idleDurationSecs = 10;
        const redirectUrl = 'box.html';
        let idleTimeout;
    
        const resetIdleTimeout = function() {
            if(idleTimeout) clearTimeout(idleTimeout);
            idleTimeout = setTimeout(() => location.href = redirectUrl, idleDurationSecs * 1000);
        };
      
        resetIdleTimeout();
        window.onmousemove = resetIdleTimeout;
        window.onkeypress = resetIdleTimeout;
        window.click = resetIdleTimeout;
        window.onclick = resetIdleTimeout;
        window.touchstart = resetIdleTimeout;
        window.onfocus = resetIdleTimeout;
        window.onchange = resetIdleTimeout;
        window.onmouseover = resetIdleTimeout;
        window.onmouseout = resetIdleTimeout;
        window.onmousemove = resetIdleTimeout;
        window.onmousedown = resetIdleTimeout;
        window.onmouseup = resetIdleTimeout;
        window.onkeypress = resetIdleTimeout;
        window.onkeydown = resetIdleTimeout;
        window.onkeyup = resetIdleTimeout;
        window.onsubmit = resetIdleTimeout;
        window.onreset = resetIdleTimeout;
        window.onselect = resetIdleTimeout;
        window.onscroll = resetIdleTimeout;
    
    })();
    </script>
</div>


</body>

</html>

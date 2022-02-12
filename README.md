# camhire_Task_1
# for main page
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
   
</head>
 <script>
   function create()
   {
        window.location.href = "create.html";
   }

  function login()
{
    var uname=document.getElementById("email").value;
    var upassword=document.getElementById("pwd1").value;
    var dialog = document.getElementById('first'); 
    var dial = document.getElementById('second'); 

    if (uname == "" || upassword == "") 
    {
    document.getElementById("errorMsg").innerHTML = "Please fill the required fields"
    
    }
    else if(uname=="admin" && upassword=="admin")
    {
       dialog.show(); 
       document.getElementById('hide').onclick = function() {    
        window.location = "search.html";
        dialog.close();    
        }; 
 
    }
    else
        dial.show();
        document.getElementById('hi').onclick = function() {    
        dial.close();  
        };
}    
  

function clearFunc()
    {
        document.getElementById("email").value="";
        document.getElementById("pwd1").value="";
    }   
</script>

<style>
    body
   {
     margin:0px; background-color:#4099c2; color:#f7f7f7; font-family:Arial, Helvetica, sans-serif;
   }
   #main
   {
     width:600px; height:260px; margin-left:auto; margin-right:auto; border-radius:5px; padding-left:10px; margin-top:100px;
     border-top:3px double #f1f1f1; border-bottom:3px double #f1f1f1; padding-top:20px;
   }
   #main table
   {
     font-family:"Comic Sans MS", cursive;
   } 
  /* css code for textbox */
  #main .tb
  {
    height:28px; width:230px; border:1px solid #4099c2; color:#4099c2; font-weight:bold; border-left:5px solid #f7f7f7; opacity:0.9;
  }

   /* css code for button*/
   #main .btn
   {
    width:80px; height:32px; outline:none;  font-weight:bold; border:0px solid #4099c2; text-shadow: 0px 0.5px 0.5px #fff;	
    border-radius: 2px; font-weight: 600; color: #4099c2; letter-spacing: 1px; font-size:14px; -webkit-transition: 1s; -moz-transition: 1s; transition: 1s;
   }
  
   #main .btn:hover
   {
    background-color:#4099c2; outline:none;  border-radius: 2px; color:#f1f1f1; border:1px solid #f1f1f1;
   }
   #main .button
   {
    width:200px; height:32px; outline:none;  font-weight:bold; border:0px solid #4099c2; text-shadow: 0px 0.5px 0.5px #fff;	
    border-radius: 2px; font-weight: 600; color: #4099c2; letter-spacing: 1px; font-size:14px; -webkit-transition: 1s; -moz-transition: 1s; transition: 1s;
   }
  
   #main .button:hover
   {
    background-color:#4099c2; outline:none;  border-radius: 2px; color:#f1f1f1; border:1px solid #f1f1f1;
   }
</style>
<body>
    <!-- Main div code -->
	<div id="main">
        <div class="h-tag">
        <h2>Login Details...</h2>
        </div>
        <!-- Login box -->
        <div class="login">
        <table cellspacing="2" align="center" cellpadding="8" border="0">
        <tr>
        <td>Enter User Name :</td>
        <td><input type="text" placeholder="Enter user name here" id="email" class="tb" /></td>
        </tr>
        <tr>
        <td>Enter Password :</td>
        <td><input type="password" placeholder="Enter Password here" id="pwd1" class="tb" /></td>
        </tr>
        <tr>
        <td></td>
        <td>
        <input type="submit" value="Reset" onclick="clearFunc()" class="btn" />
        <input type="submit" value="Login" class="btn" onClick="login()" /></td>
        <td></td>
        <td><input type="submit" class="button" value="Create an account" onclick="create()"></td>
        
        </table>
        </div>
           <!-- login box div ending here.. -->
        <dialog id="first">
          <p>Username and Password is correct</p>
          <button id="hide">Continue</button>  
        </dialog>   
        <dialog id="second">
          <p>Username and Password is incorrect</p>
          <button id="hi">close</button> 
        </dialog>
        </div>
        <!-- Main div ending here... -->
</body>

</html>

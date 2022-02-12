<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <style>
   body
   {
     margin:0px; background-color:#4099c2; color:#f7f7f7; font-family:Arial, Helvetica, sans-serif;
   }
  
   #main tablebody
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

  </style>
  <div class="h-tag" align="center">
    <h2>Personal Details...</h2>
    </div>
  <div id="main">
    <!-- Login box -->
    <div class="login">
    <table cellspacing="5" align="center" cellpadding="9" border="0">
      <tr>
        <td>First Name:</td>
        <td><input type="text" id="fname" placeholder="First name" name="fname" class="tb"></td>
      </tr>
      <tr>
        <td>Last Name:</td>
        <td><input type="text" id="lname" placeholder="Last name" name=lfname" class="tb"></td>
      </tr>
      <tr>
        <td>Phone Number:</td>
        <td><input type="tel" id="phone" name="phone" placeholder="+91-0123456789" pattern="+91-[0-9]{3}[0-9]{2}[0-9]{3}" required></td>
      </tr>
      <tr>
        <td>Last Name:</td>
        <td><input type="email" id="email" placeholder="abc@gmail.com" name="email" class="tb"></td>
      </tr>
      <tr>
        <td>Date of Birth:</td>
        <td><input type="date" id="birthday" name="birthday" class="tb" /></td>
    </tr>
      <tr>
        <td>Enter Password :</td>
        <td><input type="password" placeholder="Enter Password here" id="pwd1" class="tb" /></td>
        </tr>
      
      <tr>
            <td>City:</td>
            <td><input type="text" id="city" name="city" class="tb" /></td>
      </tr>
      <tr>
        <td>Address:</td>
        <td><textarea name="message" rows="2" cols="30"></textarea></td>
      </tr>
      <tr>
        <td>Login as</td>
        <td> <input list="browsers" name="browser" class="tb">
          <datalist id="browsers">
            <option value="Photographer">
            <option value="Client">
           
          </datalist></td>
      </tr>
      <td><input type="submit" value="submit" class="btn" onClick="submit()" /></td>
    </table>
  </div>

<script>
function submit()
{
  window.location = "search.html";
}
</script>
</body>
</html>

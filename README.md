# BMI_Calculator
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>Untitled Document</title>
<style>

body{
margin:0;
padding:0;
text-align:center;
font-family:Tahoma, Geneva, sans-serif;
background-image:linear-gradient(120deg,#F66,#09C);
min-height:100vh;
}

.status1{
width:500px;
position:absolute;
top:62%;
left:32%;
background-color:#FFF;
transform:translate(-50%,-50%);
padding:20px;
border-radius:10px;
box-shadow:1px 1px 20px #ee5253;
}

.status2{
	width:550px;
	position:absolute;
	top:33%;
	right:4%;

	padding:20px;
	height:55%;
	}
	

h2{
font-size:30px;
font-weight:600;
}

.tex{
text-align:left;
margin-left:150px;
}


.column{
	text-align:left;
	margin-left:100px;
	
	
}
#w{
	width:15%;
	padding-left:30px;
	position:absolute;
	bottom:52%;
	left:39%;
	}
.col{
	position:absolute;
	bottom:36%;
	left:34%;
	}
#feet{
	width:10%;
	position:absolute;
	bottom:36%;
	left:40%;
	}
.col1{
	position:absolute;
	bottom:36%;
	left:55%;
	}
#inches{
	width:10%;
	position:absolute;
	bottom:36%;
	left:64%;
	}
#cal{
	font-family:inherit;
	border:none;
	margin-top:10px;
	color:#FFF;
	background-image:linear-gradient(120deg,#F66,#09C);
	width:150px;
	border-radius:30px;
	padding:10px;
	outline:none;
	}
	
.cu{
	font-family:"Times New Roman", Times, serif;
	color:#FFF;
	width:100%;
	height:160px;
	position:absolute;
	top:0%;
	font-size:20px;
	border-collapse:collapse;
	
	
	
}
table,tr,td{
 border:1px solid pink;
 height;100px;
 padding:1px;
 

}
.tbl{
	background-color:#FFF;
  position:absolute;
  margin-bottom:5%;
}

</style>
</head>
<body>
<div class="cu">
<h2 >University of Computer Studies (Kyaing Tong)</h2>
<h3 >CS-2254 Web Development Programming </h3>
<h3 >UCSKT-18001(Ma Nang Kein Swan)</h3>

</div>
<div class="status1">
<h2>BMI Calculator</h2>
<p>Please enter your Weight and Height</p><br />

<p class="column" >Weight(lbs):</p>
<input type="text" id="w"  /><br />

<p class="column"  >Height:</p>
<span class="col" >feet</span>
<input type="text" id="feet"  />
<span class="col1" >inches</span>
<input type="text" id="inches" /><br />

<p >Your BMI is :<span id="res"></span></p>
<button id="cal" onclick="Bmi()" >Calculate</button>
</div>

<div class="status2">
<table class="tbl" >
<tr bgcolor="#F0FFFF">
<td>Underweigth:<br />0-18.5</td>
<td>A person insufficient weight, so they may need to put on some weight.They should asked a doctor or dietitian for advice.
</td>
</tr>
<tr bgcolor="#CCFFCC">
<td>Normalweight: 18.5 - 24.9</td>
<td>A person has a healthy weight for their height.By maintaining a healthy weight,they can lower their risk of developing serious health problems. </td>
</tr>
<tr bgcolor="#CCCCFF">
<td>Overweight:<br /> 25 - 29.9 </td>
<td>A person is sightly overweight. A doctor may advise them to lose some weight for health reasons. They should talk with a doctor or dietitian for advice.</td>
</tr>
<tr bgcolor="#FFFFCC">
<td>Obese: <br />30 - 35</td>
<td>A person has obesity.Their health may be at risk if they do not lose weight.They should talk with a doctor or dietitian for advice.</td>
</tr>
<tr bgcolor="#FFCCFF">
<td>Extremely:<br /> over 35 </td>
<td>Your blood pressure,blood sugar,cholesterol,and body fat may be at unhealthy levels.A doctor can help you manage it with changes in diet and exercise as well as medicine.</td>
</tr>
</table>
</div>



<script type="text/javascript">

function Bmi()
{
	var weight=parseInt(document.getElementById("w").value);
	var ft=parseInt(document.getElementById("feet").value*12);
	var inch=parseInt(document.getElementById("inches").value);
	
	var height=ft+inch;
	//alert(height);
	
	var bmi=weight/(height*height)*703;
    var finalbmi=String(bmi.toPrecision(3));
	
	
	if(finalbmi<18.5)
	{
	document.getElementById("res").innerHTML=finalbmi+"( underweight)";
	}
	else if (finalbmi<18.5 || finalbmi<24.9){
	
	document.getElementById("res").innerHTML=finalbmi+" (Normalweight)";
	
	
	}
	else if (finalbmi<25 || finalbmi<29.9){
	
	document.getElementById("res").innerHTML=finalbmi+" (Overweight)";
	
	
	}
	else if (finalbmi<30 || finalbmi<35){
		
	document.getElementById("res").innerHTML=finalbmi+" (Obese)";
	
	
	}	
	
	else if(finalbmi>35) {

		document.getElementById("res").innerHTML=finalbmi+" (Extremely)";
	}
	
	else{
		document.getElementById("res").innerHTML="Please Enter!";
	}

	
}


</script>

</body>
</html>

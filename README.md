<!DOCTYPE html>
<html lang="en">
<head>
  <title>Elite Health & Beauty</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
</head>
<body>
    <img src="logo.PNG" alt="Elite Health and Beaty Logo">
    <ul>
      <a href="index.php">Home</a> |
      <a href="prodcuts.php">Products</a> |
        <a href="stores.php">Stores</a> |
        <a href="cart.php">Shopping Cart</a> |
        <a href="about.php">About Us</a> |
      <a href="contact.php">Contacts</a><hr>
        <p>Welcome to the one stop place where you will access every type of medical and health supplements to improve your health.<br>
We have a wide range of products including beauty reams, ointments, lotions, powders, stimulants, and food supplements.<br>
Browse our extensive catalogue for your desired product and we will deliver it right into your door step.<br>
Our dedicated sales team will offer you all the help you need to purchase the right product

<div class="container-fluid">
     <div class="row">
    <div class="col-sm-4" style="background-color:lavender;">
	 <div class="col-sm-4" style="background-color:lavender;">.Employees Details<div>
	<?php
//Database Configuration
$dbhost = "localhost";
$dbuser = "root";
$dbpass = "";
$dbname = "elite_health_beauty";
//Dabase Connection
$conn= mysqli_connect($dbhost,$dbuser, $dbpass,$dbname);
if (!$conn) {
  die("Connection failed: " . mysqli_connect_error);
	}
Display Data
	$sql = "SELECT * customers";
$result = mysqli_querry($conn,$sql);

if ($mysqli_num_rows > 0) {
	<table style="color:blue">
	<tr>
	<th>First Name</th>
	<th>&nbsp Last Name</th>
	</tr>
	    while($row = mysqli_fetch_assoc($result)) {
        echo "<tr>"."<td>" "First Name:" .$row["First Name"]."</td>". "/tr>";
		echo "<tr>"."<td>" "Last Name:" .$row["Last Name"]."</td>". "/tr>";
    }
	} else {
    echo "No results";
	</table>
}
$conn->close();
</div>
  </div>
</div>
</body>
</html>



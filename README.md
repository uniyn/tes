<?php
$servername = "localhost";
$username = "root";
$password = "root";
$dbname = "test";

try
{
	$conn = new PDO("mysql:host=$servername;dbname=$dbname",$username,$password);
	$conn->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);

	echo "Koneksi Berhasil";
}
catch(PDOException $e)
{
	echo "Error :" . $e->getMessage();
}
$conn = null;
?>

This Connection Script is simple to use 
and easy to change. Its a Set details once and walk away from it.

It's been designed to work with the MYSQLI QUERY.

The only Code in the MYSQLI that you need to remember is have the Connection to the Database available.


<?php

$db['DB_HOST'] = "host"; //host will be server name or localhost
$db['DB_USER'] = "dbusername"; // dbusername will be the database user name
$db['DB_PASS'] = "dbpassword";  // dbpassword will be the database user password
$db['DB_NAME'] = "dbname";  // dbname will be the database name

foreach($db as $key => $value) {
define(strtoupper($key), $value);
}

//host, username, password, database
$connection = mysqli_connect(DB_HOST, DB_USER, DB_PASS, DB_NAME);
// If there is a connection error you will see a "Connection Error"
// and you will have to find the incorrect value and have to fix it.
if($connection) {
echo "Connected"; //You can remove the text between the quotation marks once the connection has been set
} else {
die("QUERY FAILED " . mysqli_error($connection));
}

?>

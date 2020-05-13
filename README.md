# flutter app to upload a photo to server
 a flutter app that wil take a photo from a camera or gallary and upload it to server php which will put the photo into folder

for a server i used xampp apache server and in the directry \xampp\htdocs\flutter i stored all the php file 
which contain the code with file name saveFile.php and a folder named upload to store the photo.

php code

#code 
#<?php
	$image = $_POST['image'];
	$name = $_POST['name'];
	
	$realImage = base64_decode($image);
	
	file_put_contents("upload/$name", $realImage);
	
	echo "File Uploaded.";
	
?>
#

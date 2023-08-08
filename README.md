# email-validity
//first way//
function IsEmail(email) {
   var regex = /^([a-zA-Z0-9_\.\-\+])+\@(([a-zA-Z0-9\-])+\.)+([a-zA-Z0-9]{2,4})+$/;
   if (!regex.test(email)) {
       return false;
   }
   else {
       return true;
   }
}

======throww message=========
if(IsEmail(email) == false){
       $('#email_e1').html(" Invalid Email Format");
       return false;
   }

//2nd way// cleanoutmail api 
$response  = Http::get("https://cleanoutmails.com/api/getverifyemail.php?email=$post_email&api_key=kQJY2EfJML4rXD938IzYm6jMf2vZizhc");
            
$response->collect();
            
$status = $response['status'];

if($status=="Valid"){
echo "valid";
}


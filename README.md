Opencart-2.x-3.x---APCU-Caching
Upload the files on your website root folder (like public_html or httpdocs)  

version < 2.2.0 
Edit the index.php, find the  

`
$cache = new Cache('file');  
`
and change it to  

`
$cache = new Cache('apcu');  
`

version >= 2.2.0  <br/>
Edit the /system/config/default.php, find  <br/>

`
$_['cache_type']           = 'file'; // apc, file or mem
`
`
$_['cache_expire']         = 3600;
`

change it to  

`
$_['cache_type']           = 'apcu'; // apc, file or mem 
`
`
$_['cache_expire']         = 3600;
`

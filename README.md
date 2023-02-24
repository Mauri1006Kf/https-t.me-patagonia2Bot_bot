https://pagar.uala.com.ar/orders/3606ee89-e4f8-4931-bd83-b46c51ef0111?retry
Ualá Bis - SDK PHP
MENU
Uala
HttpRequest
in package 
Application
HttpRequest.php : 7 
Table of Contents 
$defaultConfig : mixed$defaultHeaders : mixedget() : mixedpost() : mixedexecute() : mixedgetHeaders() : mixed
Properties 
$defaultConfig 
HttpRequest.php : 9 private static mixed $defaultConfig = [CURLOPT_RETURNTRANSFER => true, CURLOPT_ENCODING => '', CURLOPT_MAXREDIRS => 10, CURLOPT_TIMEOUT => 3, CURLOPT_FOLLOWLOCATION => true, CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1, CURLOPT_HEADER => true, CURLOPT_RETURNTRANSFER => true]
$defaultHeaders 
HttpRequest.php : 20 private static mixed $defaultHeaders = ['Content-Type: application/json']
Methods 
get() 
HttpRequest.php : 67 public static get(mixed $url[, mixed $data = [] ][, mixed $headers = [] ]) : mixed
Parameters
$url : mixed$data : mixed = []$headers : mixed = []
Return values
mixed —
post() 
HttpRequest.php : 52 public static post(mixed $url[, mixed $data = [] ][, mixed $headers = [] ]) : mixed
Parameters
$url : mixed$data : mixed = []$headers : mixed = []
Return values
mixed —
execute() 
HttpRequest.php : 29 private static execute(mixed $curl) : mixed
Parameters
$curl : mixed
Return values
mixed —
getHeaders() 
HttpRequest.php : 24 private static getHeaders(mixed $headers) : mixed
Parameters
$headers : mixed
Return values
mixed —
<?php namespace Uala; use Uala\Error; class HttpRequest { private static $defaultConfig = [ CURLOPT_RETURNTRANSFER => true, CURLOPT_ENCODING => '', CURLOPT_MAXREDIRS => 10, CURLOPT_TIMEOUT => 3, CURLOPT_FOLLOWLOCATION => true, CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1, CURLOPT_HEADER => true, CURLOPT_RETURNTRANSFER => true ]; private static $defaultHeaders = [ 'Content-Type: application/json', ]; private static function getHeaders($headers) { return array_merge(self::$defaultHeaders, $headers); } private static function execute($curl) { $response = curl_exec($curl); $body = substr($response, curl_getinfo($curl, CURLINFO_HEADER_SIZE)); $body = (object) json_decode($body); $statusCode = curl_getinfo($curl, CURLINFO_HTTP_CODE); if ($statusCode < 400) { return (object) [ "status" => $statusCode, "body" => $body, ]; } throw new Error( $body->message ?? $body->Message ?? 'Unknown error', $body->code ?? '666', $statusCode ); } public static function post($url, $data = [], $headers = []) { $curl = curl_init(); $curlOptions = self::$defaultConfig + [ CURLOPT_URL => $url, CURLOPT_CUSTOMREQUEST => 'POST', CURLOPT_POSTFIELDS => json_encode($data), CURLOPT_HTTPHEADER => self::getHeaders($headers) ]; curl_setopt_array($curl, $curlOptions); return self::execute($curl); } public static function get($url, $data = [], $headers = []) { $curl = curl_init(); $curlOptions = self::$defaultConfig + [ CURLOPT_URL => $url . '?' . http_build_query($data), CURLOPT_CUSTOMREQUEST => 'GET', CURLOPT_HTTPHEADER => self::getHeaders($headers) ]; curl_setopt_array($curl, $curlOptions); return self::execute($curl); } } 
X
Search results
<script async src=
"https://telegram.org/js/telegram-widget.js?21" data-telegram-login="banco1_bot" data-size="large" data-onauth="onTelegramAuth(user)" data-request-access="write">
</script>
<script type="text/javascript">
  function onTelegramAuth(user) {
    alert('Logged in as ' + user.first_name + ' ' + user.last_name + ' (' + user.id + (user.username ? ', @' + user.username : '') + ')');
  }
</script>

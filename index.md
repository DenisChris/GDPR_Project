
<h1>GDPR Cookies lab</h1>
<p>Student: Denis Chris Isac.</p>

<h2>Welcome!.</h2>

<script> 
 document.cookie = "session: you are being watched";
 document.cookie = "Ne place sa stim pe ce dai click";
 function alertCookie() { alert(document.cookie); }
 </script>

<button onclick="alertCookie()">Show cookies</button>

<script>
allCookies = document.cookie;
document.cookie = newCookie;

document.cookie = "your operating system is : Windows 10";
document.cookie = "your location: Romania";
function alertCookie() {
  alert(document.cookie);
}
</script>

<button onclick="alertCookie()">Show cookies</button>

<script> 
 
document.cookie = "test1=Hello";
document.cookie = "test2=World";

const cookieValue = document.cookie
  .split('; ')
  .find(row => row.startsWith('test2='))
  .split('=')[1];

function alertCookieValue() {
  alert(cookieValue);
}
 </script> 
 
<button onclick="alertCookieValue()">Show cookie value</button>
 
 <script> 
 function doOnce() {
  if (!document.cookie.split('; ').find(row => row.startsWith('doSomethingOnlyOnce'))) {
    alert("Do something here!");
    document.cookie = "doSomethingOnlyOnce=true; expires=Fri, 31 Dec 9999 23:59:59 GMT";
  }
}
 </script>
 
<button onclick="doOnce()">Only do something once</button>

 <script> 
function resetOnce() {
  document.cookie = "doSomethingOnlyOnce=; expires=Thu, 01 Jan 1970 00:00:00 GMT";
}
 </script>
<button onclick="resetOnce()">Reset only once cookie</button>


<p>Date: <span id="datetime"></span></p>

<script>
var dt = new Date();
document.getElementById("datetime").innerHTML = dt.toLocaleDateString();
</script>


<script> 
 document.cookie = "session: you are being watched";
 document.cookie = "Ne place sa stim pe ce dai click";
 function alertCookie() { alert(document.cookie); }
 </script>

<body> Welcome, my friend! <button onclick="alertCookie()">Show cookies</button> </body>

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
 
<button onclick="alertCookieValue()">Show cookie value</button
 
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

//ES5

if (document.cookie.split(';').some(function(item) {
    return item.trim().indexOf('reader=') == 0
})) {
    console.log('The cookie "reader" exists (ES5)')
}

//ES2016

if (document.cookie.split(';').some((item) => item.trim().startsWith('reader='))) {
    console.log('The cookie "reader" exists (ES6)')
}

//ES5

if (document.cookie.split(';').some(function(item) {
    return item.indexOf('reader=1') >= 0
})) {
    console.log('The cookie "reader" has "1" for value')
}

//ES2016

if (document.cookie.split(';').some((item) => item.includes('reader=1'))) {
    console.log('The cookie "reader" has "1" for value')
}


<h1>Events</h1>

<p>Pada chapter ini kita akan belajar bagaimana cara PhoneGap handle sebuah event. Events yang dimaksud dalam PhoneGap itu sendiri adalah sama dengan Events yang ada pada javascript. Sebuah Action bisa muncul pada device, sebagai contoh DOM (Document Object Model) telah dimuat dan device telah "Ready" maka kita bisa melakukan suatu hal.</p>

<h3>Understanding Events</h3>
<p>Jika disederhanakan lebih spesifik lagi <strong>event</strong> adalah sebuah action yang dideteksi oleh PhoneGap. Pada Pemograman JavaScript Tradisional sebuah elemen dalam sebuah web bisa memiliki event yang bisa menimbulkan suatu trigger. Sebagai contoh <strong>onrollover</strong> event pada sebuah link akan memunculkan sebuah pesan atau pada <strong>onclick</strong> sebuah fungsi javascript akan dieksekusi.
Banyak sekali event yang bisa kita gunakan dan semuanya bisa digunakan untuk phonegap, namun meskipun begitu ada beberapa event yang memang secara khusus didesain spesifik untuk phonegap diantaranya adalah :</p>

<ol>
<li>backbutton</li>
<li>deviceready</li>
<li>menubutton</li>
<li>pause</li>
<li>resume</li>
<li>searchbutton</li>
<li>online</li>
<li>offline</li>
</ol>

<p>Dari semua itu event <strong>onDeviceReady</strong> adalah event yang paling penting sebab tanpa event ini mobile application yang kita buat tidak akan pernah tahu jika phonegap telah dimuat sepenuhnya. Jika event ini telah siap maka kita bisa memanggil fungsi fungsi yang kita buat untuk mengakses Native API. Agar lebih faham lagi kita harus menguji event <strong>onDeviceReady</strong> pada aplikasi phonegap yang kita buat. Saat event ini sudah siap ada dua hal yang harus kita ketahui : 
Sesaat DOM (document object model) telah dimuat begitu juga dengan PhoneGap API kita bisa mendeteksi event event lainya dan melakukan segala sesuai yang kita inginkan.</p>

<h3>Using The Event Listener</h3>
<p>Untuk menggunakan suatu event kita memerlukan <strong>event listener</strong> sebagai contoh jika kita ingin mendeteksi event <strong>onDeviceReady</strong> maka kita perhatikan code dibawah ini : </p>


```html
<!DOCTYPE html>
<html>
<head>
<title>PhoneGap Device Ready Example</title>
<script type=”text/javascript” charset=”utf-8” src=”phonegap.js”></script>
<script type=”text/javascript” charset=”utf-8”>
document.addEventListener(“deviceready”, onDeviceReady, false);
function onDeviceReady() {
// call the phonegap api
}
</script>
</head>
<body>
</body>
</html>
```

<p>Pada code diatas kita melampirkan sebuah event listener dengan statement <strong>document.addEventListener</strong> sehingga ketika event listener sudah berada dalam state siap (deviceready) ini artinya DOM HTML telah dimuat, selanjutnya kita akan menggunakan pemisah listener untuk setiap event yang akan kita buat. Seluruh <strong>event listener</strong> akan disimpan didalam fungsi <b>onDeviceReady()</b> sebagai contoh jika kita ingin mendeteksi event <b>pause</b> dan <b>resume</b> event listener harus
disimpan didalam fungsi onDeviceReady() seperti pada code dibawah ini :</p>

```html
<!DOCTYPE html>
<html>
<head>
<title>PhoneGap Device Ready Example</title>
<script type=”text/javascript” charset=”utf-8” src=”phonegap.js”></script>
<script type=”text/javascript” charset=”utf-8”>
document.addEventListener(“deviceready”, onDeviceReady, false);
function onDeviceReady() {
// call the phonegap api
document.addEventListener(“pause”, onPause, false);
document.addEventListener(“resume”, onResume, false);
}
function onPause(){
}
function onResume(){
}
</script>
</head>
<body>
</body>
</html>
```

<H3>Understanding Event Type</h3>
<p>Sekarang kita akan mengkaji lebih detail tentang tipe tipe yang dimiliki oleh sebuah event.</p>

<h4>backbutton</h4>
<p>event backbutton akan dieksekusi saat user menekan tombol back pada android device. Untuk mendeteksi event ini simpan didalam event listener seperti pada code dibawah ini :</p>

```javascript
document.addEventListener(“backbutton”, onBackButton, false);
function onBackButton(){
//handle the back button
}
```

<p>Seperti yang telah kita pelajari sebelumnya agar event ini dieksekusi dia harus berada didalam fungsi onDeviceReady() seperti pada code dibawah ini :</p>

```html
<!DOCTYPE html>
<html>
<head>
<title>PhoneGap backbutton Example</title>
<script type=”text/javascript” charset=”utf-8” src=”phonegap.js”></script>
<script type=”text/javascript” charset=”utf-8”>
document.addEventListener(“deviceready”, onDeviceReady, false);
function onDeviceReady() {
// Register the event listener
document.addEventListener(“backbutton”, onBackButton, false);
}
// Handle the back button
//
function onBackButton() {
}
</script>
</head>
<body>
</body>
</html>
```

<h4>deviceready</h4>
<p>Seperti yang telah kita fahami sebelumnya event deviceready adalah event yang paling penting sebab kita harus mengeksekusi event ini terlebih dahulu agar kita bisa mengeksekusi event event lainya.</p>

```javascript
document.addEventListener(“deviceready”, onDeviceReady, false);
function onDeviceReady(){
//ready!
}
```

<p>Jika kita sedang mengembangkan mobile application untuk BB yaitu BlackBerry OS 4.6. Research in Motion (RIM) Browserfield tidak memiliki support custom event sehingga event deviceready tidak akan dieksekusi. Sebagai gantinya kita bisa menggunakan <b>phonegap.available</b> seperti pada code dibawah ini: </p>

```javascript
function onLoad() {
var intervalID = window.setInterval(
function() {
if (PhoneGap.available) {
window.clearInterval(intervalID);
onDeviceReady();
}
},
500
);
}
function onDeviceReady() {
// use the phonegap api!
}
```


<h4>menubutton</h4>
<p>event menubutton akan dieksekusi saat user menekan tombol menu pada android device. Untuk mendeteksi event ini simpan didalam event listener seperti pada code dibawah ini :</p>

```javascript
document.addEventListener(“menubutton”, onMenuButton, false);
function onMenuButton(){
//handle the menu button
}
```

<p>Seperti yang telah kita pelajari sebelumnya agar event ini dieksekusi dia harus berada didalam fungsi onDeviceReady() seperti pada code dibawah ini :</p>

```html
<!DOCTYPE html>
<html>
<head>
<title>PhoneGap menubutton Example</title>
<script type=”text/javascript” charset=”utf-8” src=”phonegap.js”></script>
<script type=”text/javascript” charset=”utf-8”>
document.addEventListener(“deviceready”, onDeviceReady, false);
function onDeviceReady() {
// Register the event listener
document.addEventListener(“menubutton”, onMenuButton, false);
}
// Handle the menu button
//
function onMenuButton() {
}
</script>
</head>
<body>
</body>
</html>
```

<h4>pause</h4>
<p>event pause akan dieksekusi ketika aplikasi disimpan sebagai background, sebuah aplikasi akan dinyatakan pause ketika dia bukan lagi sebagai foreground (active windows). </p>

```javascript
document.addEventListener(“pause”, onPause, false);
function onPause(){
//handle the pause event
}
```
<p>Seperti yang telah kita pelajari sebelumnya agar event ini dieksekusi dia harus berada didalam fungsi onDeviceReady() seperti pada code dibawah ini :</p>

```html  
<!DOCTYPE html>
<html>
<head>
<title>PhoneGap pause Example</title>
<script type=”text/javascript” charset=”utf-8” src=”phonegap.js”></script>
<script type=”text/javascript” charset=”utf-8”>
document.addEventListener(“deviceready”, onDeviceReady, false);
function onDeviceReady() {
// Register the event listener
document.addEventListener(“pause”, onPause, false);
}
// Handle the pause
//
function onPause() {
}
</script>
</head>
<body>
</body>
</html>
```

<h4>resume</h4>
<p>event resume akan dieksekusi ketika aplikasi dikembalikan lagi menjadi foreground (active window) setelah sebelumnya ia dijadikan sebagai background.</p>

```javascript
document.addEventListener(“resume”, onResume, false);
function onResume(){
//handle the resume event
}
```

<p>Seperti yang telah kita pelajari sebelumnya agar event ini dieksekusi dia harus berada didalam fungsi onDeviceReady() seperti pada code dibawah ini :</p>

```html  
<!DOCTYPE html>
<html>
<head>
<title>PhoneGap resume Example</title>
<script type=”text/javascript” charset=”utf-8” src=”phonegap.js”></script>
<script type=”text/javascript” charset=”utf-8”>
document.addEventListener(“deviceready”, onDeviceReady, false);
function onDeviceReady() {
// Register the event listener
document.addEventListener(“resume”, onResume, false);
}
// Handle the resume
//
function onResume() {
}
</script>
</head>
<body>
</body>
</html>
```

<h4>searchbutton</h4>
<p>event searchbutton akan dieksekusi jika user menekan tombol search pada android device.</p>

```javascript
document.addEventListener(“searchbutton”, onSearchButton, false);
function onSearchButton(){
//handle the search button
}
```

<p>Seperti yang telah kita pelajari sebelumnya agar event ini dieksekusi dia harus berada didalam fungsi onDeviceReady() seperti pada code dibawah ini :</p>

```html
<!DOCTYPE html>
<html>
<head>
<title>PhoneGap searchbutton Example</title>
<script type=”text/javascript” charset=”utf-8” src=”phonegap.js”></script>
<script type=”text/javascript” charset=”utf-8”>
document.addEventListener(“deviceready”, onDeviceReady, false);
function onDeviceReady() {
// Register the event listener
document.addEventListener(“searchbutton”, onSearchButton, false);
}
// Handle the search button
//
function onSearchButton() {
}
</script>
</head>
<body>
</body>
</html>
```

<h4>online</h4>
<p>event online akan dieksekusi jika phonegap application sedang berada dalam state online, event ini hanya support untuk iOS, Android dan blackberry.</p>

```javascript
document.addEventListener(“online”, isOnline, false);
function isOnline(){
//handle the online event
}
```

<p>Seperti yang telah kita pelajari sebelumnya agar event ini dieksekusi dia harus berada didalam fungsi onDeviceReady() seperti pada code dibawah ini :</p>

```html
<!DOCTYPE html>
<html>
<head>
<title>PhoneGap online Example</title>
<script type=”text/javascript” charset=”utf-8” src=”phonegap.js”></script>
<script type=”text/javascript” charset=”utf-8”>
document.addEventListener(“deviceready”, onDeviceReady, false);
function onDeviceReady() {
// Register the event listener
document.addEventListener(“online”, isOnline, false);
}
// Handle the online event
//
function isOnline() {
}
</script>
</head>
<body>
</body>
</html>
```

<h4>offline</h4>
<p>event offline akan dieksekusi jika phonegap application sedang berada dalam state offline, event ini hanya support untuk iOS, Android dan blackberry.</p>

```javascript
document.addEventListener(“offline”, isOffline, false);
function isOffline(){
//handle the offline event
}
```

<p>Seperti yang telah kita pelajari sebelumnya agar event ini dieksekusi dia harus berada didalam fungsi onDeviceReady() seperti pada code dibawah ini :</p>

```html
<!DOCTYPE html>
<html>
<head>
<title>PhoneGap offline Example</title>
<script type=”text/javascript” charset=”utf-8” src=”phonegap.js”></script>
<script type=”text/javascript” charset=”utf-8”>
document.addEventListener(“deviceready”, onDeviceReady, false);
function onDeviceReady() {
// Register the event listener
document.addEventListener(“offline”, isOffline, false);
}
// Handle the offline event
//
function isOffline() {
}
</script>
</head>
<body>
</body>
</html>
```

<p>Setelah mempelajari hal itu semua sekarang kita akan mengaplikasikanya dengan membuat mobile application sederhana. Mobile Application akan merespon dua event yaitu event <b>resume</b> dan <b>pause</b>. Dibawah ini adalah sample code mobile application tersebut :</p>

```html
<!DOCTYPE html>
<html>
<head>
<title>PhoneGap Event Example</title>
<script type=”text/javascript” charset=”utf-8” src=”phonegap.js”></script>
<script type=”text/javascript” charset=”utf-8”>
document.addEventListener(“deviceready”, onDeviceReady, false);
function onDeviceReady() {
// Register the event listeners
document.addEventListener(“pause”, onPause, false);
document.addEventListener(“resume”, onResume, false);
}
// Handle the pause
//
function onPause() {
alert(“Paused!”);
}
// Handle the resume
//
function onResume() {
alert(“Resumed!”);
}
</script>
</head>
<body>
</body>
</html>
```

<h4>How it Works</h4>
<p>Pertama <b>event listener</b> adalah kunci sebab ini akan mendeteksi event type <b>deviceready</b> jika event ini sudah dieksekusi selanjutnya kita bisa memanggil PhoneGap API dengan aman, selain itu event type deviceready akan mengeksekusi fungsi OnDeviceReady() yang didalamnya terdapat dua event listener yaitu pause event dan resume event.</p>

<p>Selanjutnya kita akan membuat mobile application sederhana lagi yang memiliki kemampuan untuk mendeteksi klik dari suatu tombol. Perhatikan code dibawah ini :</p>

```html
<!DOCTYPE html>
<html>
<head>
<title>PhoneGap Button Example</title>
<script type=”text/javascript” charset=”utf-8” src=”phonegap.js”></script>
<script type=”text/javascript” charset=”utf-8”>
document.addEventListener(“deviceready”, onDeviceReady, false);
function onDeviceReady() {
// Register the event listeners
document.addEventListener(“searchbutton”, onSearch, false);
document.addEventListener(“menubutton”, onMenuButton, false);
document.addEventListener(“backbutton”, onBackButton, false);
}
// Handle the backbutton
//
function onBackButton() {
alert(“You hit the back button!”);
}
// Handle the menubutton
//
function onMenuButton() {
alert(“You hit the menu button!”);
}
// Handle the searchbutton
//
function onSearchButton() {
alert(“You hit the search button!”);
}
</script>
</head>
<body>
</body>
</html>
```

<h4>How it Works</h4>
<p>Hampir sama seperti sample mobile application sebelumnya setelah kita memastikan phonegap application telah siap tiga buah event listener diregistrasikan didalam fungsi OnDeviceReady()</p>



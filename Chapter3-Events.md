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

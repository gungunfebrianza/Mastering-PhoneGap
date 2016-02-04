<h1>Set up adobe build service</h1>

<p>Saya asumsikan kita tidak mempunyai seluruh device seperti iPhone, Android, BlackBerry, Firefox OS dan sebagainya, selain itu kita tidak ingin atau tidak bisa melakukan instalasi SDK (Software Development Kit) dari setiap platform. Jadi untuk masalah kompilasi kita akan menggunakan jasa Adobe Phonegap Build yang bisa kita buka di : build.phonegap.com 
Sebenarnya servis ini didesain secara spesifik untuk developer yang ingin project mereka dikompilasi on the cloud dan menerima app-store ready apps untuk iOS, Android, webOS, Symbian, BlackBerry, Windows Phone 7, dan devices lainya. Untuk menggunakan layanan ini kita harus melakukan registrasi terlebih dahulu di https://build.phonegap.com/plans</p>

<p>Silahkan anda masuk ke halaman tersebut dan pilih Completely Free</p>
<img src="https://github.com/PUSRISTEK/Learning-PhoneGap/blob/master/image/phonegap-signup.JPG"></img>

<p>Setelah melakukan proses signup, pada tab private terdapat tombol upload zip. Tombol itu akan menjadi tempat kita melakukan proses upload source code phonegap application untuk dikompilasi on the cloud, kemudian aplikasi yang telah dikompilasi bisa kita instalasi di smartphone device melalui QR Code yang diberikan. Sebelum masuk kesini kita akan mengkaji
Sebuah source code sederhana yang telah saya sediakan.</p> <img src="https://github.com/PUSRISTEK/Learning-PhoneGap/blob/master/image/phonegap-upload.JPG"></img>

<p>Sebagai bahan uji coba kita akan membuat sebuah aplikasi mobile yang akan berjalan diplatform iOS dan Android, proses kompilasinya sendiri akan menggunakan layanan cloud milik adobe. Silahkan buka folder <strong>source-code-sample</strong> didalamnya terdapat sebuah file bernama <strong>Hello World.zip</strong>. Dibawah ini adalah Struktur dari source code Hello World:</p>
<img src="https://github.com/PUSRISTEK/Learning-PhoneGap/blob/master/image/phonegap-structure-project.JPG"></img>

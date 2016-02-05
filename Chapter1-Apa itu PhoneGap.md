<h1>Apa Itu PhoneGap</h1>

<p>PhoneGap adalah sebuah project open source yang digunakan untuk membuat sebuah mobile application. Dengan PhoneGap kita bisa menggunakan web technology (HTML, CSS & Javascript) untuk membuat sebuah mobile application. HTML, CSS dan Javascript akan diubah menjadi suatu package yang bisa digunakan diberbagai device yang memiliki platform yang berbeda-beda.</p>

<p>PhoneGap memiliki Foreign Function Interface(FFI) yang bisa membantu kita untuk mengakses native features dari suatu device. Native Feature yang dimiliki oleh suatu platform seperti camera, geolocation, accelerometer, file dan sebagainya bisa kita akses menggunakan Javascript melalui interface FFI. Selain itu kita juga bisa mengakses Native User Interface yang dimiliki
suatu platform menggunakan FFI. Misalkan untuk menampilkan sebuah dialog.</p>

<p>Meskipun begitu membuat aplikasi dengan phonegap tidak sama dengan membangun sebuah website. Sebab filosofi phonegap adalah bagaimana caranya membuat sebuah web agar bisa berkomunikasi dengan sebuah hardware device. Kemudian jika kita membuat aplikasi dengan phonegap yang akan didistribusikan kedalam sebuah marketplace, diusahakan isinya jangan hanya berisi sebuah static webpage tanpa memanfaatkan kemampuan suatu API milik phonegap.
sebab beberapa application store akan menolaknya disebabkan aplikasi mobile yang dibuat tidak memiliki nilai untuk ditampilkan di application store. Banyak sekali aplikasi mobile yang dibuat menggunakan phonegap sukses dimarketplace.</p>

<h3>History</h3>
<p>Phonegap pertama kali dikembangkan oleh iPhoneDevCamp pada kegiatan hackathon pada tahun 2008. Banyak sekali yang ikut berkontribusi mengembangkan phonegap sebab setiap iphone developer yang masih newbie pasti menggunakan <strong>Objective-C</strong>. Sementara tidak semua web developer memahami Objective-C. Satu pertanyaan universal yang mendorong teciptanya phonegap adalah apakah mungkin seseorang menciptakan sebuah framework yang
bisa membantu web developer untuk menggunakan kemampuan HTML, CSS dan Javascript agar bisa berinteraksi dengan native device seperti iPhone, Blackberry, Android etc untuk mengakses native features yang dimiliki setiap native device? seperti camera, accelerometer, gyroscope dst.. </p>

<p>Waktu terus berlalu akhirnya Phonegap terus dikembangkan oleh suatu perusahaan yang bernama Nitobi yang pada akhirnya diakuisisi oleh adobe, sebagai bagian dari suatu yang diakuisisi source code dari phonegap akhirnya didonasikan kepada [ASF] Apache Software Foundation yang membuat phonegap menjadi open source. Pertama kali dikenal dengan sebutan Apache Cordova.</p>
<p>Banyak sekali pertanyaan tentang apa sih perbedaan phonegap dengan apache cordova?
PhoneGap adalah Cordova + dengan layanan adobe yang membuat kapabilitasnya menjadi lebih luas sementara cordova bersifat independen</p>

<h3>Foreign Function Interface</h3>
<p>Sistem FFI yang disediakan membuat kita sebagai developer mampu membangun sebuah jembatan antara javascript dan native code untuk mengerjakan sebuah task. Sekumpulan Foreign Function ini dibundle didalam sebuah plug-ins meskipun begitu cordova atau phonegap sudah menyediakan beberapa fitur dasar dalam masing masing base package.</p>
<p>PhoneGap menawar banyak sekali fitur yang dibutuhkan untuk mengembangkan sebuah mobile application, selanjutnya kita akan belajar menggunakan phonegap command line interface yang bita kita gunakan untuk membangun dan memelihara aplikasi phonegap melalui terminal. Dengan CLI pula kita bisa package dan compile mobile application yang telah kita buat
untuk diuji coba baik itu menggunakan virtual emulator atau perangkat device asli. PhoneGap CLI adalah alat bantu yang bisa digunakan untuk mempersiapkan aplikasi yang kita buat sebelum didistribusikan dimarketplace seperti apple store atau google play.</p>

<p>PhoneGap menawarkan beberapa kemampuan agar kita bisa mengakses native features seperti :</p>
<ol>
<li>Accelerometer</li>
<li>Camera</li>
<li>Compass</li>
<li>Contacts</li>
<li>Files</li>
<li>Geolocation</li>
<li>Media</li>
<li>Network</li>
<li>Notification(alert, sound, vibration)</li>
<li>Storage</li>
</ol>

<p>Jika kita mengembangkan mobile application untuk platform iOS dan Android device kesempatan untuk memiliki semua fitur diatas besar. Meskipun begitu ada beberapa commonly native features yang tidak akan bisa kita gunakan dibeberapa platform jika kita mengembangkan aplikasi untuk blackberry, WebOS, Windows Phone7, Symbian dan sebagainya. Sebagai contoh pada windows phone 7 tidak disediakan fitur untuk mengakses camera, compass dan storage.</p>

<h3>Supported Platform</h3>
<p>PhoneGap application mempunyai kemampuan untuk berjalan dibanyak mobile platform dengan menggunakan 1 codebase. Dengan plugins kita bisa membuat PhoneGap project yang kita buat menjadi lebih baik lagi, karena didalam plugins terdapat sekumpulan script yang bisa kita gunakan untuk menambah fungsi-fungsi baru kedalam aplikasi mobile yang kita buat.</p>

<h3>PhoneGap Capabilities</h3>
<p>Jika kita ingin membuat mobile application yang kita buat bisa berinteraksi dengan sebuah remote web service misalkan sebuah RESTful API kita bisa menggunakan jQuery agar bisa memainkan AJAX, kemudian jika mobile application yang kita buat berjalan dengan harapan pada iPhone Device ini bukan berarti akan berjalan dengan sempurna juga di device lainya. Hal yang harus kita lakukan adalah mengujinya satupersatu.</p>

<h4>Understanding The Basic of PhoneGap Application :</h4>
<p>Kita akan membahas beberapa hal dasar yang bisa kita lakukan menggunakan phonegap.</p>

<h4>1. Working With Contacts</h4>
<p>List Contacts merupakan Ubiquitous Feature sebab pasti ada diseluruh smartphones. Ada beberapa method yang bisa kita pakai menggunakan PhoneGap diantaranya adalah :</p>
<ul>
<li>Untuk membuat sebuah contact kita bisa menggunakan method <i>create()</i></li>
<li>Untuk menyimpan sebuah contact kita bisa menggunakan method <i>save()</i></li>
<li>Untuk mencari sebuah contact kita bisa menggunakan method <i>find()</i></li>
<li>Untuk menduplikasi sebuah contact kita bisa menggunakan method <i>clone()</i></li>
<li>Untuk menghapus sebuah contact kita bisa menggunakan method <i>remove()</i></li>
</ul>

<p>Untuk membuat sebuah contact kita akan mengirimkan sebuah <b>Javascript Object Notation</b> ke method <i>contacts.create().</i> Informasi kontak akan disimpan didalam memori aplikasi namun jika ingin menyimpannya kedalam database maka kita akan menggunakan method <i>save().</i> PhoneGap API mendukung banyak sekali property untuk membuat sebuah field pada kontak seperti untuk menampilkan name, nickname, phone number, email addreses, birthday, gender, photos dan sebagainya yang selanjutnya
akan kita gunakan untuk melakukan pencarian menggunakan method <i>contacts.find()</i> untuk mendapatkan user yang dikehendaki.</p>
<p>Lalu <i>clone()</i> method dapat kita gunakan untuk kloning kontak yang ada dimemori begitu juga untuk menghapus sebuah kontak kita bisa menggunakan method <i>remove().</i></p>

<h4>2. Working With Camera</h4>
<p>Hampir sebagian besar smartphones sudah mendukung built-in camera. PhoneGap API memiliki dua jalan untuk melakukan capture sebuah gambar salah satunya akses camera melalui <i>camera</i> object, yang kedua menggunakan <i>media capture</i> API. Secara spesifik yaitu menggunakan <i>camera.getPicture()</i> untuk mengambil sebuah foto menggunakan camera atau menerima foto yang berasal dari device photo album. Kita juga bisa memilih agar camera menyediakan <b>Base64-encoded photo image (default)</b> atau lokasi file suatu image yang bisa kita gunakan
untuk render sebuah image, post image sebagai sebuah data ke kesebuah remote server, atau menyimpannya secara lokal.</p>

<h4>3. Working With Geolocation</h4>
<p>Hampir sebagian besar smartphones juga sudah memiliki kemampuan geolocation, dengan GPS sebuah smartphones bisa mendapatkan posisi latitude dan longtitude posisi saat ini secara akurat. <i>Geolocation</i> API pada phonegap membuat kita bisa mengetahui posisi device saat ini (latitude, longtitude dan sebagian lagi sudah mendukung altitude), selain itu bisa juga kita gunakan untuk melacak pergerakan sebuah device.</p>

<h4>4. Working With Media Files</h4>
<p>Phonegap memiliki <i>Media Capture</i> API yang bisa kita gunakan untuk melakukan capture data analog audio dan video, seperti merekam suara, play, pause, dan stop sebuah file media. Dengan ini kita bisa membuat sebuah mobile application yang memiliki kemampuan untuk merekam audio dan video</p>

<h4>5. Working With Storage Options</h4>
<p>Karena kita sudah menggunakan HTML5 kita bisa menggunakan SQLite untuk menyimpan data secara lokal yang selanjutnya bisa kita gunakan untuk melakukan singkronisasi data antara device dengan remote database. Mobile Application yang kita buat bisa menggunakan AJAX untuk memanggil data tertentu dalam sebuah remote database kemudian memanfaatkan JSON untuk mengirim dan menyimpanya kedalam SQLite didevice yang kita miliki.</p>

<h3>Quick Overview of The API</h3>
<p>Di bawah ini adalah beberapa API yang dimiliki oleh PhoneGap :</p>
<ul>
<li>Accelerometer, untuk berinteraksi dengan device motion sensor.</li>
<li>Camera, untuk capture photo menggunakan device camera.</li>
<li>Capture, untuk capture file media.</li>
<li>Compass, untuk berinteraksi dengan kompas.</li>
<li>Connection, untuk cek status koneksi ke jaringan Wifi atau Cellular Network.</li>
<li>Contacts, untuk berinteraksi dengan contact pada database device.</li>
<li>Device, untuk mendapatkan informasi device.</li>
<li>Event, untuk melakukan hook native event melalui javascript.</li>
<li>File, untuk melakukan hook native filesystem melalui javascript.</li>
<li>Geolocation, untuk mengetahui posisi device berada.</li>
<li>Media, untuk merekam dan memulai audio/video file.</li>
<li>Network, untuk cek koneksi kejaringan wifi.</li>
<li>Notification, untuk berinteraksi menggunakan notifikasi pada device.</li>
<li>Storage, untuk melakukan hook native device storage.</li>
</ul>

<h3>Mobile Design Issues</h3>
<p>Sedikit penekanan bahwa menciptakan mobile application dengan phonegap bukan berarti kemampuanya hanya sebatas bermain dengan API PhoneGap saja. Kita akan membuat mobile application menggunakan HTML 5, CSS dan Javascript. Selanjutnya kita akan menggunakan beberapa framework javascript lainya untuk melakukan desain User Interface seperti jQuery, jQTouch, Xuljs dan masih banyak lagi.</p>


<h3>Build & Testing PhoneGap Application</h3>
<p>[API] Application Programming Interface milik PhoneGap didesain agar bisa berkomunikasi dengan hardware dalam sebuah mobile device. Ada banyak sekali cara untuk membangun dan menguji aplikasi phonegap yang kita buat. Kabar bagusnya adalah kita cukup menggunakan satu codebase saja untuk membuat sebuah package yang bisa digunakan disetiap platform. 
Ada banyak cara untuk menguji mobile aplikasi yang kita buat baik itu menggunakan emulator atau live testing menggunakan suatu hardware device.</p>
<p>Sebagai contoh jika kita ingin mengembangkan sebuah mobile application untuk apple device seperti iphone, kita membutuhkan xcode yang harus kita install pada sebuah mac computer. Selanjutnya Developer bisa menggunakan xcode dan mengujinya menggunakan iOS simulator. Jadi jika kita ingin mengembangkan aplikasi agar bisa berjalan diberbagai platform kita membutuhkan beberapa software development yang terkait dengan platform yang ingin kita kembangkan.
Ini artinya kita tetap memerlukan sekumpulan software development untuk masing masing plafrom. Meskipun begitu mengembangkan mobile aplikasi dengan phonegap kita tetap menggunakan satu codebase saja.</p>

<h3>The Adobe PhoneGap Build Service</h3>
<p>PhoneGap sudah dilengkapi adobe service & extension yang membuat kapabilitas PhoneGap bisa lebih powerful. Salah satunya adalah Adobe PhoneGap Service yang membuat kita bisa menguji aplikasi mobile yang kita buat tanpa harus melakukan instalasi seluruh native SDK versi terakhir dan membeli seluruh device agar kita bisa menguji aplikasi mobile yang kita buat satu persatu, sebab adobe sudah menyediakan semua hal yang kita butuhkan dan prosesnya akan dilakukan secara cloud.</p>
<p>Masalah seperti munculnya OS versi terbaru, SDK Versi terbaru, mobile device terbaru yang bisa muncul setiap bulan kini tidak akan lagi menjadi duri tajam yang menusuk. Code yang akan kita buat tetap berada dalam operasi standar yang akan berjalan diseluruh platform. Semua ini adobe tawarkan melalui layanan three-tier plan yang bisa kita akses di : build.phonegap.com/plans. Layanan ini (Adobe PhoneGap Build Service) bisa kita gunakan agar kita tidak perlu melakukan instalasi software development seperti xcode untuk membuat sebuah mobile application dengan PhoneGap. Layanan ini akan membantu anda untuk membuat sebuah mobile application secara cloud.
sebelum kita menggunakan Adobe PhoneGap Build Service selanjutnya kita akan melakukan instalasi phonegap.</p>

<h3>Instalasi PhoneGap</h3>
<p>Kita membutuhkan PhoneGap Dekstop Application yang menyediakan layanan drag and drop untuk membuat sebuah phonegap application. Ini hanya sebagai alternatif bagi mereka yang menginginkan pengembangan mobile aplikasi secara visual, meskipun begitu kita tetap bisa menggunakan phonegap command line interface untuk membuat mobile application.</p>
<p>Untuk OS Windows silahkan download disini :</p>
<p><a href="https://github.com/phonegap/phonegap-app-desktop/releases/download/0.2.1/PhoneGapSetup-win32.exe">Download</a></p>
<p>Download dan lakukan instalasi sampai selesai. Kemudian ada beberapa lagi yang harus kita instal yaitu :</p>

<ul>
<li>Python Versi 2.7 - <a href="https://www.python.org/download/releases/2.7/">Download</a></li>
<li>Git - <a href="http://git-scm.com/downloads">Download</a></li>
<li>Node.js - <a href="https://nodejs.org/en/download/">Download</li>
</ul>

Jika sudah kita akan melakukan instalasi Cordova :

```
npm install -g cordova
```

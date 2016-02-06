<h1>Start Up!</h1>
<p>Ada beberapa konsep inti yang harus kita fahami sebelum terjun kedunia <b>Front End Web Development</b>
sebab ini akan menjadi fondasi yang akan kita bangun sambil mempelajari beberapa skill sekaligus. Ada banyak sekali buku yang menjelaskan tentang seluk beluk HTML, CSS dan JavaScript.
Sebab semua itu akan menjadi fondasi yang kita gunakan untuk membuat PhoneGap Application.</p>

<h3>JavaScript Object Literals</h3>
<p>Jika anda baru memulai belajar pemograman, ada sebuah frasa atau terminologi dalam pemograman yang disebut dengan
OOP (object oriented programming) sebuah paradigma pemograman yang menganalogikan segala sesuatu di alam semesta ini
yang bisa kita sentuh pasti memiliki properties dan values. Anda bisa membaca ebook bagian awal saja dari ebook yang
telah saya buat sebelumnya untuk memahami OOP. Cek disini : https://github.com/PUSRISTEK/OOPPHPPDO </p>

<p>Sebagai contoh jika anda adalah sebuah object maka nama, umur, tinggi, berat adalah properties yang anda miliki
dan informasinya disebut dengan values begitu juga dengan sebuah object literal dengan aturan values dari sebuah properties 
harus diisi pada sebuah properties yang sudah memiliki tipe data dengan artian kita akan menggunakan data yang valid.
Dalam javascript sebuah object literal disimpan didalam <b>Curly Brace seperti { key:value }</b> {} an empty brace juga
dinyatakan sebagai sebuah object hanya saja dia tidak memiliki properties dan values. Dibawah ini adalah contoh script
sebuah objek  yang didalamnya memiliki beberapa properties berikut dengan Primitive Data Types dan valuesnya</p>

```javascript
var object = {
string: "PhoneGap",
array: [4,2,0],
boolean: true,
number: 0,
emptyObject: {},
fn: function(){
var declaredButNoValueAssigned;
console.log("fn scoped variable: " + declaredButNoValueAssigned);
var emptyValue = null;
// This function returns a null value
return emptyValue;
}
};

console.log(obj.string); // value
console.log(typeof obj.string); // string
console.log(obj.array); // [4,2,0]
console.log(typeof obj.boolean);// boolean
console.log(typeof {}); // object
console.log(obj.fn());// fn scoped variable: undefined
// null
```
<h3>Namespace with Object Literals</h3>
<p>Dengan object literal kita bisa mengatur fungsi fungsi yang terkait dengan yang kita butuhkan. Namespace menjadi konsep umum dan powerful
untuk berbagi dengan bahasa pemograman lainya mulai dari server side scripting (Node.js) hingga ke client-side dan installable application dengan phonegap.
Semua bahasa pemograman mempunyai cara yang unik dalam mengekspresikan sebuah object dan ide. Masing masing mempunyai syntatical rules yang harus diikuti
agar bisa digunakan, sehingga mempunyai aturan yang ketat agar bisa mengkomunikasikan sebuah konsep agar dapat dimengerti oleh mesin komputer.
Dalam JavaScript sebuah <b>Object Literals</b> membantu developer dalam melakukan enkapsulasi logika dalam cara yang ekspresif dan penuh aturan sehingga
bisa difahami oleh developer lainya. Langsung saja dibawah ini adalah contoh penggunakan namespace dalam sebuah javascript : </p>

```javascript 
var app = {
settings: {
version: "0.0.1"
}
};
app.user = {};
app.user.register = function(){};
```

<p>Jika ingin memahami lebih dalam lagi tentang namespace dalam javascript silahkan anda baca buku <b>Essential JavaScript Namespacing Patterns</b> karya Addy Osmani.</p>

<h3>Loading Script with LABjs</h3>
<p>Ada banyak sekali cara dalam memuat sebuah javascript code mulai dari penggunaan tag <<b>script></b> atau menggunakan Content Delivery Network, namun ada cara yang lebih baik
untuk memanajemen script yaitu menggunakan LABjs. LABjs juga Open Source dibuat oleh Open Web Evangelist, Kyle Simpson. LABjs akan kita gunakan sebab kita akan berhadapan dengan banyak
sekali file javascript sehingga kita perlu mekanisme baru untuk memanajemenya, perhatikan code dibawah ini perbandingan antara cara tradisional memuat javascript dengan LABjs :</p>

<p>Tradisional</p>
```javascript 
<script src="framework.js"></script>
<script src="plugin.framework.js"></script>
<script src="myplugin.framework.js"></script>
<script src="init.js"></script>
```
<p>LABjs</p>
```javascript 
<script>
$LAB
.script("framework.js").wait()
.script("plugin.framework.js")
.script("myplugin.framework.js").wait()
.script("init.js").wait();
</script>
```

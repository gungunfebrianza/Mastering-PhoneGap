<h1>Previous Knowledge and Requirements</h1>
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

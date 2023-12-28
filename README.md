# OOP Introduction in Typescript
Repo untuk mereview ulang tentang OOP dan praktik menggunakan OOP di typescript.

## Review OOP
OOP adalah paradigma pemrograman dimana sebuah program disusun oleh objek-objek. Dalam OOP kita memecah aplikasi yang kompleks menjadi bagian-bagian kecil berupa objek. Objek di OOP merupakan representasi dari objek/benda di dunia nyata, misal: Menu Restoran. Sebuah objek wajib memiliki attribut dan perilaku. Sebagai permisalan, Menu Restoran bisa memiliki attribut berupa: nama menu, harga, stok dsb. Sedangkan untuk perilaku Menu Restoran dapat berupa: hitung harga total menu, cek ketersediaan menu, dsb. 

Pada OOP objek dibuat dengan cara menginstansiasikan (instansiasi adalah proses pembuatan objek baru dari sebuah class) sebuah class. Class adalah blueprint dari objek yang fungsi utamanya adalah untuk diinstansiasikan menjadi objek, jadi objek yang dibuat nantinya akan memiliki attribut-attribut dan method-method yand didefiniskan pada class. Sebagai contoh, Menu Restaurant jika dijadikan class di typescript akan menjadi seperti ini:

```typescript
class MenuRestoran {
  /** Constructor
  * constructor(args) adalah method bawaan javascript yang khusus digunakan untuk menginisialisasi sebuah objek dengan nilai-nilai argumen yang kita berikan pada constructor
  */
  contructor(nama: string, harga: number, stok: number) {
    // mengakses attribut objek perlu diawali dengan syntax `this` untuk menunjukkan variabel yang akan kita akses merupakan attribut objek
    this.nama = nama
    this.harga = harga
    this.stok = stok
  }

  totalHarga(jumlah: number) {
    return this.harga * jumlah
  }

  cekKetersediaan(jumlah) {
    stokSekarang = this.stok
    if ((stokSekarang - jumlah) < 0) {
      return false
    } else {
      return true
    }
  }  
}
```
Untuk menginstasiasikan class diatas kita dapat menggunakan syntax sebagai berikut: 
```typescript
// new MenuRestoran(args) akan memanggil constructor dengan argumen yang diberikan
const pizza = new MenuRestoran("pizza", 1000, 10)
console.log(pizza.name) // pizza
console.log(pizza.harga) // 1000
console.log(pizza.stok) // 10
console.log(pizza.cekKetersediaan(11)) // false
console.log(pizza.totalHarga(10)) // 10000
```
Untuk penjelasan lebih lengkap terkait class, bisa dibaca disini https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes.

## Pilar - pilar OOP

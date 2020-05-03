# MARKDOWN
Markdown adalah satu bahasa yang diciptakan untuk mempermudah pembuatan dan pembacaan code HTML. Markdown diciptakan dalam bahasa Perl.
Format tulisan makrdown sendiri adalah plain-text yang artinya kamu bisa membuat markdown dari text-editor biasa seperti notepad, sublime dll.
## Menjelaskan lebih lanjut tentang sintax Mardown
#### Paragraf^^
Membuat paragraf pada markdown itu mudah, yaitu dengan mengetikkan sesuatu yang kita inginkan maka itu akan otomatis dikonversi menjadi paragraf selama belum mengklik `enter`. Jadi `enter` adalah tanda awal paragraf.

#### Heading^^
Heading bisa juga disebut sebagai Judul. Membuat judul cukup dilakukan dengan kode hash `#`.
- Contoh nya untuk membuat judul `<h1>Ini Judul Paragraf</h1>` pada markdown syntaxnya `#Ini Judul Paragraf` 
- Dan kita dapat menggunakan `#` sebanyak 1-6 yang menandakan level tag `h` yang akan dibuat. Contoh satu lagi, kalau ingin membuat `<h3>Ini Judul Paragraf</h3>` pada markdown syntaxnya `### Ini Judul Paragraf`

#### Bold^^
Efek Bold dapat digunakan menggunakan syntax `**`. Misalnya untuk membuat `<b>Bold</b>` pada markdown syntaxnya seperti ini `**Bold**`. **Bold**

#### Efek Italyc^^
Efek italyc dapat dibuat dengan menggunakan syntax `*`. Misalnya untuk membuat `<i>Miring</i>` dapat digunakan syntax `*Miring*` pada markdown. *Gw dah agak miring*

#### Blockquote^^
Blockquote dapat dibuat dengan syntax `>ini blockquote` yang akan menghasilkan `<blockquote>ini blockquote</blockquote>`.
>ini blockquote

#### Ordered List^^
Ordered list atau daftar terurut adalah penomeran dari daftar item. Pembuatan `<ol><li>1. Telur Dadar</li><li>2. Ayam Geprek</li></ol>` dapat dilakukan dengan sederhana, tinggal mengetikkan `spasi` + `nomor` pada paragraf baru (harus mengetikkan enter terlebih dahulu). Contoh `1 Telur Dadar` akan menghasilkan :
  1. Telur Dadar
  2. Ayam Gepprek
 
#### Unordered List^^
 Unordered list atau daftar takk terurut dibuat dengan cara hampir sama dengan ordered list, namun unordered list mengguakan syntax `*`. Contoh : `* Telur Dadar` akan menghasilkan :
  * Telur Dadar
  * Ayam Geprek
  
#### Hyperlink^^
Hyperlink pada markdown cukup singkat. Untuk membuat `<a href='http://yourlink.com'>Your Link</a>` cukup dengan mengetikkan syntax `[Your Link](http://yourlink.com)`.Contoh `[link githubku](http://github.com)` akan menghasilkan : [link githubku](http://github.com)

#### Horizontal Rule^^
Horizontal Rule pada markdown dapat dibuat dengan syntax `---`kemudian ketik `enter`. Maka syntaxnya akan menghasilkan seperti ini :

---

#### Membuat Tabel^^
Tabel pada markdown dapat dibuat dengan cara seperti berikut :
`| Name  | Age |
 | ----- | --- |
 | Mia   | 18  |`
 dan hasilnya:
 | Name  | Age |
 | ----- | --- |
 | Mia   | 18  |


#### Menambahkan Gambar
Membuat ataupun menambahkan gambar pada markdown hampir mirip pengunaannya dengan [Hyperlink](https://github.com/ce318040/my_exercise/tree/master/task0x02#hyperlink).   
>![](image.png "Desc") atau bisa menggunakan sintaks HTML   
![DevOps](https://github.com/ce318040/my_exercise/blob/master/task0x02/img/devops_circle.jpg "DevOps Circle")


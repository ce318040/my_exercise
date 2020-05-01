**1. VCS (Version Control System)**  
Konsep VCS (Version Control System)
Menurutku VCS ini bukan video call tok ini salah satu kegunaan git , misalnya tok kita mau membangun sebuah proyek jadi ada banyak kita developernya ini tok, lalu proyek kita ini kita simpan di repositori online (GITHUB) dan lokal, yang lokal kita ambil dari online, jadi masing – masing developer bekerja di lokal. Nah, jdi developer ini nanti akan melakukan push (menambah/melakukan perubahan) terhadap proyek itu jadi tok versi proyek yang online udah berbeda dengan versi yang awal. Bisa aja ada yang ngubah Front End atau Back End nya. Nah jadi si VCS ini lah yang akan merekam semua perubahan itu tok, tapi kalo misalnya kita ingin kembali ke perubahan yang sebelum-sebelumnya pun bisa aja. 
- Contoh nya gini lah tok :
   * Kita (aku dan itok) ngerjain sebuah proposal PKM tok, jadi aku ngerjain Bab 1 dan itok ngerjain Bab 2. Nah proposal awal sebelumnya (tamplate) udah kita upload di github, lalu kita download lah proposal itu ke laptop kita. Nah, yang kita download ini lah kan yang mau kita ubah tok, nah setelah udah kita ubah, kita masing – masing upload versi terbaru kita tok, aku ngupload versi terbaru ku dan itok upload versi terbaru itok sendiri. Jadi si github ini nanti secara otomatis melakukan perubahan yang kulakukan dan perubahan yang itok lakukan. Tentunya Github juga mencatat aku melakukan perubahan A pada waktu B, dan juga mencatat perubahan X yang itok lakukan pada waktu Y. Jadi jikalaupun itok mau ngambil proposal versi sebelum itok ubah (masih hanya aku yang ubah) bisa saja tok, karena setiap perubahan yang kita lakukan pasti beda-beda versinya dan perubahan itu dicatat oleh github. Makanya dia namanya Version Control Tok. Dan tadi kan itok ngerjain bab 2 dan aku ngerjain bab 1, sewaktu kita sudah mengupload versi terbaru kita masing – masing ke github kan tok itu bakalan otomatis tergabung yang udah kita ubah itu tok. Jadi itu lah salah satu keistimewahan github juga tok.

**2. Cara Kerja GITHUB**
  -	`Repository (Repo)` itu folder proyek yang kita upload di github, jadi tadi proposal yang kita buat itu kita upload di repository tok.
  -	`Public reporitosy` itu semua orang (user) dapat melihat repo ku sendiri
  -	`Private repository` itu hanya aku yang dapat melihat repo ku dan beberapa user yang aku izinkan 
  -	Proses pengambilan (pertama kali) proposal yang ingin kita ubah dari github itu dinamakan `CLONE`
  -	Setelah di clone, proses download proposal itu bukan clone lagi namanya melainkan `PULL`
  -  Sewaktu sudah diubah proposalnya lalu diupload lagi (proses upload) namanya `PUSH`
  -  Sebelum kita push, kita harus buat `COMMIT`. `COMMIT` itu semacam pesan perubahan (misalnya : commit –m “mengubah judul proyek pada Bab 2”), setelah di commit baru dapat di Push. Intinya kita mempush proyek sekaligus mempush commit
  -  Nah sewaktu kita melakukan perubahan pada proposal kita kan tok, manatau ada yang  yang sama yang kita buat di proposal kita itu si github ini akan memberitahu apakah perubahan yang kita lakukan bertabrakan. Apabila terjadi seperti itu maka akan menghasilkan `BRANCH`. Branch punyaku dan Branch punya itok, Dia bercabang gitu tok.
    * Misalnya kayak gini tok :
      * Sewaktu “common base” belum ada tabrakan, yang hijau itu misalnya perubahan yang itok buat bertabrakan dengan masternya makanya dia menciptakan Branch yang baru. Nah, lalu untuk memperbaiki ini kalau bertabrakan kan tok akan kita merge. Kita pilih mana yang kita buang mana yang kita pertahankan. Lebih tepatnya tok Branch itu jalur (cabang) yang dilalui si titik hijau.
  -  Lalu ada juga namanya `FORK` tok, menurutku ini hampir sama dengan CLONE. Kan kalau Clone tadi dia mendownload ke lokal kita sementara kalau FORK ini semacam mendownload repository orang supaya tersimpan juga di repo kita (Simpelnya mencopy repository orang biar ada di repository kita),
      * Misalnya lah kan tok kita otak-atik lah code yang ada di repo kita (yang kita copy tadi),  lalu setelah itu kita mau gabungkan lah ke repo aslinya (punya orang lain tadi) inilah yang dinamakan `PULL-REQUEST`. 
  -  `Pull-Request` ini adalah istilah yang bisa kita artikan sebagai permintaan untuk menggabungkan kode. Kita udah membuat perubahan  di repository hasil fork, lalu ingin menggabungkan dengan repository sumber. Maka kita harus membuat Pull Request. Trus, kalau yang punya repo sumber setuju maka bergabunglah codenya. 
      *( Perbaikan : `Pull-request` tidak hanya ketika ingin menggabungkan proyek atao chages yg kita miliki ke orang lain, tetapi misalnya jika kita didalam sebuah repository yg sama, terus ada buat branch yg berbeda, maka sewaktu kita mau menggabungkan branch kita ke master, itu juga kita perlu pull-request, jadi ndak bisa langsung menggabungkan ato merge)

**Kurang lebih kekgini lah Pengimplementasiannya dalam pembuatan repository**
- Pertama aku udah punya akun github dlu lah kan tok:
- Jadi untuk membuat repository online kita, kita klik lah create repository ini dulu :
- Jadi disini tok kubuat repository name nya “Task1”, lalu descriptionnya “Task one with Tok Ivan” :v, (btw nama akun ku username ku kubuat ce318040). Lalu kondisi repositorynya kubuat private tok, biar tak sembarangan orang makek punyakku, nanti ku kasih izin itok ngakses
- Lalu kemudian click button “create repository”, inilah tampilan repo yang kubuat tadi tok. Bisa kita lihat bahwa belum ada disitu folder yang ku upload.
- Nah maka kita akan mencoba mengupload folder dulu (misalnya task ku ini lah kan tok). Sebelumnya aku udah punya Git tok itulah yg kufoto kemaren sama itok, Kemudian aku bukak folder Task yang ingin aku upload, lalu aku klik kanan di sembarang tempat lalu memilih Git Bash, maka tampilannya akan seperti pada gambar dibawah.
- Selanjutnya kita ketikkan command git init untuk menginstalasi bahwa folder task beserta isinya merupakan folder yang akan di kontrol. 
- Lalu selanjutnya kita akan login dulu ke git supaya dapat terhubung ke github. Yaitu menggunakan command : 
    * git config --global user.email “myemail”
    * git config –global user.name “myname”
- Lalu command git add . itu untuk menyimpan keseluruhan file yang ada dalam folder pada repo dan hanya digunakan pada saat upload pertama kali saja.
  (Perbaikan : git add untuk menyimpan changes/perubahan yang terjadi di repo lokal)
- Kemudian kita masuk ke command git commit –m “commit task mia”  untuk menambah keterangan atau status perubahan saat upload ke repo online.
- Kemudian kita lanjut dengan memasukkan command git remote add origin https://github.com/ce318040/Task1.git untuk men-setting remote origin dari repo online, repo online bisa dilihat pada link yang pada repo, ini diperlukan untuk mengakses repo tersebut sehingga kita bisa melakukan apapun di repo online tersebut. 
- Selanjutnya command untuk mengupload file yang ada pada repo lokal dengan command git push –u origin master
- Kemudian kita akan login kea kun github kita
- Dan proses mengupload sudah berhasil




**Perbaikan Tambahan :**
- git init untuk menginisialisasi repo git pada komputer kita
- git add untuk menambahkan file kedalam staging area 
- git status untuk mengetahui status repo kita, apakah ada file baru?, apakah ada file yang berubah? apakah ada file yang di hapus/hilang?
- git commit untuk melakukan commit
- git config untuk masukin konfigurasi ke dalam git
- git branch untuk membuat branch
- git help 

Ketika kita sudah membuat sebuah repo maka git-nya/komputer kita akan mengenali 3 area, yaitu:
1. `Working tree` yang merupakan folder tempat bekerja
2. `Staging area` ini bahwa kita memberitahu ke git bahwa kita sudah melakukan perubahan
3. `History` jika sudah dilakukan perubahan dan sudah di commit maka itu akan masuk ke are history


<b>enter</enter>

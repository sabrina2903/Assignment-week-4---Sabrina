membuat sebuah folder kosong dengan namamu sendiri
: mkdir sabrina
membuat sebuah file di dalam folder tersebut dengan nama README.md, isi file tersebut dengan kalimat
"Halo perkenalkan aku halaman utama"
: echo "Halo perkenalkan aku halaman utama" > README.md  
inisialisasi folder tersebut dengan Git, kemudian simpan perubahan menggunakan commit dengan pesan
"First commit"
: git init 
git add README.md
git commit -m "First commit"
Ganti teks sebelumnya dengan `"Hello world"
: echo "Hello world" > README.md
Tampilkan isi teks tersebut pada command line menggunakan command cat
: cat README.md
Ternyata kamu tidak ingin perubahan tersebut, dan ingin kembali ke perubahan seperti commit yang terakhir. Lakukan teknik git backtracking untuk mengembalikan ke perubahan commit yang terakhir.
: git checkout README.md
buat branch baru dengan nama cv, hal ini berguna agar histori kita tidak tercampur
: git branch cv
pindah branch ke dalam cv, kemudian buat file dengan nama cv.txt dan isi file tersebut dengan kalimat:
"Ini adalah file CV"
: git checkout cv
echo "Ini adalah file CV" > cv.txt
kemudian simpan perubahan menggunakan commit dengan pesan
"Initial CV"
: git add cv.txt
git commit -m "Initial CV"
tambahkan 3 perusahaan yang akan kamu lamar, dan setiap menuliskan 1 nama perusahaan kamu harus melakukan dokumentasi dan menyimpan perubahan menggunakan commit
: echo "PT Samsung" >> cv.txt
git commit -am "menambahkan perusahaan pertama"

echo "Skilvul" >> cv.txt
git commit -am "menambahkan perusahaan kedua"

echo "Google" >> cv.txt
git commit -am "menambahkan perusahaan ketiga"

kembali ke branch master
: git checkout master
ubah file README.md menjadi
Halo perkenalkan aku halaman utama

Ini adalah update pertama pada branch master
jangan lupa untuk menyimpan perubahan menggunakan commit dengan pesan
"update master pertama"
: echo -e "Halo perkenalkan aku halaman utama \n  \n Ini adalah update pertama pada branch master" > README.md
git commit -am "update master pertama"
gabungkan branch cv ke dalam branch master menggunakan perintah git merge
: git merge cv
mengunggah Git Repository project tersebut tersebut ke dalam GitHub
: membuat repository di github, kemudian salin link, dan ketik di git bash
git remote add origin (link repository)
git push -u origin master

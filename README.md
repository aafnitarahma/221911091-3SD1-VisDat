# 221911091-3SD1-VisDat
Segala hal yang berkaitan dengan projek Ujian Akhir Semester 6 Mata Kuliah Visualisasi Data dan Informasi.

> Data untuk visualisasi _side-by-side bar chart_ adalah https://github.com/aafnitarahma/221911091-3SD1-VisDat/blob/main/Data%20Pendidikan%20Provinsi%20Papua%20Kemendikbud%20(2).xlsx 'Sheet2' <br>
> Data untuk pengklasteran kabupaten dengan _R Studio_ adalah https://github.com/aafnitarahma/221911091-3SD1-VisDat/blob/main/Data%20Pendidikan%20Provinsi%20Papua%20Kemendikbud%20(2).xlsx 'Tabel Merge' <br>
> Data untuk pengklasteran kabupaten dengan _Tableau_ adalah https://github.com/aafnitarahma/221911091-3SD1-VisDat/blob/main/File%20SHP%20Sudah%20Gabung%20Data/gadm40_Papua_kab_isi.shp <br>
> Makalah di https://github.com/aafnitarahma/221911091-3SD1-VisDat/blob/main/221911091-3SD1-VisDat.pdf <br>
> Hasil visualisasi diunggah menggunakan _server Tableau Public_, yang dapat diakses di https://public.tableau.com/views/UjianAkhirSemesterUASVisualisasiDatadanInformasi/Dashboard1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link <br>


Proses Pembuatan Visualisasi Data: <br>
1. Setelah mengumpulkan data pendidikan, berupa data Jumlah Sekolah, Jumlah Guru, dan Jumlah Peserta Didik setiap kabupaten di Provinsi Papua (artinya level data sampai kecamatan), dilakukan penggabungan data menjadi satu _dataset_ utuh data pokok pendidikan (DAPODIK) sampai level kecamatan di Provinsi Papua. Selain itu, ketiga data tersebut untuk SMA dan SMK digabungkan, dengan pertimbangan tingkatan pendidikannya sama. Catatan: data pokok pendidikan yang didapatkan per tanggal 9 Juni belum tersinkronisasi sebesar 
2. Data yang diperoleh masih berupa data agregat, untuk itu perlu mengolah data ke bentuk variabel yang diinginkan, yakni Rasio Murid terhadap Guru (Jumlah Murid pada suatu tingkatan pendidikan/Jumlah Guru pada suatu tingkatan pendidikan) dan Rasio Murid terhadap Sekolah (Jumlah Murid pada suatu tingkatan pendidikan/Jumlah Sekolah pada suatu tingkatan pendidikan)
3. Beralih ke data lain, yaitu data geospasial yang diperlukan untuk membuat visualisasi peta. Data ini tersedia sampai level desa, tetapi cakupannya seluruh Indonesia, sehingga perlu dilakukan pemotongan _polygon_ (dalam penelitian ini, proses tersebut menggunakan _QGIS_ 3.16). Catatan: pencarian data geospasial ini sangat sulit, yang akhirnya Saya temukan hanya batas administrasi per tahun 2015, sehingga ketika diperiksa jumlah kecamatan hanya 385 yang seharusnya 576, yang menyebabkan visualisasi tema sampai kecamatan dibatalkan, dan hanya disajikan dalam _side-by-side bar chart_. 
4. Setelah itu, dilakukan _merge_ tabel data pendidikan dan data geospasial (menggunakan _Geoda_) yang nanti akan digunakan sebagai _input_ dalam analisis _cluster_ menggunakan Tableau.
5. Melakukan analisis _cluster_ sekaligus visualisasi dengan _Tableau_, secara bersamaan membandingkan hasil klaster _Tableau_ dan _R Studio_.
6. Menggabungkan visualisasi yang dihasilkan dalam satu _dashboard_ untuk kemudian dipublikasikan.
7. Evaluasi untuk visualisasi ini mungkin ke depannya bisa dikembangkan visualisasi yang _up to date_ otomatis terhadap masukan data baru ke web Kemendikbud (ada sinkronisasi baru), pemetaan hasil klaster sampai tingkat kecamatan jika bisa didapatkan shp kecamatan di Provinsi Papua secara lengkap, serta penggunaan data yang lebih lengkap untuk visualisasinya--sehingga semua daerah diketahui kondisinya, tidak ada yang ditinggalkan.

# SIG-Teori-Modul7-RasterMosaicingandClipping

## Data
[N05E080.SRTMGL1.hgt.zip](https://www.qgistutorials.com/downloads/N05E080.SRTMGL1.hgt.zip)

[N06E079.SRTMGL1.hgt.zip](https://www.qgistutorials.com/downloads/N06E079.SRTMGL1.hgt.zip)

[N06E080.SRTMGL1.hgt.zip](https://www.qgistutorials.com/downloads/N06E080.SRTMGL1.hgt.zip)

[N06E081.SRTMGL1.hgt.zip](https://www.qgistutorials.com/downloads/N06E081.SRTMGL1.hgt.zip)

[N07E079.SRTMGL1.hgt.zip](https://www.qgistutorials.com/downloads/N07E079.SRTMGL1.hgt.zip)

[N07E080.SRTMGL1.hgt.zip](https://www.qgistutorials.com/downloads/N07E080.SRTMGL1.hgt.zip)

[N07E081.SRTMGL1.hgt.zip](https://www.qgistutorials.com/downloads/N07E081.SRTMGL1.hgt.zip)

[N08E079.SRTMGL1.hgt.zip](https://www.qgistutorials.com/downloads/N08E079.SRTMGL1.hgt.zip)

[N08E080.SRTMGL1.hgt.zip](https://www.qgistutorials.com/downloads/N08E080.SRTMGL1.hgt.zip)

[N08E081.SRTMGL1.hgt.zip](https://www.qgistutorials.com/downloads/N08E081.SRTMGL1.hgt.zip)

[N09E080.SRTMGL1.hgt.zip](https://www.qgistutorials.com/downloads/N09E080.SRTMGL1.hgt.zip)

[ne_10m_admin_0_countries.zip](https://www.qgistutorials.com/downloads/ne_10m_admin_0_countries.zip)

## Prosedur

1. Buka QGIS dan cari file yang diunduh di panel Browser . Perluas file zip individual untuk menampilkan .hgtfile. Tahan Ctrltombol dan pilih semua file individual. Setelah dipilih, seret ke kanvas.
2. Anda akan melihat 11 lapisan individu dimuat di panel Lapisan dan ditampilkan di kanvas. Kami akan menggabungkan ubin individu ini menjadi satu mosaik. Pergi ke Memproses ‣ Kotak Alat. 
3. Cari dan temukan alat GDAL ‣ Raster aneka ‣ Gabung . Klik dua kali untuk meluncurkannya.
4. Dalam dialog Gabung , klik tombol … di sebelah Lapisan masukan . Klik Select All untuk memilih semua layer individual.
5. Seperti disebutkan dalam rincian lapisan dataset , tipe data masukan adalah bilangan bulat bertanda 16-bit . Untuk menjaga integritas data, kita harus menyimpan tipe data yang sama untuk layer gabungan. Pilih Int16sebagai tipe data Keluaran . Juga format data keluaran default adalah GeoTiff. File GeoTiff bisa menjadi sangat besar jika tidak dikompresi. Pilih sebagai Profil . Klik Jalankan .High Compression.
6. Setelah pemrosesan selesai, layer baru OUTPUTakan ditambahkan ke panel Layers . Jika lapisan tidak berada di bagian atas tumpukan, pilih dan seret ke bagian atas panel Lapisan .
7. Anda akan melihat bahwa OUTPUTlapisan berisi data elevasi gabungan dari ubin masukan individual. Visualisasi default hanya menampilkan nilai piksel dalam kisaran 0-255. Namun data kami berisi piksel dengan nilai -14 hingga 2371, menghasilkan rendering kontras yang rendah. Mari kita ubah menjadi visualisasi yang lebih baik. Klik tombol Open the layer Styling panel di panel Layers .
8. Di panel Layer Styling , klik dropdown Render type dan pilih Hillshaderenderer. Opsi rendering ini sangat cocok untuk data elevasi.
9. Operasi umum lainnya saat bekerja dengan raster adalah dengan memotong raster ke area yang Anda minati. Untuk tutorial ini, kami akan mengklip layer gabungan ke batas negara untuk Sri Lanka. Temukan ne_10m_admin_0_countries.zipfile yang diunduh dan perluas. Seret ne_10m_admin_0_countries.shpfile ke kanvas.
10. ne_10m_admin_0_countriesPilih layer yang baru ditambahkan di panel Layers . Klik tombol Select Features by area atau satu klik pada Attributes Toolbar . Setelah dipilih, klik poligon untuk Sri Lanka untuk memilihnya.
11. Tetap pilih apa adanya dan buka Processing ‣ Toolbox . Cari dan temukan GDAL ‣ Ekstraksi raster ‣ Klip raster dengan alat lapisan topeng. Klik dua kali untuk meluncurkannya.
12. Dalam dialog Clip Raster by Mask Layer , tetapkan OUTPUTsebagai Input Layer . Pilih ne_10m_admin_0_countriessebagai layer Mask , dan centang kotak Selected features only . Masukkan 0.0000sebagai Menetapkan nilai nodata yang ditentukan ke band keluaran . Seperti sebelumnya, pilih sebagai Profile . Klik Jalankan .High compression,
13. Layer baru OUTPUTakan ditambahkan ke panel Layers . Pada titik ini, mungkin sulit untuk melihat hasilnya karena kita memiliki terlalu banyak lapisan tumpang tindih yang terlihat. Klik tombol Kelola Tema Peta di panel Lapisan dan pilih .Hide All Layers.
14. Nyalakan hanya OUTPUTlayer terbaru dan beri gaya dengan Hilshadeperender seperti yang dilakukan sebelumnya.
15. Lapisan elevasi keluaran gabungan dan subset untuk Sri Lanka sudah siap.
16. selesai.







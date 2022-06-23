# **Final Project**

**Data Rangers**

Final project purwadhika.

Mengelola dan membuat pemodelan dari data yang sudah diberikan, data yang akan digunakan adalah data Used Cars in Belarus.

sumber data : UsedCarsBelarus

**Contents**

Business Problem Understanding
Data Understanding
Data Wrangling
EDA
Data Preprocessing
Modeling
Conclusion
Recommendation

## **Business Problem Understanding**

**Context**

Kami adalah sebuah perusahaan yang bergerak dalam bidang penjualan mobil bekas yang berada di Belarus. Pada saat ini perkembangan teknologi yang sudah maju, tentunya kami memasarkan produk (dalam hal ini mobil bekas) melalui internet atau online yang dijalankan oleh divisi sales penjualan atau marketing. Dan pada Dewasa ini, moda transportasi sangat dibutuhkan oleh semua kalangan, mulai dari transportasi umum hingga kendaraan pribadi. Alasan yang paling mendasar adalah untuk kebutuhan mobilitas. Namun dari semua jenis moda transportasi, kendaraan bermotor seperti mobil adalah jenis moda transportasi yang memiliki permintaan tinggi dan banyak dari kalangan menengah keatas yang mempunyai permintaan tinggi terhadap kebutuhan mobil pribadi sebagai moda transportasi karena alasan fleksibilitas.

Namun harga beli mobil baru menjadi permasalahan setiap individu karena mempunyai harga yang relatif tinggi serta memiliki depresiasi harga yang selalu naik untuk setiap tahunnya meskipun fitur yang dimiliki hampir sama dengan keluaran terbarunya, oleh karena itu banyak permintaan atau peminat akan mobil bekas yang memiliki kondisi masih bagus untuk dijadikan pilihan sebagai kendaraan pribadi, dari berbagai alasan tersebut, peluang bisnis pun muncul sehingga banyak para penyedia jasa layanan jual beli mobil bekas, mulai dari pedagang mobil, makelar mobil/broker hingga ke perusahaan yang menyediakan layanan platform jual beli mobil bekas seperti kami dan seiring berjalannya waktu mereka pun memasarkannya juga secara online.

Dari banyaknya layanan jual beli mobil bekas yang akan memasarkan setiap unit mobil yang dimiliki ke bursa pasar secara online, tentunya kami membutuhkan sebuah keputusan untuk dapat menentukan harga jual mobil yang kompetitif atau dalam artian memberikan harga yang ideal sesuai dengan kondisi mobil sehingga dapat menarik calon pembeli serta perusahaan membutuhkan analisa mengenai stok yang sudah dimiliki agar kedepannya sesuai dengan permintaan bursa pasar mobil bekas.


## **Business Process**

**Bisnis Proses**
Pada pengerjaan proyek ini, kami akan menjelaskan mengenai alur dari proses bisnsi perusahaan dalam penjualan mobil bekas.

![image.png](attachment:73faa252-ad20-426c-9d89-b12f1d43581f.png)

## **Problem Statement**

Salah satu tantangan terbesar bagi kami sebagai layanan platform jual beli mobil secara online adalah pemecahan masalah untuk dapat memiliki model bisnis yang menguntungkan secara finansial bagi perusahaan dalam hal menggantinkan COGS yang mana proses awalnya dilakukan secara manual.

Dalam memberikan harga yang ideal, tentunya perusahaan harus memiliki tim yang ahli dalam menentukan harga jual mobil yang sudah ada agar perusahaan mendapatkan profit, seperti stok mobil yang berada didalam gudang, namun harus membutuhkan SDM yang banyak dan itu akan menimbulkan biaya operasional yang tinggi apabila jumlah stok mobil melimpah. Sedangkan alur yang harus dilakukan adalah, melakukan kunjungan atau inspeksi langsung terhadap stok mobil yang sudah ada, lalu dilakukannya pengecekan kepada setiap unit yang ada, setelah itu keluarlah biaya modal (COGS), kemudian perusahaan baru dapat bisa melakukan penentuan penawaran harga jual mobil kepada calon customer yang nantinya akan ditawarkan langsung oleh sales penjualan.

Mengingat bahwa harga penawaran harus ideal, untuk menentukan harga jual mobil pun dengan memberikan petunjuk minimal yang memungkinkan untuk menawarkan unit mobil dengan membandingkan kompetitor di lingkungan mereka untuk mendapatkan harga yang kompetitif sangatlah penting. Sales dari perusahaan layanan pun dapat memasukkan harga yang lebih tinggi untuk fitur/jenis mobil apa pun yang mereka anggap perlu, namun hal tersebut juga akan memakan waktu dan biaya operasional yang tinggi apabila stok yang dimiliki sangat banyak misalkan stok yang masuk melebihi 50 unit, maka dari permasalahan yang ada, kami akan membuat sebuah pemodelan untuk menentukan harga jual yang ideal agar dapat memangkas waktu serta perusahaan dapat menentukan harga yang ideal/kompetitif dengan cost operasional yang rendah. **Dengan bertambahnya layanan jual beli mobil yang ada, untuk menentukan harga yang tepat untuk dapat tetap kompetitif sangatlah penting**.

Dalam menentukan harga mobil bekas pun juga harus melalui beberapa tahap, contohnya seperti :

1. Tahun pembuatan mobil
2. Kondisi Mobil
3. Harga pesaing

Dari ke 3 faktor diatas, permasalahan yang paling mendasar adalah tahun pembuatan dan kondisi dari mobil bekas. 

[sumber informasi](https://www.otoloka.id/tips-and-trick/bingung-menentukan-harga-jual-mobil-bekas-ini-caranya-169401)

## **Goals**
Berdasarkan permasalahan tersebut, tim sales penjualan di perusahaan dapat **menentukan harga jual yang tepat untuk tiap unit mobil** serta **melakukan efisiensi pekerjaan dari proses penentuan `COGS` secara manual menjadi machine learning.** Sehingga apabila jumlah stok mobil yang datang melebihi kapasitas dari SDM yang dimiliki, perusahaan akan menghemat cost yang dikeluarkan untuk menambah jumlah pegawai karena dalam penentuan COGS sudah digantikan dengan machine learning.

## **Business Question**
Dalam pengerjaan proyek ini, ada beberapa business question yang akan kami tangani, yaitu :

**Business Question For EDA**

1. Jumlah stok mobil berdasarkan brand produsen mobil (10 teratas).
2. Berapa nilai median harga dari produsen mobil dengan stok unit terbanyak?
3. Bagaimana perbandingan antara harga distribusi mobil dengan kondisi "with damage" & "with mileage"?
4. Bagaimana pengaruh tahun produksi terhadap harga jual mobil?
5. Perbandingan distribusi harga unit mobil berdasarkan dari jenis bahan bakar mobil.
6. Berapa persen dari keseluruhan stok mobil yang menggunakan transmisi manual dan transmisi otomatis?
7. Jumlah stok mobil berdasarkan warna
8. Perbandingan harga jual mobil berdasarkan warna

**Business Question For For Machine Learning**
- Bagaimana proyeksi dari model yang telah dibuat dan pengaruhnya terhadap perusahaan?
- Kapan machine learning akan digunakan?

**Analytics Approach**
Jadi, yang perlu kami lakukan adalah menganalisis data untuk dapat menemukan pola dari fitur-fitur yang ada, yang membedakan tipe unit mobil dengan tipe yang lainnya. 

Selanjutnya, kami akan membangun suatu model regresi yang akan membantu sales dari layanan jual beli mobil untuk dapat menyediakan 'tool' prediksi harga jual yang ideal, yang mana akan berguna untuk tim sales penjualan layanan jual beli mobil dalam menentukan harga jual listing-nya dan tim pengadaan barang (mobil) untuk menentukan margin harga beli mobil.

**Project Limitation**
Evaluasi metrik yang akan digunakan adalah RMSE, MSE, dan MAE, di mana RMSE adalah nilai rataan akar kuadrat dari error, MSE adalah selisih antara nilai target output dengan nilai actual output, MAE adalah rataan nilai absolut dari error yang dihasilkan oleh model regresi. Semakin kecil nilai RMSE, MAE, yang dihasilkan, berarti model semakin akurat dalam memprediksi harga jual sesuai dengan limitasi fitur yang digunakan. 

**Deskripsi Isi Data**

Berikut adalah deskripsi dari isi data yang akan di analisa 


| **Attribute** | **Description** |
| --- | --- |
| make | Machine Firm |
| model | Model of car |
| priceUSD | Price in USD |
| year | Production Year |
| condition | Represents the condition at the sale moment |
| mileage(kilometers) | Mileage in kilometers |
| fuel_type | Type of the fuel (electro, petrol, diesel) |
| volume(cm3) | Volume of the engine |
| color | Color of Car |
| transmission | Transmission of Car |
| drive_unit | Type of drive unit |
| segment | segment (this feature was collected manually, so it could be wrong) |

<br>

## **Explanatory Data Analyst**

1. Jumlah Stok Mobil Berdasarkan Brand Produsen Mobil (10 teratas)
![image.png](attachment:8bb931d8-bd7c-4b93-a08d-699bb0def8ad.png)
Dari data yang telah kami dapatkan, kami telah mendapatkan insight mengenai jumlah stok mobil bekas dari perusahaan

Insight :
- Dari stok yang dimiliki, terdapat 10 produsen dengan jumlah stok terbanyak di perusahaan, yaitu 
    1. Volkswagen
    2. Audi
    3. BMW
    4. Opel
    5. Renault
    6. Mercedes-Benz
    7. Ford
    8. Peugot
    9. Nissan
    10. Toyota
- Stok mobil terbanyak yaitu dari produsen volkswagen dengan stok sebanyak 6.802
- Stok mobil dengan jumlah paling rendah atau sedikit yaitu toyota sebanyak 2.168

dan dari mengutip dari laman [focus2move](https://www.focus2move.com/belarus-auto-market/) bahwa pengguna mobil dibelarus memilih produsen mobil dari :
   1. Renault 
   2. Lada Vasta
   3. Volkswagen
   4. Nissan
   5. Skoda
   6. Kia
   7. Hyundai
   
Recomendation :
- Ada beberapa merk yang masih kurang diminati oleh para pengguna mobil namun stok yang kami miliki masih banyak, sehingga perlu dilakukan promosi.
- Perusahaan memfokuskan stok mobil sesuai dengan pangsa pasar yang ada, yaitu dari ke 7 brand produsen mobil yang sudah disebutkan diatas agar stok yang dimiliki sesuai dengan permintaan pangsa pasar di belarus

Action : 
- Mengoptimalkan penjualan dari stok yang sudah dimiliki oleh tim sales
- Pengadaan barang baru dengan stok mobil dari produsen yang diminati di bursa pasar mobil bekas belarus


2. Berapa Nilai Median Harga Dari Produsen Mobil Dengan Stok Terbanyak 
![image.png](attachment:9843729b-8917-4ee5-9a06-45893e0cfe3a.png)

Insight
- Mengutip dari laman [ceicdata.com](https://www.ceicdata.com/id/indicator/belarus/gdp-per-capita) rata-rata pendapatan perkapita di Belarus 6.698 per tahunnya, sedangkan tidak seluruh pendapatan digunakan untuk membeli mobil yang merupakan kebutuhan sekunder. Namun dapat terlihat dari grafik di atas masih terdapat beberapa stok yang median harganya masih di atas rata-rata pendapatan perkapita di Belarus.

Recomendation:
- Karena pembelian mobil mewah sangat jarang dan hanya beberapa orang saja yang membeli, sebaiknya perusahaan lebih mengincar mangsa pasar yang kelas menengah saja.

Action:
- Tidak perlu menambahkan stok stok mobil yang termasuk ke mobil kelas mewah, dan perlu melakukan tambahan riset mengenai perkembangan tren merk produsen tiap tahunnya untuk mobil kelas menengah yang harganya di bawah 6.698 sehingga lebih efisien untuk penambahan stok ke depan. 

3. Bagaimana perbandingan antara harga distribusi mobil dengan kondisi "with damage" & "with mileage"
![image.png](attachment:8337bb48-ba6f-4ef2-baf9-b0f131dc5c3f.png)

- Insight
 Berdasarkan hasil analisa diatas, untuk fitur kondisi menunjukan adanya pengaruh untuk kondisi "with mileage" adalah kondisi mobil bekas dengan kondisi normal terdapat perbedaan harga, yaitu kondisi "with mileage" memiliki harga yang lebih tinggi (100 USD -200000 USD), dibandingkan dengan kondisi "with damage" dengan rentang harga (100 USD - 25000 USD)
- Recomendiation
 Dari hasil analisa yang diperoleh, perusahaan harus cermat dalam memilih kendaraan yang akan langsung dijual serta memilah jenis kendaraan yang rusak (with damage).
- action
Dari hasil rekemondasi yang kami peroleh, maka perusahaan sebaiknya melakukan treatmen atau perawatan atau servis sesuai dengan kondisi mobil sehingga perusahaan dapat menjual dalam keadaan normal dan menghasilkan profit yang lebih tinggi

4. Bagaimana pengaruh tahun produksi terhadap harga jual mobil (berdasarkan dari data tahun produksi 1980)
![image.png](attachment:89e3cbe5-6bf0-4244-8ada-2845fdc4f051.png)

- Insight :
Dari hasil yang kami dapatkan, grafik menunjukan adanya pengaruh tahun terhadap distribusi harga jual, dimana apabila tahun produksi mobil semakin muda maka harga nya semakin bervariasi.
- Recomendation :
Perusahaan perlu melakukan sortir atau pemilihan jenis mobil dengan cermat apabila mendapatkan mobil dengan tahun produksi yang masih muda, karena harga nya bervariasi ditakutkan terjadinya miss dalam penentuan harga
- Action :
Perusahaan perlu memiliki sebuah model atau `tools` yang membantu untuk menentukan harga jual dengan risiko kesalahan penentuan harga yang rendah seperti machine learning

5. Perbandingan distribusi harga unit mobil berdasarkan dari jenis bahan bakar mobil
![image.png](attachment:9f0d8beb-4a93-4a7d-b19a-c61f137d5956.png)

![image.png](attachment:75bcc436-6cf3-46d8-b78a-baea5482e690.png)

Dari data yang sudah kami dapatkan, kami mendapatkan informasi mengenai perbandingan distribusi harga unit mobil dengan mengelompokan jenis bahan bakar yang digunakan yaitu petrol dan diesel.

Insight :
- Jenis bahan bakar petrol memiliki rentang distribusi harga dari 95 USD - 235235 USD
- Jenis bahan bakar diesel memiliki rentang distribusi harga dari 150 USD - 111690 USD
- Persentase ketersediaan unit stok untuk jenis bahan bakar petrol sebesar 64.55%
- Persentase ketersediaan unit stok untuk jenis bahan bakar diesel sebesar 35.45%

dan kami mendapatkan sumber berita yang menyatakan bahwa mobil diesel lebih diminati oleh banyak calon pengguna, karena mobil dengan tipe bahan bakar diesel dari segi perawatan lebih mudah dan dari segi konsumsi bahan bakarnya lebih irit atau efisien.

source [bensin kita](https://bensinkita.com/mobil-diesel-versus-mobil-bensin-mana-yang-lebih-enak-dan-irit/)

Recomendation :

Dari hasil analisis dari insight diatas, kami merekomendasikan untuk perusahaan menyeimbangkan jumlah stok dari unit berjenis bahan bakar diesel dengan petrol agar sesuai target market.

Action :

- Untuk divisi tim pengadaan barang menambahkan stok untuk unit mobil dengan jenis bahan bakar diesel dan tidak menambahkan stok mobil dengan jenis bahan bakar petrol atau dalam artian sesuai dengan kebutuhan permintaan pasar. Dan perusahaan harus menyeimbangkan jumlah stok antara mobil dengan jenis bahan bakar petrol dan diesel agar konsumen atau peminat mobil diesel dapat diserap transaksinya melalui perusahaan kami agar perputaran keuangan di perusahaan lebih tinggi.

6. Berapa persen dari keseluruhan stok mobil yang menggunakan transmisi manual dan transmisi otomatis?
![image.png](attachment:99a7f3b4-13ff-4bb1-beb1-81e07328b92a.png)

![image.png](attachment:15294073-09f1-40c2-ba03-7113f5f431dc.png)

![image.png](attachment:161cf46a-9e77-45e1-bfa9-62b8d3ed8798.png)

Dari data yang telah kami dapatkan, kami mendapatkan data mengenai jumlah persentase dari pengguna mobil dengan transmisi manual dan transmisi matic.

Insight :

- Jenis mobil dengan transmisi otomatis memiliki distribusi harga dari  224 USD - 235235 USD 
- Jenis mobil dengan transmisi manual / mehcanics memiliki distribusi harga dari 95 USD - 80000 USD
- Stok mobil dengan jenis transmisi otomatis sebanyak 36.25%
- Stok mobil dengan jenis transmisi manual sebanyak 63.75% 

Recomendation : 

Dari hasil insight yang kami dapatkan, perusahaan harus meningkatkan jumlah unit mobil dengan jenis transmisi otomatis karena mengutip dari laman [otomoti](https://otomotif.tempo.co/read/1382401/data-pengemudi-semakin-banyak-beralih-ke-mobil-matik) banyak pengguna mobil yang beralih ke jenis transmisi otomatis.

Action :

Perusahaan dalam pengadaan barangnya pada nantinya sebaiknya beralih ke jenis transmisi mobil otomatis agar sesuai dengan kebutuhan pasar yang mampu mendongkrak profit.

7. Jumlah stok mobil berdasarkan warna 
![image.png](attachment:3dc77111-5650-460b-ad12-095e65b4b92b.png)

Dari data yang telah kami peroleh, kami mendapatkan data mengenai jumlah stok unit mobil berdasarkan dari warna mobil

Insight :
- Stok terbanyak dari data yang kami dapatkan yaitu berwarna Hitam diikuti dengan warna silver dan biru
- Stok mobil dengan warna paling sedikit adalah warna oranye, kuning dan ungu

Recomendation :
Dari total jumlah unit mobil yang ada dan mengutip laman dari [garasi.id](https://garasi.id/artikel/10-warna-mobil-bekas-paling-laku-dan-paling-aman-dikendarai/5b7e58daef465d01f03faa57) kami merekomendasikan untuk perusahaan menjual mobil dengan warna - warna yang menjadi pilihan favorit semua orang.
contoh warna mobil yang menjadi favorit pengguna mobil dari laman yang telah kamu kutip adalah :
- Putih
- kuning
- Silver

Action :
- Untuk saat ini perusahaan diusahakan untuk menghabiskan stok dengan warna yang kurang diminati
- Mengoptimalkan jumlah mobil dengan warna yang diminati oleh banyak pengguna mobil

8. Perbandingan harga jual mobil berdasarkan warna
![image.png](attachment:4d65b564-6813-40dd-ad2b-0440ddfc0fa3.png)

Dari data yang telah kami dapatkan, kami telah mendapatkan distribusi harga mobil berdasarkan warna.

Insight :
- Warna putih adalah warna mobil dengan penjualan dengan sebaran harga tertinggi
- Warna oranye adalah warna mobil dengan penjualan dengan sebaran harga terendah

Recomendation : 

perusahaan harus mengoptimalkan penjualan dengan memperhatikan jenis warna yang banyak diminati karna mempengaruhi minat pelanggan.

Action : 
- Menaikan jumlah stok mobil dengan warna yang paling diminati
- mengurangi jumlah stok mobil dengan warna yang kurang diminati
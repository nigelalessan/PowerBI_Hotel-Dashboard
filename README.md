
# Power BI - Hotel Dashboard Project

## :scroll: Overview

Project ini mengeksplorasi data mengenai Atliq Hotel di India untuk memberikan wawasan, terutama pada sektor pendapatan. Dengan memperoleh wawasan berdasarkan data tersebut diharapkan dapat membantu dalam membuat keputusan strategis yang berguna dalam meningkatkan kualitas dari akomodasi tersebut terutama pada sektor pendapatan.

![Image Full Dashboard](https://github.com/nigelalessan/PowerBI_Hotel-Dashboard/blob/595ef53b989e866627fd0267bc506d4e4b1215d0/Power-BI%20Images/Screenshot%202025-01-06%20082505.jpg)


## :dart: Goals

 - Mengetahui Revenue, Revenue Per Available Room (RevPAR), Daily Sellable Room Night (DSRN), Realization %, Occupancy % dalam bentuk KPI.
 - Mengetahui pendapatan berdasarkan kategori (Revenue by Category) menggunakan visualisasi Donut Chart.
 - Mengetahui pendapatan berdasarkan ruang yang tersedia (RevPAR by Month and Week) menggunakan visualisasi Line Chart.
 - Mengetahui presentase ruangan yang dihuni berdasarkan kota (Occupancy % by City) menggunakan visualisasi Stacked Bar Chart.
 - Menampilkan tabel data dengan menambahkan conditional formatting data bar
 - Mengetahui Realization percentage dan ADR berdasarkan booking platform (Realization % and ADR Booking Platform)
 - Menambahkan filter
## :page_facing_up: Data/Table Description

![Image Table](https://github.com/nigelalessan/PowerBI_Hotel-Dashboard/blob/595ef53b989e866627fd0267bc506d4e4b1215d0/Power-BI%20Images/Data%20Model.jpg)

- Relation

        dim_date.date = fact_bookings.check_in_date  
        dim_date.date = fact_aggregated_bookings.check_in_date  
        dim_rooms.room_id = fact_bookings.room_category  

- fact_bookings
Tabel ini merupakan fact table yang berisi mengenai booking_date (tanggal booking), booking_id (booking id), booking_platform (platform yang digunakan untuk booking), booking_status (status booking), check_in_date (tanggal check in), checkout_date (tanggal check out), no_guests (jumlah tamu yang menginap), property_id (id properti), ratings_given (rating yang diberikan), revenue_generated (pendapatan yang dihasilkan dari pelanggan tertentu), revenue_realized (pendapatan akhir yang masuk ke dalam hotel), room_category (kategori ruangan)
- fact_aggregated_bookings
Tabel ini merupakan fact table yang berisi mengenai capacity (kapasitas), check_in_date (tanggal check in), property_id (id properti), room_category (kategori ruangan), successful_bookings (booking yang berhasil)
- dim_date
Tabel ini merupakan dimension table yang berisi mengenai date (tanggal), day_type (weekday atau weekend), Filter_Week (Digunakan untuk filter mingguan), mmm yy (Format tanggal per bulan), week_n (minggu ke-)
- dim_rooms
Tabel ini merupakan dimmension table yang berisi mengenai room_class (kategori ruangan), room_id (id ruangan)
- dim_hotel
Table ini merupakan dimmension table yang berisi mengenai category (kategori), city (kota), property_id (id properti), property_name (nama properti)


## :bar_chart: Visualization

- ### Title 

<img src="https://github.com/nigelalessan/PowerBI_Hotel-Dashboard/blob/595ef53b989e866627fd0267bc506d4e4b1215d0/Power-BI%20Images/Title.jpg" width="800px">

Terdapat title pada dashboard untuk menunjukkan garis besar mengenai dashboard yang dibuat tersebut berupa judul.

- ### Filter by Month and Week

<img src="https://github.com/nigelalessan/PowerBI_Hotel-Dashboard/blob/595ef53b989e866627fd0267bc506d4e4b1215d0/Power-BI%20Images/Month%20and%20week%20filter.jpg" width="800px">

Filter diatas merupakan filter bulan dan minggu, nantinya data yang kita inginkan bisa diatur berdasarkan bulan dan minggu. Dalam filter tersebut hanya terdapat 3 bulan saja di tahun 2022, yaitu Mei, Juni, Juli dan untuk minggu hanya dari minggu 19 sampai minggu ke 31, karena data hanya sebatas tanggal tersebut saja.

- ### Filter

<img src="https://github.com/nigelalessan/PowerBI_Hotel-Dashboard/blob/595ef53b989e866627fd0267bc506d4e4b1215d0/Power-BI%20Images/Filter.jpg" height="400px">

Filter diatas merupakan filter berdasarkan kota (Filter by City), filtet berdasarkan kategori kamar (Filter by Room Categories), filter berdasarkan nama properti (Filter by Property Names). Data akan dapat difilter berdasarkan filter yang tersedia tersebut.

- ### KPI

<img src="https://github.com/nigelalessan/PowerBI_Hotel-Dashboard/blob/bb8c8936784dc60229f81c9a9d03ac5d97d84db9/Power-BI%20Images/KPI.jpg" width="800px">

Kumpulan visualisasi kartu diatas merupakan KPI yang terdiri dari Revenue, RevPAR, ADR, DSRN, Realization %, Occupancy %. Revenue disini merupakan jumlah pendapatan yang diperoleh dari hotel tersebut, kemudian untuk RevPAR merupakan pendapatan yang diperoleh berdasarkan kamar yang tersedia, kemudian ADR (Average Daily Rate) yang merupakan rasio pendapatan dengan total kamar yang telah dibooking atau terjual untuk mengukur rata-rata kamar yang dibayar berdasarkan periode tertentu, kemudian DSRN (Daily Sellable Room Nights) merupakan rata-rata kamar yang bisa di booking/dijual dalam sehari dalam periode tertentu, kemudian Realization % yang merupakan presentase checked out success terhadap seluruh booking yang terjadi, kemudian Occupancy % merupakan booking yang success terhadap total kamar yang tersedia atau kapasitas yang tersedia.

- ### Revenue % by Category

<img src="https://github.com/nigelalessan/PowerBI_Hotel-Dashboard/blob/ef9f50fc092645eb8dcfda7173c371e6f4a04778/Power-BI%20Images/Revenue%20Category.jpg" width="300px">

Visualisasi Donut diatas merupakan mengukur metric presentase pendapatan berdasarkan kategori kamar yang di booking.

- ###  RevPAR by Month and Week

<img src="https://github.com/nigelalessan/PowerBI_Hotel-Dashboard/blob/ef9f50fc092645eb8dcfda7173c371e6f4a04778/Power-BI%20Images/RevPAR%20by%20Month%20and%20Week.jpg" width="300px">

Visualisasi Line Chart diatas merupakan RevPAR by Month and Week, jadi pendapatan yang diperoleh dari kamar yang tersedia berdasarkan bulan dan minggu. Terdapat juga ADR dan Occupancy % sebagain elemen pendukung

- ### Occupancy % by City

<img src="https://github.com/nigelalessan/PowerBI_Hotel-Dashboard/blob/ef9f50fc092645eb8dcfda7173c371e6f4a04778/Power-BI%20Images/Occupancy%20by%20City.jpg" width="300px">

Visualisasi Bar Chart diatas merupakan Occupancy % by City, jadi tingkat presentase Occupancy hotel berdasarkan kota.

- ### Data Table

<img src="https://github.com/nigelalessan/PowerBI_Hotel-Dashboard/blob/ef9f50fc092645eb8dcfda7173c371e6f4a04778/Power-BI%20Images/Data%20Table.jpg" width="600px">

Visualisasi Tabel diatas menampilkan data lengkap dari hotel-hotel Atliq yang tersebar di beberapa kota di India mulai dari property_id, property_name, city, Revenue, RevPAR, Occupancy %, ADR, DSRN, DBRN, DURN, Realization %, Cancellation %, Average Rating.

- ### Realization % and ADR by Platform

<img src="https://github.com/nigelalessan/PowerBI_Hotel-Dashboard/blob/ef9f50fc092645eb8dcfda7173c371e6f4a04778/Power-BI%20Images/Realization%20and%20ADR%20by%20Platform.jpg" width="300px">

Visualisasi Line and Stacked Column Chart diatas merupakan visualisasi dari pengukuran Realization % yaitu persentase checked out sukses dari semua booking yang terjadi dan ADR yang merupakan rasio pendapatan dari jumlah kamar yang telah di booking atau sudah terjual yang mengukur rata-rata pendapatan dari ruangan yang telah terjual pada periode tertentu.

 

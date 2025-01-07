
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

Relation

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


## :bar_chart: Reports

- ![Image Title](https://github.com/nigelalessan/PowerBI_Hotel-Dashboard/blob/595ef53b989e866627fd0267bc506d4e4b1215d0/Power-BI%20Images/Title.jpg)

Terdapat title pada dashboard untuk menunjukkan garis besar mengenai dashboard yang dibuat tersebut berupa judul.

- ![Image Month and Week Filter](https://github.com/nigelalessan/PowerBI_Hotel-Dashboard/blob/595ef53b989e866627fd0267bc506d4e4b1215d0/Power-BI%20Images/Month%20and%20week%20filter.jpg)

Filter diatas merupakan filter bulan dan minggu, nantinya data yang kita inginkan bisa diatur berdasarkan bulan dan minggu. Dalam filter tersebut hanya terdapat 3 bulan saja di tahun 2022, yaitu Mei, Juni, Juli dan untuk minggu hanya dari minggu 19 sampai minggu ke 31, karena data hanya sebatas tanggal tersebut saja.

- <img src="https://github.com/nigelalessan/PowerBI_Hotel-Dashboard/blob/bb8c8936784dc60229f81c9a9d03ac5d97d84db9/Power-BI%20Images/KPI.jpg" width="800px">

Filter diatas merupakan filter berdasarkan kota (Filter by City), filtet berdasarkan kategori ruangan (Filter by Room Categories), filter berdasarkan nama properti (Filter by Property Names). Data akan dapat difilter berdasarkan filter yang tersedia tersebut.


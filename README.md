# Attendance-System-Using-Face-Recognition-LBPH_Flask
***Created By Ahmad Maruf Firman***

![meh](https://user-images.githubusercontent.com/35483191/204142816-92bc8e58-c2f1-4b5d-9b04-4f9351453d5d.jpeg)

Program ini dapat jalan di Python 3.9-3.8-3.7

Using  : 
> XAMPP, Pycharm, Python Libraries 

# Add "flask_db" 
* copy script SQL di bawah ini untuk membuat tabel master personil prs_mstr dan tabel image dataset img_dataset

```
CREATE TABLE `img_dataset` (
  `img_id` int(11) NOT NULL,
  `img_person` varchar(3) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
 
CREATE TABLE `prs_mstr` (
  `prs_nbr` varchar(3) NOT NULL,
  `prs_name` varchar(50) NOT NULL,
  `prs_skill` varchar(30) NOT NULL,
  `prs_active` varchar(1) NOT NULL DEFAULT 'Y',
  `prs_added` datetime NOT NULL DEFAULT CURRENT_TIMESTAMP
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
 
ALTER TABLE `img_dataset`
  ADD PRIMARY KEY (`img_id`);
 
ALTER TABLE `prs_mstr`
  ADD PRIMARY KEY (`prs_nbr`);
```

* Tambah tabel baru dengan nama accs_hist (access history) sebagai tabel untuk menyimpan data personil yang masuk. 
Copy script SQL di bawah ini ke menu flask_db
```
 CREATE TABLE `accs_hist` (
  `accs_id` int(11) NOT NULL AUTO_INCREMENT,
  `accs_date` date NOT NULL,
  `accs_prsn` varchar(3) NOT NULL,
  `accs_added` datetime NOT NULL DEFAULT CURRENT_TIMESTAMP,
  PRIMARY KEY (`accs_id`),
  KEY `accs_date` (`accs_date`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1; 
```
![flask_db](https://user-images.githubusercontent.com/35483191/204143051-9924c020-6dcc-433a-b5a1-7c57369c81dd.PNG)

# Add This Library in Pycharm

>1. flask
>2. mysql-connector
>3. opencv-python
>4. opencv-contrib-python
>5. pillow

apabila telah berhasil maka hasilnya akan seperti ini :
![libraries](https://user-images.githubusercontent.com/35483191/204143800-6a561e3b-c23b-4da3-8bcb-945260d7776e.PNG)
- [x] **Done**

# Run Program 
* Jalankan XAMPP phpmyadmin dan file main.py di Pycharm. Lalu klik link localhost dibawah ini 

![run main](https://user-images.githubusercontent.com/35483191/204182998-8e2f797b-2c48-48fe-bfb2-fc6f10eb5ed4.png)

* Setelah klik link maka akan muncul homepage seperti dibawah ini

![homepage](https://user-images.githubusercontent.com/35483191/204183303-c0b7e665-2a48-49f9-bcb9-4ff13095777a.PNG)

* Lalu pilih "Add Student" untuk menambahkan data mahasiswa baru, masukkan Nama dan Jurusan 

![Add Student Page](https://user-images.githubusercontent.com/35483191/204183375-2a9e3ef6-c2ad-4979-b960-5531956eb9d2.PNG)

* Setelah menambahkan data baru, data wajah telah diambil dan telah ditraining maka akan muncul seperti dibawah ini

![Done add student](https://user-images.githubusercontent.com/35483191/204183433-6d8a35b3-d9b0-4cea-8b85-265c07908fac.PNG)

* Setelah data valid ter record maka selanjutnya klik "Face Recognition" dan akan muncul seperti ini 

![Face Recognition page](https://user-images.githubusercontent.com/35483191/204183479-7fdaa9ed-1706-4036-807e-ef8d0998e45d.PNG)






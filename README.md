# Attendance-System-Using-Face-Recognition-LBPH_Flask
***Created By Ahmad Maruf Firman***

![meh](https://user-images.githubusercontent.com/35483191/204142816-92bc8e58-c2f1-4b5d-9b04-4f9351453d5d.jpeg)

Program ini dapat jalan di Python 3.9-3.8-3.7

Requirement : 
> Install XAMPP, Pycharm, Python Libraries 

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

```![flask_db](https://user-images.githubusercontent.com/35483191/204143051-9924c020-6dcc-433a-b5a1-7c57369c81dd.PNG)

```
# Add This Library in Pycharm

>1. flask
>2. mysql-connector
>3. opencv-python
>4. opencv-contrib-python
>5. pillow

- [x] **Done**

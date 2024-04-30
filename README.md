
# LAB4WEB

Implementasi konsep modularisasi pada kode program praktikum 3 tentang database, sehingga
setiap halamannya memiliki template tampilan yang sama.



## Documentation

Halaman Home ( http://localhost/lab4/home )

Halaman About ( http://localhost/lab4/about )




## Screenshots Result

Home Page
![App Screenshot](https://i.ibb.co/vqQq8FX/Home.png)

About Page
![App Screenshot](https://i.ibb.co/qp5Dx2m/About.png)


## Step-by-Step

Create Header PHP

```bash
  <!DOCTYPE html>
    <html lang="en">
    <head>
    <meta charset="UTF-8">
    <title>Contoh Modularisasi</title>
    <link href="style.css" rel="stylesheet"           
    type="text/stylesheet"
    media="screen" />
    </head>
  
    <body>
    <div class="container">
    <header>
    <h1>Modularisasi Menggunakan Require</h1>
    </header>
    <nav>
    <a href="home.php">Home</a>
    <a href="about.php">Tentang</a>
    <a href="kontak.php">Kontak</a>
    </nav>
```
Header
![App Screenshot](https://i.ibb.co/VqTmTCD/header.png)

Create Footer PHP

```bash
            <footer>
                <p>&copy; 2024, Informatika, Universitas Pelita Bangsa</p>
            </footer>
        </div>
    </body>
</html>
```
Create Home PHP
```bash
<?php require('header.php'); ?>
  <div class="content">
    <h2>Ini Halaman Home</h2>
    <p>Ini adalah bagian content dari halaman.</p>
  </div>
<?php require('footer.php'); ?>
```

Create About PHP
```bash
<?php require('header.php'); ?>
  <div class="content">
    <h2>Ini Halaman About</h2>
    <p>Ini adalah bagian content dari halaman.</p>
  </div>
<?php require('footer.php'); ?>
```

Create Index PHP
```bash
<?php
  $mod = $_REQUEST['mod'];
  switch ($mod) {
    case "home":
      require("home.php");
      break;
    case "about":
      require("about");
      break;
    default:
      require("home.php");
  }
?>
```

Result
![App Screenshot](https://i.ibb.co/XVM9Zhf/header.png)



    
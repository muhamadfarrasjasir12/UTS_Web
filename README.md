# UTS_Web

Nama: Muhamad Farras Jasir

NIM: 312210361

Nama: Yehezkiel Juandro Metta

NIM: 312210376

Nama: Idris Syahrudin

NIM: 312210467

Nama: Nurkhotimah

NIM: 312010052


Tema: WEBINAR MANAGEMENT

# Admin/index

<?php 
  require('inc/db_config.php');
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Admin Login Panel</title>
    <?php require('inc/links.php'); ?>
    <style>
        div.login-form{
          position: absolute;
          top: 50%;
          left: 50%;
          transform: translate(-50%,-50%);
          width: 400px;
        }
    </style>
</head>
<body class="bg-light">

    <div class="login-form text-center rounded bg-white shadow overflow-hidden">
        <form method="POST">
            <h4 class="bg-dark text-white py-3">Admin Login Panel</h4>
            <div>
                <div class="mb-3">
                    <input name="admin_name" required type="text" class="form-control shadow-none text-center" placeholder="Username">
                </div>
                <div class="mb-4">
                    <input name="admin_pass" required type="password" class="form-control shadow-none text-center" placeholder="Password">
                </div>
                <button name="login" type="submit" class="btn text-white custom-bg shadow-none">Login</button>
            </div>
        </form>
    </div>
    

    <?php 

      if(isset($_POST['login']))
      {
        $frm_data = filteration($_POST);
    
        $query = "SELECT * FROM 'admin_cred' WHERE 'admin_name'=? AND 'admin_pass'=?";
        $values = [$frm_data['admin_name'],$frm_data['admin_pass']];
        
        $res = select($query,$values,"ss");
      }

    ?>


</body>
</html>

# About.php

<!DOCTYPE html>

<html lang="en">
  
<head>
  
    <meta charset="UTF-8">
    
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <title>Hotel Satu Arah | About</title>
    
     <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css">
     
     <?php require('inc/links.php'); ?>
     
     <style>
     
      .box{
      
        border-top-color: var(--teal) !important;
      
      }
      
  </style>
  
</head>

<body class="bg-light">
    
<?php require('inc/header.php'); ?>

<div class="my-5 px-4">
  
  <h2 class="fw-bold h-font text-center">About Us</h2>
  
  <div class="h-line bg-dark"></div>
  
  <p class="text-center mt-3">
    
  organisasi yang memberikan informasi tentang perusahaan atau organisasi tersebut.<br>Halaman ini biasanya berisi informasi tentang sejarah perusahaan atau organisasi, visi dan misi, nilai-nilai, produk atau layanan yang ditawarkan, dan tim manajemen
  .
  </p>
  
</div>

<div class="container">
  
  <div class="row justify-content-between align-items-center">
  
    <div class="col-lg-5 col-md-5 mb-4 order-lg-1 order-md-1 order-2">
    
      <h3 class="mb-3">Cara kami menjadi</h3>
      
      <p>
      
      Di Hotel Satu Arah Group kami berusaha untuk menjadi pilihan pertama di benak para tamu, pemilik, dan bakat. Dalam perjalanan kami untuk mencapai hal ini, kami mempraktikkan keyakinan dan tindakan kuat yang menghormati keragaman orang, komunitas, etika, dan planet ini.
      
      </p>
    
    </div>
    
    <div class="col-lg-5 col-md-5 mb-4 order-lg-2 order-md-2 order-1">
    
      <img src="image/13.jpeg" class="w-100">
    
  </div>
  
  </div>
</div>

<div class="container mt-5">
  
  <div class="row">
  
    <div class="col-lg-3 col-md-6 mb-4 px-4">
    
      <div class="bg-white rounded shadow p-4 border-top border-4 text-center box">
      
        <img src="image/Hotel.svg" width="70px">
         
        <h4 class="mt-3">100+ Ruangan</h4>
     
      </div>
    
    </div>
    
    <div class="col-lg-3 col-md-6 mb-4 px-4">
    
      <div class="bg-white rounded shadow p-4 border-top border-4 text-center box">
      
        <img src="image/Customers.svg" width="70px">
        
        <h4 class="mt-3">200+ Pelanggan</h4>
      
      </div>
  
    </div>
    
    <div class="col-lg-3 col-md-6 mb-4 px-4">
  
      <div class="bg-white rounded shadow p-4 border-top border-4 text-center box">
      
        <img src="image/Rating.svg" width="70px">
        
        <h4 class="mt-3">150+ Reviews</h4>
      
      </div>
    
    </div>
    
    <div class="col-lg-3 col-md-6 mb-4 px-4">
      
      <div class="bg-white rounded shadow p-4 border-top border-4 text-center box">
      
        <img src="image/Staff.svg" width="70px">
        
        <h4 class="mt-3">200+ Staff</h4>
      
      </div>
    
    </div>
  
  </div>

</div>

<h3 class="my-5 fw-bold h-font text-center">Management Team</h3>

<div class="container px-4">

  <div class="swiper mySwiper">
  
    <div class="swiper-wrapper mb-5">
    
      <div class="swiper-slide bg-white text-center overflow-hidden rounded">
      
        <img src="image/16.jpg" class="w-100" height="500px">
        
        <h5 class="mt-2">Ojan</h5>
      
      </div>
      
      <div class="swiper-slide bg-white text-center overflow-hidden rounded">
      
        <img src="image/15.jpg" class="w-100" height="500px">
        
        <h5 class="mt-2"></h5>Raqi
      
      </div>
      
      <div class="swiper-slide bg-white text-center overflow-hidden rounded">
      
        <img src="image/17.png" class="w-100" height="500px">
        
        <h5 class="mt-2">Firly</h5>
      
      </div>
      
      <div class="swiper-slide bg-white text-center overflow-hidden rounded">
      
        <img src="image/18.jpg" class="w-100" height="500px">
        
        <h5 class="mt-2">Fajri</h5>
      
      </div>
      
      <div class="swiper-slide bg-white text-center overflow-hidden rounded">
      
        <img src="image/14.jpg" class="w-100" height="500px" >
        
        <h5 class="mt-2">Aganzz</h5>
      
      </div>
    
    <div class="swiper-pagination"></div>
 
  </div>

</div>


<?php require('inc/footer.php'); ?>

# Fasilitas.php

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <title>Hotel Satu Arah | Fasilitas</title>
    
     <?php require('inc/links.php'); ?>
     
     <style>
     
      .pop:hover{
      
        border-top-color: var(--teal) !important;
        
        transform: scale(1.03);
        
        transition: all 0,3s;
      
      }
      
     </style>

</head>

<body class="bg-light">
    
<?php require('inc/header.php'); ?>

<div class="my-5 px-4">
  <h2 class="fw-bold h-font text-center">Our Fasilitas</h2>
  <div class="h-line bg-dark"></div>
  <p class="text-center mt-3">
  Fasilitas yang disediakan dalam hotel ini sangat lengkap sehingga anda seperti dimanjakan dalam rumah sendiri 
  </p>
</div>

<div class="container">
  <div class="row">
    <div class="col-lg-4 col-md-6 mb-5 px-4">
      <div class="bg-white rounded shadow p-4 border-top border-4 border-dark pop">
        <div class="d-flex align-items-center mb-2">
        <img src="image/Wifi.svg" width="40px">
        <h5 class="m-0 ms-3">Wifi</h5>
        </div>
        <p>
         
        </p>
      </div>
    </div>
    <div class="col-lg-4 col-md-6 mb-5 px-4">
      <div class="bg-white rounded shadow p-4 border-top border-4 border-dark pop">
        <div class="d-flex align-items-center mb-2">
        <img src="image/cart.svg" width="40px">
        <h5 class="m-0 ms-3">Market</h5>
        </div>
        <p>
        
        </p>
      </div>
    </div>
    <div class="col-lg-4 col-md-6 mb-5 px-4">
      <div class="bg-white rounded shadow p-4 border-top border-4 border-dark pop">
        <div class="d-flex align-items-center mb-2">
        <img src="image/p-square.svg
        " width="40px">
        <h5 class="m-0 ms-3">Tempat Parkir Luas</h5>
        </div>
        <p>
        
        </p>
      </div>
    </div>
    <div class="col-lg-4 col-md-6 mb-5 px-4">
      <div class="bg-white rounded shadow p-4 border-top border-4 border-dark pop">
        <div class="d-flex align-items-center mb-2">
        <img src="image/Pijat Plus-Plus.svg" width="40px">
        <h5 class="m-0 ms-3">Pijat Plus-Plus</h5>
        </div>
        <p>
        
        </p>
      </div>
    </div>
    <div class="col-lg-4 col-md-6 mb-5 px-4">
      <div class="bg-white rounded shadow p-4 border-top border-4 border-dark pop">
        <div class="d-flex align-items-center mb-2">
        <img src="image/Room Heater.svg" width="40px">
        <h5 class="m-0 ms-3">Room Heater</h5>
        </div>
        <p>
      
        </p>
      </div>
    </div>
    <div class="col-lg-4 col-md-6 mb-5 px-4">
      <div class="bg-white rounded shadow p-4 border-top border-4 border-dark pop">
        <div class="d-flex align-items-center mb-2">
        <img src="image/Televisi.svg" width="40px">
        <h5 class="m-0 ms-3">TV LED</h5>
        </div>
        <p>
        
        </p>
      </div>
    </div>
  </div>
</div>


<?php require('inc/footer.php'); ?>

</body>
</html>

# Kontak.php

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Management Webinar | Kritik dan Saran</title>
     <?php require('inc/links.php'); ?>
</head>
<body class="bg-light">
    
<?php require('inc/header.php'); ?>

<div class="my-5 px-4">
  <h2 class="fw-bold h-font text-center">Kritik dan Saran Webinar</h2>
  <div class="h-line bg-dark"></div>
  <p class="text-center mt-3"> 
  </p>
</div>

<div class="container"> 
  <div class="row">
    <div class="col-lg-4 col-md-6 mb-5 px-4">
      <div class="bg-white rounded shadow p-4">
        <iframe class="w-100 rounded mb-4 " height="320px" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3965.5380021387273!2d107.16671947460011!3d-6.324245893665236!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e699b0c08ad8d01%3A0x2b18001d1b1371f9!2sUNIVERSITAS%20PELITA%20BANGSA!5e0!3m2!1sid!2sid!4v1701680239879!5m2!1sid!2sid" loading="lazy"></iframe>

          <h5>Alamat</h5>
          <a href="https://maps.app.goo.gl/nKJxXBz1GM4qnopP6" target="_blank" class="d-inline-block text-decoration-none text-dark mb-2">
          <i class="bi bi-geo-alt-fill"></i>  Jl. Inspeksi Kalimalang No.9, Cibatu, Cikarang Selatan, Kabupaten Bekasi, Jawa Barat 17530
          </a>

          <h5 class="mt-4">Call Us</h5>
        <a href="tel : +622117081945" class="d-inline-block mb-2 text-decoration-none text-dark">
          <i class="bi bi-telephone-fill"></i> +622112061967
        </a>
        <br>
        <a href="tel : +622117081945" class="d-inline-block text-decoration-none text-dark">
          <i class="bi bi-telephone-fill"></i> +622121051998
        </a>

        <h5 class="mt-4">Email</h5>
        <a href="email: aganzzjuandrometta@gmail.com" class="d-inline-block mb-2 text-decoration-none text-dark">
        <i class="bi bi-envelope-fill"></i> aganzzjuandrometta@gmail.com
        </a>

        <h5 class="mt-4">Follow Us</h5>
        <a href="#" class="d-inline-block mb-3 text-dark fs-5 me-2">
          <i class="bi bi-twitter-x me-1"></i>
        </a>
        <a href="#" class="d-inline-block mb-3 text-dark fs-5 me-2">
          <i class="bi bi-facebook me-1"></i>
        </a>
        <a href="#" class="d-inline-block mb-3 text-dark fs-5">
          <i class="bi bi-instagram me-1"></i>
        </a>
      </div>
    </div>
    <div class="col-lg-4 col-md-6 px-4">
      <div class="bg-white rounded shadow p-4 border-top border-4">
        <form>
          <h5>Kirimkan Kritik dan Saran</h5>
          <div class="mt-3">
            <label class="form-label" style="font-weight: 500;">Nama</label>
            <input type="text" class="form-control shadow-none">
       </div>
       <div class="mt-3">
            <label class="form-label" style="font-weight: 500;">NIM</label>
            <input type="email" class="form-control shadow-none">
       </div>
       <div class="mt-3">
            <label class="form-label" style="font-weight: 500;">Kelas</label>
            <input type="text" class="form-control shadow-none">
       </div>
       <div class="mt-3">
            <label class="form-label" style="font-weight: 500;">Kritik dan Saran</label>
            <textarea class="form-control shadow-none" rows="5" style="resize: none;"></textarea>
       </div>
            <button type ="submit" class="btn text-white custom-bg mt-3">Kirim</button>
        </form>
      </div>
    </div>
  </div>
</div>


<?php require('inc/footer.php'); ?>

</body>
</html>

# Hasil

# Bagian Beranda

![Screenshot (521)](https://github.com/muhamadfarrasjasir12/UTS_Web/assets/150880443/a717fad0-7af4-4aca-aaff-498a3c53f5d2)

# Jadwal

![Screenshot (522)](https://github.com/muhamadfarrasjasir12/UTS_Web/assets/150880443/ae811f42-bb00-496b-80d1-becc1ead7fa5)

# Kritik Saran

![Screenshot (523)](https://github.com/muhamadfarrasjasir12/UTS_Web/assets/150880443/265d9bd2-e2b2-4487-b195-a2312ee88d0d)



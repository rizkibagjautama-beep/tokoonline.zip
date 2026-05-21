# tokoonline.zip
web toko online 
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Toko Online</title>

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family:Arial, sans-serif;
    }

    body{
      background:#f5f5f5;
      color:#333;
    }

    header{
      background:#111;
      color:white;
      padding:20px;
      text-align:center;
    }

    header h1{
      font-size:32px;
    }

    .container{
      width:90%;
      max-width:1200px;
      margin:auto;
      padding:30px 0;
    }

    .products{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
      gap:20px;
    }

    .card{
      background:white;
      border-radius:15px;
      overflow:hidden;
      box-shadow:0 5px 15px rgba(0,0,0,0.1);
      transition:0.3s;
    }

    .card:hover{
      transform:translateY(-5px);
    }

    .card img{
      width:100%;
      height:250px;
      object-fit:cover;
    }

    .card-content{
      padding:20px;
    }

    .card-content h3{
      margin-bottom:10px;
    }

    .price{
      color:#27ae60;
      font-size:20px;
      margin-bottom:15px;
      font-weight:bold;
    }

    .buy-btn{
      display:inline-block;
      width:100%;
      padding:12px;
      border:none;
      background:#111;
      color:white;
      border-radius:10px;
      cursor:pointer;
      font-size:16px;
      transition:0.3s;
    }

    .buy-btn:hover{
      background:#27ae60;
    }

    footer{
      text-align:center;
      padding:20px;
      background:#111;
      color:white;
      margin-top:40px;
    }
  </style>
</head>
<body>

  <header>
    <h1>My Online Shop</h1>
    <p>Toko online simple & modern</p>
  </header>

  <div class="container">

    <div class="products">

      <!-- Produk 1 -->
      <div class="card">
        <img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff" alt="Sepatu">

        <div class="card-content">
          <h3>Sepatu Sport</h3>
          <div class="price">Rp 299.000</div>

          <button class="buy-btn"
            onclick="buyProduct('Sepatu Sport',299000)">
            Beli Sekarang
          </button>
        </div>
      </div>

      <!-- Produk 2 -->
      <div class="card">
        <img src="https://images.unsplash.com/photo-1521572163474-6864f9cf17ab" alt="Kaos">

        <div class="card-content">
          <h3>Kaos Premium</h3>
          <div class="price">Rp 149.000</div>

          <button class="buy-btn"
            onclick="buyProduct('Kaos Premium',149000)">
            Beli Sekarang
          </button>
        </div>
      </div>

      <!-- Produk 3 -->
      <div class="card">
        <img src="https://images.unsplash.com/photo-1511707171634-5f897ff02aa9" alt="HP">

        <div class="card-content">
          <h3>Smartphone</h3>
          <div class="price">Rp 2.499.000</div>

          <button class="buy-btn"
            onclick="buyProduct('Smartphone',2499000)">
            Beli Sekarang
          </button>
        </div>
      </div>

    </div>
  </div>

  <footer>
    © 2026 My Online Shop
  </footer>

  <script>
    function buyProduct(product, price){

      // Ganti nomor dengan nomor WhatsApp kamu
      let phone = "628123456789";

      let message = 
      `Halo, saya ingin membeli:\n\n` +
      `Produk: ${product}\n` +
      `Harga: Rp ${price.toLocaleString()}`;

      let url = 
      `https://wa.me/${phone}?text=${encodeURIComponent(message)}`;

      window.open(url, '_blank');
    }
  </script>

</body>
</html>

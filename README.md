<?php
$title = "Bangalore Fresh - Home";
?>

<!DOCTYPE html>
<html>
<head>
    <title><?php echo $title; ?></title>
    <style>
        body { font-family: Arial; margin:0; }
        header { background: green; color: white; padding: 15px; text-align:center; }
        nav { background: #333; padding: 10px; }
        nav a { color: white; margin: 10px; text-decoration: none; }
        .hero {
            height: 400px;
            background: url('https://images.unsplash.com/photo-1542838132-92c53300491e') center/cover;
            display:flex;
            justify-content:center;
            align-items:center;
            color:white;
            font-size:40px;
        }
        .products {
            display:flex;
            justify-content:space-around;
            padding:20px;
        }
        .card {
            border:1px solid #ccc;
            padding:15px;
            width:200px;
            text-align:center;
        }
        footer {
            background:#222;
            color:white;
            text-align:center;
            padding:10px;
        }
    </style>
</head>

<body>

<header>
    <h1>Bangalore Fresh</h1>
    <p>Fresh Fruits & Vegetables Delivered Daily</p>
</header>

<nav>
    <a href="index.php">Home</a>
    <a href="products.php">Products</a>
    <a href="contact.php">Contact</a>
</nav>

<div class="hero">
    Fresh & Organic Products
</div>

<h2 style="text-align:center;">Our Products</h2>

<div class="products">

    <div class="card">
        <img src="https://www.pexels.com/photo/vibrant-display-of-fresh-tropical-fruits-30740199/">
        <h3>Fruits</h3>
        <p>Fresh seasonal fruits</p>
    </div>

    <div class="card">
        <img src="https://images.unsplash.com/photo-1540420773420-3366772f4999" width="100%">
        <h3>Vegetables</h3>
        <p>Organic vegetables</p>
    </div>

    <div class="card">
        <img src="https://images.unsplash.com/photo-1580910051074-3eb694886505" width="100%">
        <h3>Dairy</h3>
        <p>Milk & dairy products</p>
    </div>

</div>

<footer>
    <p>© <?php echo date("Y"); ?> Bangalore Fresh</p>
</footer>

</body>
</html>

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bangalore Fresh</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial, Helvetica, sans-serif;
}

body{
background:#f5f5f5;
}

/* HEADER */
header{
background:#b30000;
color:white;
padding:15px;
display:flex;
justify-content:space-between;
align-items:center;
}

header h1{
font-size:24px;
}

nav a{
color:white;
text-decoration:none;
margin:0 10px;
font-weight:bold;
}

nav a:hover{
text-decoration:underline;
}

/* HERO */
.hero{
height:400px;
width:100%;  
background:url('https://images.unsplash.com/photo-1560845137-1c409fc58595?q=80&w=708&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D') center/cover no-repeat;
display:flex;
align-items:center;
justify-content:center;
color:white;
text-align:center;
}

.hero h2{
font-size:40px;
background:rgba(0,0,0,0.5);
padding:20px;
border-radius:10px;
}

/* FILTER BUTTONS */
.filters{
text-align:center;
margin:30px 0;
}

.filters button{
padding:10px 20px;
margin:5px;
border:none;
background:#b30000;
color:white;
cursor:pointer;
border-radius:5px;
}

.filters button:hover{
background:#800000;
}

/* PRODUCTS */
.products{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:20px;
padding:20px;
}

.card{
background:white;
border-radius:10px;
overflow:hidden;
box-shadow:0 4px 10px rgba(0,0,0,0.1);
transition:0.3s;
}

.card:hover{
transform:scale(1.05);
}

.card img{
width:100%;
height:200px;
object-fit:cover;
}

.card h3{
padding:10px;
}

.card p{
padding:0 10px 10px;
}

.card button{
margin:10px;
padding:10px;
background:#b30000;
color:white;
border:none;
width:90%;
cursor:pointer;
border-radius:5px;
}

/* CONTACT */
.contact{
background:#222;
color:white;
padding:30px;
text-align:center;
}

.contact h2{
margin-bottom:15px;
}

footer{
background:#111;
color:white;
text-align:center;
padding:10px;
}

/* WHATSAPP FLOAT */
.whatsapp{
position:fixed;
bottom:20px;
right:20px;
background:#25D366;
color:white;
padding:15px;
border-radius:50%;
font-size:20px;
text-decoration:none;
}

</style>
</head>

<body>

<header>
<h1>Bangalore Fresh</h1>
<nav>
<a href="#">Home</a>
<a href="#products">Products</a>
<a href="#contact">Contact</a>
</nav>
</header>

<section class="hero">
<h2 style="font-size: 24px;">
Fresh Chicken, Meat, Red meat & Seafood Delivered at your door step in 30 min
</h2>
</section>

<div class="filters">
<button onclick="filter('all')">All</button>
<button onclick="filter('chicken')">Chicken</button>
<button onclick="filter('mutton')">Mutton</button>
<button onclick="filter('seafood')">Seafood</button>
<button onclick="filter('redmeat')">Red Meat</button>
</div>

<section class="products" id="products">

<div class="card chicken">
<img src="https://media.istockphoto.com/id/1323003448/photo/fresh-raw-chicken-on-a-rustic-wooden-table.webp?a=1&b=1&s=612x612&w=0&k=20&c=Kft2vBCjhcJDVVBeYOOlSoNIxU1jo5XJzgK68MhI3UU=">
<h3>Fresh Chicken</h3>
<p>Cleaned & hygienic farm fresh chicken.</p>
<button onclick="order('Fresh Chicken')">Order Now</button>
</div>

<div class="card mutton">
<img src="https://images.unsplash.com/photo-1689760661360-5a7ed8eb2d64?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTB8fHJhdyUyMG11dHRvbnxlbnwwfHwwfHx8MA%3D%3D">
<h3>Mutton</h3>
<p>Premium quality tender mutton.</p>
<button onclick="order('Mutton')">Order Now</button>
</div>

<div class="card seafood">
<img src="https://images.unsplash.com/photo-1615141982883-c7ad0e69fd62?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NDd8fHJhdyUyMHNlYSUyMGZvb2R8ZW58MHx8MHx8fDA%3D">
<h3>Fresh Fish</h3>
<p>Daily fresh sea fish available.</p>
<button onclick="order('Fresh Fish')">Order Now</button>
</div>

<div class="card redmeat">
<img src="https://images.unsplash.com/photo-1632154023554-c2975e9be348?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MzB8fHJhdyUyMHJlZCUyMG1lYXR8ZW58MHx8MHx8fDA%3D">
<h3>Red Meat</h3>
<p>High quality red meat cuts.</p>
<button onclick="order('Red Meat')">Order Now</button>
</div>

</section>

<section class="contact" id="contact">
<h2>Contact Us</h2>
<p>📍 Bangalore Fresh</p>
<p>📞 +91 8197451760</p>
<p>📧 freshwetfood@bangalorefresh.com</p>
</section>

<footer>
<p>© 2026 Fresh Wet Food. All Rights Reserved.</p>
</footer>

<a class="whatsapp" href="https://wa.me/918197451760">📲</a>

<script>
function filter(category){
let cards=document.querySelectorAll('.card');
cards.forEach(card=>{
if(category==='all'){
card.style.display='block';
}else{
if(card.classList.contains(category)){
card.style.display='block';
}else{
card.style.display='none';
}
}
});
}

function order(product){
let phone="919000000000";
let message="Hello, I want to order "+product;
window.open("https://wa.me/"+phone+"?text="+encodeURIComponent(message));
}
</script>

</body>
</html>
```

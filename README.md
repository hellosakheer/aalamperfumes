
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>aalamperfumes</title>
    
</head>
<body>
    
<style>

/* Google Fonts for a luxury feel */
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Poppins:wght@300;400;600&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}
/* Preloader Styles */
#preloader {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #1a1a1a;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 9999;
    transition: opacity 0.8s ease;
}

.loader-content {
    text-align: center;
}

.loader-logo {
    font-family: 'Playfair Display', serif;
    color: #fff;
    font-size: 40px;
    letter-spacing: 10px;
    margin-bottom: 20px;
}

.loader-bar {
    width: 0;
    height: 2px;
    background: #b5835a;
    animation: loading 2s forwards;
}

@keyframes loading {
    0% { width: 0; }
    100% { width: 100%; }
}

.fade-out {
    opacity: 0;
    pointer-events: none;
}
.navbar {
    background: #fff;
    height: 80px;
    width: 100%;
    border-bottom: 1px solid #eee;
    position: fixed;
    top: 0;
    z-index: 1000;
}

.nav-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

.logo a {
    font-family: 'Playfair Display', serif;
    font-size: 24px;
    color: #1a1a1a;
    text-decoration: none;
    letter-spacing: 2px;
}

.logo span {
    font-weight: 300;
    font-size: 14px;
    display: block;
    margin-top: -5px;
}

.nav-links {
    display: flex;
    list-style: none;
}

.nav-links li {
    margin: 0 15px;
}

.nav-links a {
    text-decoration: none;
    color: #333;
    font-weight: 400;
    transition: 0.3s;
}

.nav-links a:hover, .nav-links a.active {
    color: #b5835a; /* Gold/Bronze accent */
}

.nav-icons i {
    font-size: 18px;
    margin-left: 20px;
    cursor: pointer;
    color: #333;
}

/* Responsive Menu Code */
.menu-btn {
    display: none;
    font-size: 22px;
    cursor: pointer;
}

#click {
    display: none;
}

@media (max-width: 768px) {
    .menu-btn {
        display: block;
    }
    .nav-links {
        position: fixed;
        top: 80px;
        left: -100%;
        background: #fff;
        height: 100vh;
        width: 100%;
        display: block;
        text-align: center;
        transition: all 0.3s ease;
    }
    #click:checked ~ .nav-links {
        left: 0;
    }
    .nav-links li {
        margin: 40px 0;
    }
}

/*Hero Section

/* Hero Section */
.hero {
    height: 100vh; /* Full screen height */
    width: 100%;
    background: linear-gradient(to right, rgba(0,0,0,0.5), rgba(0,0,0,0.1)), 
                url('https://images.unsplash.com/photo-1541643600914-78b084683601?q=80&w=2000&auto=format&fit=crop'); /* Replace with your 4K image link */
    background-size: cover;
    background-position: center;
    display: flex;
    align-items: center;
    padding: 0 10%;
    color: #fff;
}

.hero-content {
    max-width: 600px;
}

.hero-content h4 {
    text-transform: uppercase;
    letter-spacing: 4px;
    font-size: 14px;
    margin-bottom: 10px;
    color: #b5835a; /* Our gold accent */
}

.hero-content h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(40px, 8vw, 70px); /* Responsive font size */
    line-height: 1.1;
    margin-bottom: 20px;
}

.hero-content p {
    font-size: 18px;
    margin-bottom: 30px;
    font-weight: 300;
    line-height: 1.6;
    opacity: 0.9;
}

/* Buttons */
.btn-primary, .btn-secondary {
    padding: 15px 35px;
    text-decoration: none;
    font-size: 14px;
    font-weight: 600;
    letter-spacing: 1px;
    transition: 0.3s;
    display: inline-block;
    margin-right: 15px;
}

.btn-primary {
    background: #b5835a;
    color: #fff;
    border: 1px solid #b5835a;
}

.btn-primary:hover {
    background: transparent;
    color: #fff;
    border-color: #fff;
}

.btn-secondary {
    background: transparent;
    color: #fff;
    border: 1px solid #fff;
}

.btn-secondary:hover {
    background: #fff;
    color: #000;
}

/* Animations */
.fade-in {
    animation: fadeInUp 1s ease forwards;
    opacity: 0;
}

@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* Mobile Adjustments */
@media (max-width: 768px) {
    .hero {
        padding: 0 5%;
        text-align: center;
        justify-content: center;
    }
    .hero-content h1 {
        font-size: 40px;
    }
    .btn-primary, .btn-secondary {
        margin: 10px;
        width: 80%;
    }
}

.products-section {
    padding: 80px 10%;
    background: #fff;
}

.section-title {
    text-align: center;
    margin-bottom: 50px;
}

.section-title h2 {
    font-family: 'Playfair Display', serif;
    font-size: 36px;
    color: #1a1a1a;
}

.section-title p {
    color: #888;
    letter-spacing: 1px;
}

/* The Grid System */
.product-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr); /* 4 items per line */
    gap: 30px; /* Space between products */
}

.product-card {
    background: #fff;
    transition: transform 0.3s ease;
    cursor: pointer;
}

.product-img {
    position: relative;
    overflow: hidden;
    background: #f9f9f9;
    aspect-ratio: 3/4; /* Keeps all images the same size */
}

.product-img img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s ease;
}

.product-card:hover .product-img img {
    transform: scale(1.1);
}

/* Hover Overlay */
.overlay {
    position: absolute;
    bottom: -50px;
    left: 0;
    width: 100%;
    height: 50px;
    background: rgba(0,0,0,0.8);
    display: flex;
    justify-content: center;
    align-items: center;
    transition: 0.3s;
}

.product-card:hover .overlay {
    bottom: 0;
}

.add-cart {
    color: #fff;
    background: none;
    border: none;
    text-transform: uppercase;
    font-size: 12px;
    letter-spacing: 2px;
    cursor: pointer;
}

.tag {
    position: absolute;
    top: 10px;
    left: 10px;
    background: #b5835a;
    color: #fff;
    padding: 5px 10px;
    font-size: 10px;
    text-transform: uppercase;
}

.product-info {
    padding: 15px 0;
    text-align: center;
}

.product-info h3 {
    font-size: 18px;
    margin-bottom: 5px;
    color: #333;
}

.product-info p {
    font-size: 14px;
    color: #777;
    margin-bottom: 8px;
}

.product-info .price {
    font-weight: 600;
    color: #1a1a1a;
}

/* Responsive: 2 per line on tablets, 1 per line on phones */
@media (max-width: 1024px) {
    .product-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (max-width: 600px) {
    .product-grid {
        grid-template-columns: repeat(1, 1fr);
    }
}
/* Cart Icon Badge */
.cart-icon-container {
    position: relative;
    display: inline-block;
    cursor: pointer;
}
#cart-count {
    position: absolute;
    top: -10px;
    right: -10px;
    background: #b5835a;
    color: white;
    font-size: 10px;
    padding: 2px 6px;
    border-radius: 50%;
}

/* Cart Sidebar */
.cart-sidebar {
    position: fixed;
    right: -400px; /* Hidden by default */
    top: 0;
    width: 350px;
    height: 100%;
    background: #fff;
    z-index: 2000;
    box-shadow: -5px 0 15px rgba(0,0,0,0.1);
    transition: 0.4s ease;
    display: flex;
    flex-direction: column;
}
.cart-sidebar.active { right: 0; }

.cart-header {
    padding: 20px;
    border-bottom: 1px solid #eee;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.cart-items {
    flex: 1;
    overflow-y: auto;
    padding: 20px;
}

.cart-footer {
    padding: 20px;
    border-top: 1px solid #eee;
}

.checkout-btn {
    width: 100%;
    background: #1a1a1a;
    color: #fff;
    padding: 15px;
    border: none;
    margin-top: 15px;
    cursor: pointer;
    font-weight: 600;
}

#cart-overlay {
    position: fixed;
    top: 0; left: 0;
    width: 100%; height: 100%;
    background: rgba(0,0,0,0.5);
    display: none;
    z-index: 1500;
}
#cart-overlay.active { display: block; }
.main-footer {
    background: #111;
    color: #fff;
    padding: 70px 10% 20px;
    margin-top: 50px;
}

.footer-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 40px;
}

.footer-box h3 {
    font-family: 'Playfair Display', serif;
    font-size: 24px;
    margin-bottom: 20px;
    color: #b5835a;
}

.footer-box h4 {
    font-size: 18px;
    margin-bottom: 20px;
    border-bottom: 1px solid #b5835a;
    display: inline-block;
    padding-bottom: 5px;
}

.footer-box p {
    font-size: 14px;
    line-height: 1.8;
    color: #ccc;
    margin-bottom: 10px;
}

.footer-box ul {
    list-style: none;
}

.footer-box ul li {
    margin-bottom: 10px;
}

.footer-box ul li a {
    color: #ccc;
    text-decoration: none;
    transition: 0.3s;
}

.footer-box ul li a:hover {
    color: #b5835a;
    padding-left: 5px;
}

/* Social Media */
.social-links a {
    color: #fff;
    background: #333;
    width: 35px;
    height: 35px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    margin-right: 10px;
    transition: 0.3s;
}

.social-links a:hover {
    background: #b5835a;
}

/* WhatsApp Button */
.whatsapp-btn {
    display: inline-block;
    background: #25d366;
    color: #fff;
    padding: 10px 20px;
    border-radius: 5px;
    text-decoration: none;
    font-weight: 600;
    margin-top: 10px;
    transition: 0.3s;
}

.whatsapp-btn:hover {
    background: #128c7e;
    transform: scale(1.05);
}

/* Floating Button */
.floating-wa {
    position: fixed;
    bottom: 30px;
    right: 30px;
    background: #25d366;
    color: white;
    width: 60px;
    height: 60px;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 30px;
    box-shadow: 2px 2px 10px rgba(0,0,0,0.3);
    z-index: 1000;
}

.footer-bottom {
    text-align: center;
    margin-top: 50px;
    padding-top: 20px;
    border-top: 1px solid #222;
    font-size: 12px;
    color: #777;
}

/* Mobile Responsive */
@media (max-width: 768px) {
    .footer-container {
        text-align: center;
    }
    .footer-box h4 {
        display: block;
    }
}

/*Contact Section

.contact-section {
    padding: 100px 10%;
    background: #fdfcfb; /* Soft cream background */
}

.contact-container {
    display: grid;
    grid-template-columns: 1.5fr 1fr;
    gap: 50px;
    align-items: start;
}

.contact-form h2, .newsletter-box h2 {
    font-family: 'Playfair Display', serif;
    margin-bottom: 25px;
    font-size: 32px;
}

.input-group {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
}

input, textarea {
    width: 100%;
    padding: 15px;
    margin-bottom: 20px;
    border: 1px solid #ddd;
    outline: none;
    font-family: inherit;
}

input:focus, textarea:focus {
    border-color: #b5835a;
}

/* Newsletter Specific Styling */
.newsletter-box {
    background: #1a1a1a;
    color: #fff;
    padding: 40px;
    border-radius: 5px;
}

.newsletter-box p {
    color: #ccc;
    margin-bottom: 25px;
    line-height: 1.6;
}

.news-input {
    display: flex;
}

.news-input input {
    margin-bottom: 0;
    border: none;
}

.news-input button {
    background: #b5835a;
    color: white;
    border: none;
    padding: 0 20px;
    cursor: pointer;
    transition: 0.3s;
}

.news-input button:hover {
    background: #8e6543;
}

/* Mobile Responsive */
@media (max-width: 900px) {
    .contact-container {
        grid-template-columns: 1fr;
    }
}
/* Search Bar Styling */
.search-container {
    text-align: center;
    margin-bottom: 40px;
}

#productSearch {
    width: 100%;
    max-width: 500px;
    padding: 12px 25px;
    border-radius: 30px;
    border: 1px solid #ddd;
    font-size: 16px;
    transition: 0.3s;
}

#productSearch:focus {
    border-color: #b5835a;
    box-shadow: 0 0 10px rgba(181, 131, 90, 0.2);
}

/* Back to Top Button */
#backToTop {
    position: fixed;
    bottom: 100px; /* Sits above the WhatsApp button */
    right: 30px;
    background: #1a1a1a;
    color: white;
    width: 45px;
    height: 45px;
    border-radius: 5px;
    border: none;
    cursor: pointer;
    display: none; /* Hidden by default */
    z-index: 999;
    transition: 0.3s;
}

#backToTop:hover {
    background: #b5835a;
}

.modal {
    display: none; 
    position: fixed;
    z-index: 3000;
    left: 0; top: 0;
    width: 100%; height: 100%;
    background-color: rgba(0,0,0,0.8);
    backdrop-filter: blur(5px);
}

.modal-content {
    background-color: #fff;
    margin: 5% auto;
    width: 80%;
    max-width: 900px;
    position: relative;
    padding: 40px;
    animation: zoomIn 0.3s ease;
}

.modal-body {
    display: grid;
    grid-template-columns: 1fr 1.2fr;
    gap: 40px;
}

.modal-img img {
    width: 100%;
    height: auto;
    border-radius: 4px;
}

.modal-details h2 {
    font-family: 'Playfair Display', serif;
    font-size: 32px;
    margin-bottom: 10px;
}

.modal-price {
    font-size: 24px;
    color: #b5835a;
    font-weight: 600;
    margin-bottom: 20px;
}

.scent-notes {
    margin: 20px 0;
    padding: 15px 0;
    border-top: 1px solid #eee;
    border-bottom: 1px solid #eee;
    font-size: 14px;
}

.close-modal {
    position: absolute;
    right: 20px; top: 10px;
    font-size: 30px;
    cursor: pointer;
}

@keyframes zoomIn {
    from { transform: scale(0.9); opacity: 0; }
    to { transform: scale(1); opacity: 1; }
}

/* Mobile Modal */
@media (max-width: 768px) {
    .modal-body { grid-template-columns: 1fr; }
    .modal-content { width: 95%; margin: 10% auto; padding: 20px; }
}
/* Brand Story */
.brand-story {
    padding: 100px 10%;
    text-align: center;
    background: #fff;
}

.story-content span {
    color: #b5835a;
    letter-spacing: 5px;
    text-transform: uppercase;
    font-size: 12px;
}

.story-content h2 {
    font-family: 'Playfair Display', serif;
    font-size: 40px;
    margin: 20px 0;
}

.story-content p {
    max-width: 700px;
    margin: 0 auto;
    line-height: 1.8;
    color: #666;
}

.signature {
    margin-top: 30px;
    width: 150px;
    opacity: 0.7;
}

/* Reviews Section */
.reviews {
    background: #f9f9f9;
    padding: 80px 10%;
}

.reviews-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
    margin-top: 40px;
}

.review-card {
    background: #fff;
    padding: 40px;
    text-align: center;
    box-shadow: 0 10px 30px rgba(0,0,0,0.05);
    border-radius: 5px;
}

.stars {
    color: #b5835a;
    margin-bottom: 15px;
}

.review-card p {
    font-style: italic;
    color: #444;
    margin-bottom: 20px;
    line-height: 1.6;
}

.review-card h4 {
    text-transform: uppercase;
    font-size: 13px;
    letter-spacing: 2px;
    color: #1a1a1a;
}


.king-letter {
    position: fixed;
    right: 30px;
    top: 50%; /* Starting position */
    width: 220px;
    background: #ffffff; /* Old paper color */
    padding: 25px 15px;
    border: 2px solid #b5835a;
    box-shadow: 8px 8px 20px rgba(0,0,0,0.2), inset 0 0 50px rgba(181, 131, 90, 0.2);
    z-index: 4000;
    text-align: center;
    border-radius: 2px;
    transform: translateY(-50%);
    transition: top 0.1s ease-out; /* This creates the "floating" movement */
}

/* Paper edge effect */
.king-letter::before, .king-letter::after {
    content: "";
    position: absolute;
    height: 10px;
    width: 100%;
    background: #b89494;
    left: 0;
}
.king-letter::before { top: -10px; border-radius: 10px 10px 0 0; }
.king-letter::after { bottom: -10px; border-radius: 0 0 10px 10px; }

.royal-seal {
    width: 40px;
    margin-bottom: 10px;
}

.letter-content h3 {
    font-family: 'Courier New', Courier, monospace;
    font-size: 18px;
    color: #1a1a1a;
    margin-bottom: 10px;
    border-bottom: 1px double #b5835a;
}

.letter-content p {
    font-size: 15px;
    line-height: 1.4;
    color: #0c0b0b;
    font-style: normal;
}

.instruction {
    margin-top: 10px;
    color: #fcfbfa !important;
    font-weight: bold;
}

.scroll-footer {
    margin-top: 15px;
    font-size: 10px;
    letter-spacing: 2px;
    font-weight: bold;
    color: #888;
}

/* Hide on very small screens to avoid blocking products */
@media (max-width: 900px) {
    .king-letter {
        display: none;
    }
}



</style>







<div id="preloader">
    <div class="loader-content">
        <h1 class="loader-logo">AALAM</h1>
        <div class="loader-bar"></div>
    </div>
</div>

<nav class="navbar">
    <div class="nav-container">
        <div class="logo">
            <a href="#">Aalam <span>Perfumes</span></a>
        </div>

        <input type="checkbox" id="click">
        <label for="click" class="menu-btn">
            <i class="fas fa-bars"></i>
        </label>

        <ul class="nav-links">
            <li><a href="#" class="active">Home</a></li>
            <li><a href="#">Collections</a></li>
            <li><a href="#">Men</a></li>
            <li><a href="#">Women</a></li>
            <li><a href="#">Contact</a></li>
        </ul>

        <div class="nav-icons">
            <a href="#"><i class="fas fa-search"></i></a>
            <a href="#"><i class="fas fa-shopping-cart"></i></a>
        </div>
    </div>
</nav>

<!--Hero Section-->

<section class="hero">
    <div class="hero-content">
        <h4 class="fade-in">New Collection 2026</h4>
        <h1 class="fade-in">Essence of Elegance</h1>
        <p class="fade-in">Discover the art of fine fragrance with Aalam Perfumes. Crafted for those who leave a lasting impression.</p>
        <div class="hero-btns fade-in">
            <a href="#" class="btn-primary">Shop Now</a>
            <a href="#" class="btn-secondary">Explore Scents</a>
        </div>
    </div>
</section>

<!--Peoduct-->
<section class="products-section">
    <div class="section-title">
        <h2>Our Signature Collection</h2>
        <p>Premium fragrances for every occasion</p>
    </div>

    <div class="product-grid">
        <div class="product-card">
            <div class="product-img">
                <img src="https://images.unsplash.com/photo-1594035910387-fea47794261f?w=500" alt="Perfume 1">
                <span class="tag">New</span>
                <div class="overlay">
                    <button class="add-cart">Add to Cart</button>
                </div>
            </div>
            <div class="product-info">
                <h3>Oud Al Aalam</h3>
                <p>Luxury Woody Scent</p>
                <div class="price">₹120.00</div>
            </div>
        </div>

        </div>
</section>
<div class="nav-icons">
    <a href="#"><i class="fas fa-search"></i></a>
    <div class="cart-icon-container" onclick="toggleCart()">
        <i class="fas fa-shopping-cart"></i>
        <span id="cart-count">0</span>
    </div>
</div>

<div id="cart-sidebar" class="cart-sidebar">
    <div class="cart-header">
        <h2>Your Basket</h2>
        <span class="close-cart" onclick="toggleCart()">&times;</span>
    </div>
    
    <div class="cart-items" id="cart-items">
        <p class="empty-msg">Your cart is empty.</p>
    </div>

    <div class="cart-footer">
        <div class="total-container">
            <span>Total:</span>
            <span id="cart-total">$0.00</span>
        </div>
        <button class="checkout-btn">Proceed to Checkout</button>
    </div>
</div>
<div id="cart-overlay" onclick="toggleCart()"></div>


        
<div class="search-container">
    <input type="text" id="productSearch" placeholder="Search for your signature scent..." onkeyup="filterProducts()">
</div>

<button id="backToTop" onclick="scrollToTop()"><i class="fas fa-arrow-up"></i></button>


<div id="product-modal" class="modal">
    <div class="modal-content">
        <span class="close-modal" onclick="closeModal()">&times;</span>
        <div class="modal-body">
            <div class="modal-img">
                <img id="modal-image" src="" alt="Perfume Large">
            </div>
            <div class="modal-details">
                <h2 id="modal-title">Perfume Name</h2>
                <p class="modal-price" id="modal-price">$0.00</p>
                <div class="scent-notes">
                    <p><strong>Top Notes:</strong> Bergamot, Pink Pepper</p>
                    <p><strong>Heart Notes:</strong> Jasmine, Turkish Rose</p>
                    <p><strong>Base Notes:</strong> Amber, Patchouli, Vanilla</p>
                </div>
                <p class="modal-desc">A sophisticated blend of rare ingredients designed for the modern individual.</p>
                <button class="btn-primary" id="modal-add-btn">Add to Cart</button>
            </div>
        </div>
    </div>
</div>
<section class="brand-story">
    <div class="story-content">
        <span>Since 2026</span>
        <h2>The Art of Fragrance</h2>
        <p>Aalam Perfumes was born from a passion for rare botanicals and the hidden alchemy of scent. Every bottle is a journey, designed to evoke emotion and define your presence.</p>
        <img src="https://images.unsplash.com/photo-1592945403244-b3fbafd7f539?w=400" alt="Signature" class="signature">
    </div>
</section>

<section class="reviews">
    <div class="section-title">
        <h2>What Our Clients Say</h2>
    </div>
    <div class="reviews-container">
        <div class="review-card">
            <div class="stars">★★★★★</div>
            <p>"The Oud Aalam is breathtaking. I get compliments every time I wear it. Truly a luxury experience."</p>
            <h4>— AYSHA MA.</h4>
        </div>
        <div class="review-card">
            <div class="stars">★★★★★</div>
            <p>"Fast shipping and the packaging was beautiful. You can tell they care about quality."</p>
            <h4>— SANIYYA IRFAN.</h4>
        </div>
        <div class="review-card">
            <div class="stars">★★★★★</div>
            <p>"Aalam has replaced my designer perfumes. The scent lasts all day long."</p>
            <h4>— HALEEMA.</h4>
        </div>
    </div>
</section>

<footer class="main-footer">
    <div class="footer-container">
        <div class="footer-box">
            <h3>Aalam Perfumes</h3>
            <p>Crafting memories through scents. Our perfumes are curated with the finest ingredients from around the world.</p>
            <div class="social-links">
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-facebook-f"></i></a>
                <a href="#"><i class="fab fa-pinterest"></i></a>
            </div>
        </div>

        <div class="footer-box">
            <h4>Quick Links</h4>
            <ul>
                <li><a href="#">About Us</a></li>
                <li><a href="#">Privacy Policy</a></li>
                <li><a href="#">Shipping & Returns</a></li>
                <li><a href="#">Track Order</a></li>
            </ul>
        </div>

        <div class="footer-box">
            <h4>Contact Us</h4>
            <p><i class="fas fa-map-marker-alt"></i> Vaduthala Alappuzha, Majlisul Abrar Complex</p>
            <p><i class="fas fa-phone"></i> +91 88910 15965</p>
            <p><i class="fas fa-envelope"></i> info@aalamperfumes.com</p>
        </div>

        <div class="footer-box">
            <h4>Customer Support</h4>
            <p>Need help choosing a scent?</p>
            <a href="https://wa.me/8891015965?text=Hi Aalam Perfumes, I need help with a fragrance!" class="whatsapp-btn" target="_blank">
                <i class="fab fa-whatsapp"></i> Chat on WhatsApp
            </a>
        </div>
    </div>
    
    <div class="footer-bottom">
        <p>&copy; 2026 Aalam Perfumes. All Rights Reserved. | Designed with Luxury</p>
    </div>
</footer>

<a href="https://wa.me/8891015965" class="floating-wa" target="_blank">
    <i class="fab fa-whatsapp"></i>
</a>



<div id="royal-scroll" class="king-letter">
    <div class="letter-content">
        <!--img src="#" alt="Seal" class="royal-seal"-->
        <h3>Aalam Notice</h3>
        <p>Our digital checkout is under maintenance.</p>
        <p class="instruction">Kindly click the <strong>WhatsApp</strong> icon below to place your order.</p>
        <div class="scroll-footer">BY ORDER OF AALAM</div>
    </div>
</div>

<script>
window.addEventListener('load', () => {
    const preloader = document.getElementById('preloader');
    
    // Add a slight delay so the user sees the branding
    setTimeout(() => {
        preloader.classList.add('fade-out');
    }, 1500);
});
// Change navbar background on scroll
window.addEventListener('scroll', () => {
    const navbar = document.querySelector('.navbar');
    if (window.scrollY > 50) {
        navbar.style.boxShadow = "0 2px 10px rgba(0,0,0,0.1)";
    } else {
        navbar.style.boxShadow = "none";
    }
});
//Hero Section
window.addEventListener('scroll', function() {
    const hero = document.querySelector('.hero');
    let offset = window.pageYOffset;
    // This moves the background image at 50% scroll speed
    hero.style.backgroundPositionY = offset * 0.5 + "px";
});

const grid = document.querySelector('.product-grid');
const productHTML = grid.innerHTML; // Get the first card we wrote

// Loop to add 23 more cards
for (let i = 0; i < 23; i++) {
    grid.innerHTML += productHTML;
}
let cart = JSON.parse(localStorage.getItem('AALAM_CART')) || [];

// Open/Close Cart
function toggleCart() {
    document.getElementById('cart-sidebar').classList.toggle('active');
    document.getElementById('cart-overlay').classList.toggle('active');
}

// Add Product to Cart
function addToCart(name, price, image) {
    const item = { name, price, image, quantity: 1 };
    
    // Check if already in cart
    const existingItem = cart.find(i => i.name === name);
    if(existingItem) {
        existingItem.quantity++;
    } else {
        cart.push(item);
    }
    
    updateCartUI();
    saveCart();
    if(!document.getElementById('cart-sidebar').classList.contains('active')) {
        toggleCart();
    }
}

function updateCartUI() {
    const cartContainer = document.getElementById('cart-items');
    const cartCount = document.getElementById('cart-count');
    const cartTotal = document.getElementById('cart-total');
    
    cartContainer.innerHTML = '';
    let total = 0;
    let count = 0;

    cart.forEach((item, index) => {
        total += item.price * item.quantity;
        count += item.quantity;
        
        cartContainer.innerHTML += `
            <div class="cart-item">
                <img src="${item.image}" width="50">
                <div>
                    <h4>${item.name}</h4>
                    <p>$${item.price} x ${item.quantity}</p>
                    <button onclick="removeFromCart(${index})">Remove</button>
                </div>
            </div>
        `;
    });

    cartCount.innerText = count;
    cartTotal.innerText = `$${total.toFixed(2)}`;
}

function removeFromCart(index) {
    cart.splice(index, 1);
    updateCartUI();
    saveCart();
}

function saveCart() {
    localStorage.setItem('AALAM_CART', JSON.stringify(cart));
}

// Initial UI Update
updateCartUI();
//Contact info
// Contact Form Submission
document.getElementById('perfumeContactForm').addEventListener('submit', function(e) {
    e.preventDefault();
    
    // Simple visual feedback
    const btn = this.querySelector('button');
    const originalText = btn.innerText;
    
    btn.innerText = "Message Sent!";
    btn.style.background = "#25d366"; // Green for success
    
    this.reset(); // Clear the form

    setTimeout(() => {
        btn.innerText = originalText;
        btn.style.background = "#b5835a";
    }, 3000);
});
// 1. Search Filter Logic
function filterProducts() {
    let input = document.getElementById('productSearch').value.toLowerCase();
    let cards = document.getElementsByClassName('product-card');

    for (let i = 0; i < cards.length; i++) {
        let title = cards[i].querySelector('.product-info h3').innerText.toLowerCase();
        if (title.includes(input)) {
            cards[i].style.display = "";
        } else {
            cards[i].style.display = "none";
        }
    }
}

// 2. Back to Top Logic
window.onscroll = function() {
    const btn = document.getElementById("backToTop");
    if (document.body.scrollTop > 400 || document.documentElement.scrollTop > 400) {
        btn.style.display = "block";
    } else {
        btn.style.display = "none";
    }
};

function scrollToTop() {
    window.scrollTo({ top: 0, behavior: 'smooth' });
}
function openQuickView(name, price, image) {
    document.getElementById('modal-title').innerText = name;
    document.getElementById('modal-price').innerText = `$${price}`;
    document.getElementById('modal-image').src = image;
    
    // Set the button to work inside the modal
    document.getElementById('modal-add-btn').onclick = function() {
        addToCart(name, price, image);
        closeModal();
    };

    document.getElementById('product-modal').style.display = "block";
}

function closeModal() {
    document.getElementById('product-modal').style.display = "none";
}

// Close modal if user clicks outside of it
window.onclick = function(event) {
    let modal = document.getElementById('product-modal');
    if (event.target == modal) {
        closeModal();
    }
}
// Reveal elements on scroll
const revealOnScroll = () => {
    const sections = document.querySelectorAll('section');
    sections.forEach(section => {
        const sectionTop = section.getBoundingClientRect().top;
        const windowHeight = window.innerHeight;
        if (sectionTop < windowHeight * 0.85) {
            section.style.opacity = "1";
            section.style.transform = "translateY(0)";
        }
    });
};

// Set initial state for reveal
document.querySelectorAll('section').forEach(section => {
    section.style.opacity = "0";
    section.style.transform = "translateY(50px)";
    section.style.transition = "all 0.8s ease-out";
});

window.addEventListener('scroll', revealOnScroll);

window.addEventListener('scroll', () => {
    const letter = document.getElementById('royal-scroll');
    const scrollPercent = window.scrollY / (document.documentElement.scrollHeight - window.innerHeight);
    
    // This calculates a new 'top' position based on how far you have scrolled
    // It stays roughly in the middle of the screen but 'bobs' up and down
    const moveRange = 200; // How many pixels it can move up/down
    const newTop = 50 + (scrollPercent * moveRange - (moveRange / 2));
    
    letter.style.top = `${newTop}%`;
});

</script>

</body>
</html>

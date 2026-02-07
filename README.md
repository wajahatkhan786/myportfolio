# myportfolio
im happy
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Walkin | Premium Sandals Collection</title>
    
    <!-- Google Fonts for modern typography -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Oswald:wght@300;500;700&family=Roboto:wght@300;400;500&display=swap" rel="stylesheet">

    <style>
        /* --- CSS Variables & Reset --- */
        :root {
            /* Color Palette - Black & Grey Theme */
            --bg-body: #050505;       /* Deepest Black */
            --bg-card: #141414;       /* Dark Grey for cards */
            --bg-nav: rgba(5, 5, 5, 0.95);
            --text-main: #ffffff;
            --text-muted: #a0a0a0;
            --accent: #333333;        /* Dark Grey for borders */
            --highlight: #ffffff;     /* White for buttons/icons */
            
            /* Spacing & Transition */
            --container-width: 1200px;
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Roboto', sans-serif;
            background-color: var(--bg-body);
            color: var(--text-main);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3, h4 {
            font-family: 'Oswald', sans-serif;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: 700;
        }

        a {
            text-decoration: none;
            color: inherit;
            transition: var(--transition);
        }

        ul {
            list-style: none;
        }

        img {
            max-width: 100%;
            display: block;
            object-fit: cover;
        }

        /* --- Utility Classes --- */
        .container {
            max-width: var(--container-width);
            margin: 0 auto;
            padding: 0 20px;
        }

        .section-padding {
            padding: 80px 0;
        }

        .text-center {
            text-align: center;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            border: 2px solid var(--text-main);
            background: transparent;
            color: var(--text-main);
            font-family: 'Oswald', sans-serif;
            font-size: 14px;
            letter-spacing: 2px;
            text-transform: uppercase;
            cursor: pointer;
            transition: var(--transition);
        }

        .btn:hover {
            background: var(--text-main);
            color: var(--bg-body);
        }

        .btn-primary {
            background: var(--text-main);
            color: var(--bg-body);
        }

        .btn-primary:hover {
            background: transparent;
            color: var(--text-main);
        }

        /* --- Header / Navigation --- */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: var(--bg-nav);
            backdrop-filter: blur(10px);
            z-index: 1000;
            border-bottom: 1px solid var(--accent);
        }

        .nav-wrapper {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 80px;
        }

        .logo {
            font-size: 28px;
            font-family: 'Oswald', sans-serif;
            font-weight: 700;
            letter-spacing: 2px;
        }

        .logo span {
            color: var(--text-muted);
        }

        nav ul {
            display: flex;
            gap: 30px;
        }

        nav a {
            font-size: 14px;
            font-weight: 500;
            color: var(--text-muted);
            text-transform: uppercase;
        }

        nav a:hover, nav a.active {
            color: var(--text-main);
        }

        .cart-icon {
            font-size: 18px;
            cursor: pointer;
        }

        /* --- Hero Section --- */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.4)), url('https://picsum.photos/seed/shoes_hero/1920/1080');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
        }

        .hero-content h1 {
            font-size: 72px;
            margin-bottom: 20px;
            line-height: 1.1;
        }

        .hero-content p {
            font-size: 18px;
            color: #dcdcdc;
            margin-bottom: 40px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        /* --- Features Section --- */
        .features {
            background-color: var(--bg-card);
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            text-align: center;
        }

        .feature-item i {
            font-size: 30px;
            margin-bottom: 15px;
            display: block;
        }

        .feature-item h3 {
            margin-bottom: 10px;
            font-size: 18px;
        }

        .feature-item p {
            color: var(--text-muted);
            font-size: 14px;
        }

        /* --- Product Collection (Sandals) --- */
        .section-title {
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-size: 42px;
            margin-bottom: 10px;
        }

        .section-title p {
            color: var(--text-muted);
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
        }

        .product-card {
            background-color: var(--bg-card);
            border: 1px solid var(--accent);
            overflow: hidden;
            transition: var(--transition);
            position: relative;
        }

        .product-card:hover {
            transform: translateY(-5px);
            border-color: var(--text-muted);
        }

        .product-image {
            width: 100%;
            height: 320px;
            position: relative;
            overflow: hidden;
        }

        .product-image img {
            width: 100%;
            height: 100%;
            transition: transform 0.5s ease;
        }

        .product-card:hover .product-image img {
            transform: scale(1.1);
        }

        .tag {
            position: absolute;
            top: 15px;
            left: 15px;
            background-color: var(--text-main);
            color: var(--bg-body);
            padding: 5px 10px;
            font-size: 10px;
            font-weight: 700;
            text-transform: uppercase;
        }

        .product-info {
            padding: 20px;
            text-align: center;
        }

        .product-category {
            color: var(--text-muted);
            font-size: 12px;
            text-transform: uppercase;
            margin-bottom: 5px;
            display: block;
        }

        .product-title {
            font-size: 18px;
            margin-bottom: 10px;
            color: var(--text-main);
        }

        .product-price {
            font-size: 16px;
            font-weight: 500;
            color: var(--text-muted);
            margin-bottom: 15px;
            display: block;
        }

        /* --- About / Promo Section --- */
        .promo-section {
            background-color: #111;
            display: grid;
            grid-template-columns: 1fr 1fr;
            align-items: center;
        }

        .promo-image img {
            width: 100%;
            height: 100%;
            min-height: 500px;
        }

        .promo-content {
            padding: 80px;
        }

        .promo-content h2 {
            font-size: 36px;
            margin-bottom: 20px;
        }

        .promo-content p {
            color: var(--text-muted);
            margin-bottom: 30px;
        }

        /* --- Footer --- */
        footer {
            background-color: #000;
            padding: 60px 0 20px;
            border-top: 1px solid var(--accent);
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-col h4 {
            margin-bottom: 20px;
            font-size: 16px;
        }

        .footer-col ul li {
            margin-bottom: 10px;
        }

        .footer-col ul li a {
            color: var(--text-muted);
            font-size: 14px;
        }

        .footer-col ul li a:hover {
            color: var(--text-main);
            padding-left: 5px;
        }

        .newsletter-form {
            display: flex;
            margin-top: 15px;
        }

        .newsletter-form input {
            padding: 10px;
            background: #1a1a1a;
            border: 1px solid #333;
            color: #fff;
            width: 100%;
            outline: none;
        }

        .newsletter-form button {
            padding: 10px 20px;
            background: #fff;
            border: none;
            cursor: pointer;
            font-weight: bold;
        }

        .copyright {
            text-align: center;
            border-top: 1px solid #1a1a1a;
            padding-top: 20px;
            font-size: 12px;
            color: #555;
        }

        /* --- Responsive Design --- */
        @media (max-width: 768px) {
            .hero-content h1 {
                font-size: 48px;
            }
            
            .promo-section {
                grid-template-columns: 1fr;
            }

            .promo-image img {
                min-height: 300px;
            }

            .promo-content {
                padding: 40px 20px;
            }

            nav {
                display: none; /* Simple hiding for mobile for this demo */
            }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="container nav-wrapper">
            <div class="logo">WALKIN<span>.</span></div>
            <nav>
                <ul>
                    <li><a href="#" class="active">Home</a></li>
                    <li><a href="#collection">Collection</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
            <div class="cart-icon">
                CART (0)
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>WALK WITH<br>CONFIDENCE</h1>
            <p>Discover the ultimate collection of premium sandals. Designed for comfort, engineered for style.</p>
            <a href="#collection" class="btn btn-primary">Shop Now</a>
        </div>
    </section>

    <!-- Features Section -->
    <section class="section-padding features">
        <div class="container">
            <div class="features-grid">
                <div class="feature-item">
                    <i>✦</i>
                    <h3>Premium Leather</h3>
                    <p>Handcrafted with the finest genuine leather for durability.</p>
                </div>
                <div class="feature-item">
                    <i>✦</i>
                    <h3>Ultimate Comfort</h3>
                    <p>Ergonomic soles designed to keep you walking all day.</p>
                </div>
                <div class="feature-item">
                    <i>✦</i>
                    <h3>Modern Aesthetics</h3>
                    <p>Sleek black and grey designs that match every outfit.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Product Collection -->
    <section id="collection" class="section-padding">
        <div class="container">
            <div class="text-center section-title">
                <h2>Latest Collection</h2>
                <p>Our top picks for the season</p>
            </div>

            <div class="product-grid">
                <!-- Product 1 -->
                <article class="product-card">
                    <div class="product-image">
                        <span class="tag">New</span>
                        <!-- Placeholder image with specific seed for variety -->
                        <img src="https://picsum.photos/seed/sandal1/600/800" alt="Midnight Walker Sandal">
                    </div>
                    <div class="product-info">
                        <span class="product-category">Men's Collection</span>
                        <h3 class="product-title">Midnight Walker</h3>
                        <span class="product-price">$85.00</span>
                        <button class="btn">Add to Cart</button>
                    </div>
                </article>

                <!-- Product 2 -->
                <article class="product-card">
                    <div class="product-image">
                        <img src="https://picsum.photos/seed/sandal2/600/800" alt="Urban Grey Slide">
                    </div>
                    <div class="product-info">
                        <span class="product-category">Casual</span>
                        <h3 class="product-title">Urban Grey Slide</h3>
                        <span class="product-price">$60.00</span>
                        <button class="btn">Add to Cart</button>
                    </div>
                </article>

                <!-- Product 3 -->
                <article class="product-card">
                    <div class="product-image">
                        <span class="tag">Hot</span>
                        <img src="https://picsum.photos/seed/sandal3/600/800" alt="Stealth Strap">
                    </div>
                    <div class="product-info">
                        <span class="product-category">Outdoor</span>
                        <h3 class="product-title">Stealth Strap</h3>
                        <span class="product-price">$95.00</span>
                        <button class="btn">Add to Cart</button>
                    </div>
                </article>

                <!-- Product 4 -->
                <article class="product-card">
                    <div class="product-image">
                        <img src="https://picsum.photos/seed/sandal4/600/800" alt="Onyx Comfort">
                    </div>
                    <div class="product-info">
                        <span class="product-category">Men's Collection</span>
                        <h3 class="product-title">Onyx Comfort</h3>
                        <span class="product-price">$75.00</span>
                        <button class="btn">Add to Cart</button>
                    </div>
                </article>
            </div>
            
            <div class="text-center" style="margin-top: 50px;">
                <a href="#" class="btn btn-primary">View All Products</a>
            </div>
        </div>
    </section>

    <!-- Promo / About Section -->
    <section id="about" class="promo-section">
        <div class="promo-image">
            <!-- Abstract dark texture image representing craftsmanship -->
            <img src="https://picsum.photos/seed/texture_dark/800/800" alt="Walkin Craftsmanship">
        </div>
        <div class="promo-content">
            <h2>The Walkin Standard</h2>
            <p>Hum maante hain ke footwear sirf pehnne ka cheez nahi, balki ek experience hai. Walkin sandals ko design kiya gaya hai un logon ke liye jo quality aur style ko compromise nahi karna chahte.</p>
            <p>Har pair mein hamari craftsmanship aur dedication chamakti hai. Black aur Grey tones ka use karke humne un designs ko banaya hai jo kabhi purane nahi honge.</p>
            <a href="#" class="btn">Read Our Story</a>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <div class="logo" style="margin-bottom: 20px;">WALKIN<span>.</span></div>
                    <p style="color: #666; font-size: 14px;">Premium footwear for the modern soul. Quality, comfort, and style in every step.</p>
                </div>
                <div class="footer-col">
                    <h4>Shop</h4>
                    <ul>
                        <li><a href="#">New Arrivals</a></li>
                        <li><a href="#">Best Sellers</a></li>
                        <li><a href="#">Men's Sandals</a></li>
                        <li><a href="#">Accessories</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h4>Support</h4>
                    <ul>
                        <li><a href="#">Contact Us</a></li>
                        <li><a href="#">Shipping & Returns</a></li>
                        <li><a href="#">Size Guide</a></li>
                        <li><a href="#">FAQ</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h4>Newsletter</h4>
                    <p style="color: #666; font-size: 14px;">Subscribe for latest updates.</p>
                    <form class="newsletter-form" onsubmit="event.preventDefault();">
                        <input type="email" placeholder="Your Email">
                        <button type="submit">GO</button>
                    </form>
                </div>
            </div>
            <div class="copyright">
                &copy; 2023 Walkin Footwear. All Rights Reserved.
            </div>
        </div>
    </footer>

</body>
</html>

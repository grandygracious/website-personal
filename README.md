<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Satarbucks - Coffee & More</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* CSS Styles */
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
            color: #333;
        }

        header {
            background-color: #006341; /* Starbucks-like green */
            color: white;
            padding: 1rem 2rem;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo img {
            margin-right: 10px;
            height: 50px;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 20px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: opacity 0.3s;
        }

        nav ul li a:hover {
            opacity: 0.8;
        }

        /* Hero Section */
        .hero {
            background: url('https://images.unsplash.com/photo-1497935586351-b67a49e012bf?ixlib=rb-1.2.1&auto=format&fit=crop&w=1200&q=80') no-repeat center center/cover;
            height: 400px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.4);
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            padding: 0 20px;
        }

        .hero-content h2 {
            font-size: 3rem;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        .hero-content p {
            font-size: 1.5rem;
            margin-bottom: 20px;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
        }

        .btn {
            background-color: #006341;
            color: white;
            border: none;
            padding: 12px 24px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            font-size: 1rem;
            transition: all 0.3s;
        }

        .btn:hover {
            background-color: #004d32;
            transform: translateY(-2px);
        }

        /* Menu Section */
        .menu {
            padding: 4rem 2rem;
            text-align: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        .menu h2 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            color: #006341;
        }

        .menu-items {
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
        }

        .item {
            background: white;
            border-radius: 10px;
            padding: 1.5rem;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            width: 250px;
            transition: all 0.3s;
        }

        .item:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
        }

        .item img {
            border-radius: 10px;
            margin-bottom: 1rem;
            width: 100%;
            height: 150px;
            object-fit: cover;
        }

        .item h3 {
            margin: 0.5rem 0;
            color: #006341;
        }

        .item p {
            color: #666;
            margin-bottom: 1rem;
            font-size: 0.9rem;
        }

        .item span {
            font-weight: bold;
            color: #006341;
            font-size: 1.2rem;
        }

        /* About Section */
        .about {
            padding: 4rem 2rem;
            text-align: center;
            background: white;
            margin: 2rem 0;
        }

        .about-content {
            max-width: 1200px;
            margin: 0 auto;
            text-align: left;
        }

        .about h2 {
            color: #006341;
            font-size: 2.5rem;
            margin-bottom: 2rem;
            text-align: center;
        }

        .about p {
            line-height: 1.8;
            margin-bottom: 1.5rem;
        }

        .locations {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            margin-top: 2rem;
        }

        .city {
            width: 48%;
            margin-bottom: 2rem;
        }

        .city h3 {
            color: #006341;
            border-bottom: 2px solid #006341;
            padding-bottom: 0.5rem;
            margin-bottom: 1rem;
        }

        .city ul {
            list-style-type: none;
            padding: 0;
        }

        .city li {
            margin-bottom: 0.5rem;
            padding-left: 1.5rem;
            position: relative;
        }

        .city li::before {
            content: "•";
            color: #006341;
            font-weight: bold;
            position: absolute;
            left: 0;
        }

        /* Contact Section */
        .contact {
            padding: 4rem 2rem;
            text-align: center;
            background: white;
            margin: 2rem 0;
            max-width: 1200px;
            margin: 0 auto;
        }

        .contact h2 {
            color: #006341;
            font-size: 2.5rem;
        }

        .contact form {
            max-width: 500px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .contact input, .contact textarea {
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: 'Poppins', sans-serif;
            font-size: 1rem;
        }

        .contact textarea {
            height: 150px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background: #006341;
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 2rem;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 1rem;
        }

        .social-links a {
            color: white;
            text-decoration: none;
            transition: opacity 0.3s;
        }

        .social-links a:hover {
            opacity: 0.8;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            nav {
                flex-direction: column;
                text-align: center;
            }
            
            .logo {
                margin-bottom: 1rem;
            }
            
            nav ul {
                padding: 0;
            }
            
            .hero-content h2 {
                font-size: 2rem;
            }
            
            .hero-content p {
                font-size: 1.2rem;
            }
            
            .city {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">
                <img src="https://cdn.pixabay.com/photo/2017/09/03/11/05/starbucks-2709927_1280.jpg" alt="Satarbucks Logo">
                <h1>Satarbucks</h1>
            </div>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#menu">Menu</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="hero-content">
            <h2>Welcome to Satarbucks</h2>
            <p>Your daily dose of happiness in a cup!</p>
            <button class="btn">Order Now</button>
        </div>
    </section>

    <section id="menu" class="menu">
        <h2>Our Menu</h2>
        <div class="menu-items">
            <div class="item">
                <img src="https://images.unsplash.com/photo-1517701550927-30cf4ba1dba5?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Coffee">
                <h3>Satarbucks Brew</h3>
                <p>Rich, bold, and unforgettable espresso blend with caramel undertones.</p>
                <span>$4.99</span>
            </div>
            <div class="item">
                <img src="https://images.unsplash.com/photo-1551029506-0807df4e2031?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Latte">
                <h3>Caramel Cloud</h3>
                <p>Sweet, creamy latte with homemade caramel sauce and whipped cream.</p>
                <span>$5.99</span>
            </div>
            <div class="item">
                <img src="https://images.unsplash.com/photo-1510591509098-f4fdc6d0ff04?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Cold Brew">
                <h3>Iced Galaxy</h3>
                <p>Cool, refreshing cold brew with hints of vanilla and blueberry.</p>
                <span>$4.49</span>
            </div>
        </div>
    </section>

    <section id="about" class="about">
        <div class="about-content">
            <h2>About Satarbucks</h2>
            <p>Satarbucks adalah sebuah kafe fiktif yang terinspirasi dari Starbucks, menawarkan pengalaman minum kopi premium dengan sentuhan unik dan suasana yang nyaman. Kami berkomitmen untuk menyajikan kopi berkualitas tinggi dengan racikan spesial yang memanjakan lidah.</p>
            
            <p>Satarbucks didirikan pada tahun 2023 dengan misi memberikan pengalaman ngopi yang berbeda. Kami menggunakan biji kopi pilihan dari berbagai penjuru dunia, seperti Arabika Ethiopia (rasa floral & fruity), Robusta Vietnam (bold & kuat), dan Kopi Toraja (khas Indonesia, earthy & smooth).</p>
            
            <p>Selain kopi, kami juga menyediakan berbagai minuman signature seperti Caramel Cloud, Iced Galaxy, dan Satarbucks Brew. Kami juga menawarkan pilihan dessert lezat seperti Croissant, Red Velvet Cake, dan Tiramisu, serta opsi non-kopi seperti Matcha Latte dan Chocolate Avocado.</p>
            
            <p>Kami percaya bahwa secangkir kopi bukan hanya minuman, melainkan sebuah cerita, kebahagiaan, dan inspirasi. Setiap tegukan di Satarbucks dirancang untuk memberikan pengalaman yang tak terlupakan.</p>
            
            <h3>Our Locations in Indonesia</h3>
            <div class="locations">
                <div class="city">
                    <h3>Jakarta</h3>
                    <ul>
                        <li>Satarbucks Grand Indonesia (Lantai 3, West Mall)</li>
                        <li>Satarbucks Plaza Senayan (Food Hall)</li>
                        <li>Satarbucks Pondok Indah Mall (Lantai 2)</li>
                    </ul>
                </div>
                <div class="city">
                    <h3>Bandung</h3>
                    <ul>
                        <li>Satarbucks Paris Van Java (Near Main Entrance)</li>
                        <li>Satarbucks Braga Street (Historic Café)</li>
                    </ul>
                </div>
                <div class="city">
                    <h3>Surabaya</h3>
                    <ul>
                        <li>Satarbucks Tunjungan Plaza (Lantai 5)</li>
                        <li>Satarbucks Pakuwon Mall (Food Court Area)</li>
                    </ul>
                </div>
                <div class="city">
                    <h3>Bali</h3>
                    <ul>
                        <li>Satarbucks Seminyak Beach (Beachfront Café)</li>
                        <li>Satarbucks Ubud Art Market (Cultural Vibes)</li>
                    </ul>
                </div>
            </div>
            
            <p><strong>Jam Operasional:</strong> Setiap hari <strong>08:00 - 22:00 WIB</strong>.</p>
        </div>
    </section>

    <section id="contact" class="contact">
        <h2>Contact Us</h2>
        <form>
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <textarea placeholder="Your Message" required></textarea>
            <button type="submit" class="btn">Send Message</button>
        </form>
    </section>

    <footer>
        <div class="social-links">
            <a href="https://instagram.com/satarbucks.id" target="_blank">Instagram</a>
            <a href="https://facebook.com/satarbucks.id" target="_blank">Facebook</a>
            <a href="mailto:info@satarbucks.id">Email</a>
        </div>
        <p>&copy; 2023 Satarbucks. All rights reserved.</p>
        <p>#SatarbucksID #CoffeeJourney</p>
    </footer>
</body>
</html>
        

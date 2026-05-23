<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Renajoe Exclusive Centre | Chalets, Conference, Restaurant | Kubease</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/js/all.min.js"></script>
    <style>
        :root {
            --primary: #e67e22; 
            --primary-dark: #d35400;
            --dark: #2c3e50; 
            --light: #f8f9fa;
            --text: #333333;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            color: var(--text);
            background-color: #ffffff;
            line-height: 1.6;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            color: var(--dark);
            margin-bottom: 40px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--primary);
            border-radius: 2px;
        }

        /* Navigation */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 8%;
            background: #ffffff;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo-text {
            font-size: 22px;
            font-weight: bold;
            color: var(--dark);
        }

        .logo-highlight {
            color: var(--primary);
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 25px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 600;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.65), rgba(0, 0, 0, 0.65)), url('150433.jpg') no-repeat center center/cover;
            height: 65vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: white;
            padding: 0 20px;
        }

        .hero h1 {
            font-size: 3.2rem;
            margin-bottom: 10px;
            font-weight: 800;
        }

        .hero p {
            font-size: 1.25rem;
            margin-bottom: 30px;
            max-width: 700px;
        }

        .cta-buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .btn {
            padding: 12px 30px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: bold;
            text-transform: uppercase;
            font-size: 0.9rem;
            transition: transform 0.3s, background 0.3s;
        }

        .btn:active { transform: scale(0.95); }
        .btn-primary { background-color: var(--primary); color: white; }
        .btn-primary:hover { background-color: var(--primary-dark); }
        .btn-whatsapp { background-color: #25D366; color: white; display: flex; align-items: center; gap: 8px; }
        .btn-whatsapp:hover { background-color: #20ba5a; }

        /* About Section */
        .about {
            padding: 70px 8%;
            background-color: #ffffff;
        }

        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            align-items: center;
        }

        .about-text p {
            font-size: 1.1rem;
            color: #555;
            margin-bottom: 15px;
            line-height: 1.8;
        }

        .landmark-card {
            background-color: var(--light);
            padding: 25px;
            border-radius: 10px;
            border-left: 4px solid var(--primary);
            box-shadow: 0 4px 6px rgba(0,0,0,0.02);
        }

        .landmark-card h4 {
            color: var(--dark);
            margin-bottom: 15px;
            font-size: 1.2rem;
        }

        .landmark-list {
            list-style: none;
        }

        .landmark-list li {
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1rem;
        }

        /* Gallery Section */
        .gallery {
            padding: 70px 8%;
            background-color: var(--light);
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            grid-gap: 20px;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.08);
            background-color: #fff;
            aspect-ratio: 4/3;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.4s ease;
            display: block;
        }

        .gallery-item:hover img {
            transform: scale(1.08);
        }
        
        .gallery-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(0,0,0,0.85), rgba(0,0,0,0.4), transparent);
            color: white;
            padding: 20px 15px 15px 15px;
            font-size: 1rem;
            font-weight: 600;
            text-align: center;
        }

        /* Amenities Section */
        .amenities {
            padding: 70px 8%;
            background-color: #ffffff;
        }

        .amenities-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 25px;
        }

        .amenity-card {
            background: var(--light);
            padding: 25px;
            border-radius: 8px;
            text-align: center;
            transition: background 0.3s;
        }
        
        .amenity-card:hover {
            background: #edf1f5;
        }

        .amenity-card i {
            font-size: 2.2rem;
            color: var(--primary);
            margin-bottom: 15px;
        }

        .amenity-card h3 {
            color: var(--dark);
            font-size: 1.15rem;
        }

        /* Contact Section */
        .contact {
            padding: 70px 8%;
            background-color: var(--dark);
            color: white;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 40px;
        }

        .contact-details h2 {
            font-size: 2.2rem;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .contact-item {
            margin-bottom: 20px;
            display: flex;
            align-items: flex-start;
            gap: 15px;
        }

        .contact-item i {
            font-size: 1.2rem;
            color: var(--primary);
            margin-top: 4px;
        }

        .contact-item a {
            color: white;
            text-decoration: none;
            transition: color 0.2s;
        }

        .contact-item a:hover { color: var(--primary); }

        .map-box {
            border-radius: 8px;
            overflow: hidden;
            height: 300px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }

        .map-box img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* Footer */
        footer {
            background: #1a252f;
            color: #7f8c8d;
            text-align: center;
            padding: 25px;
            font-size: 0.9rem;
            border-top: 1px solid #34495e;
        }

        @media (max-width: 768px) {
            nav { flex-direction: column; gap: 10px; }
            .nav-links li { margin: 5px 10px; }
            .hero h1 { font-size: 2.2rem; }
            .about, .gallery, .amenities, .contact { padding: 50px 6%; }
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo-text">Renajoe <span class="logo-highlight">Exclusive Centre</span></div>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#gallery">Gallery</a></li>
            <li><a href="#amenities">Amenities</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <section class="hero" id="home">
        <h1>Renajoe Exclusive Centre</h1>
        <p>Premium chalet accommodations, modern conference facilities, and excellent road-side dining in Kubease.</p>
        <div class="cta-buttons">
            <a href="tel:0503144885" class="btn btn-primary"><i class="fa-solid fa-phone"></i> Call to Book</a>
            <a href="https://wa.me/233503144885" target="_blank" class="btn btn-whatsapp"><i class="fa-brands fa-whatsapp"></i> WhatsApp Us</a>
        </div>
    </section>

    <section class="about" id="about">
        <div class="about-grid">
            <div class="about-text">
                <h2>Premium Accommodations</h2>
                <p><strong>Renajoe Exclusive Centre</strong> offers beautiful chalet lodgings perfectly tailored for travelers, tourists, and corporate events. Featuring 19 fully furnished, comfortable bedrooms with private terraces, we ensure a serene environment to relax and recharge.</p>
                <p>Every room comes complete with full air-conditioning, water heaters, flat-screen televisions, private refrigerators, clean towels, and bathroom bidets. Free high-speed Wi-Fi is accessible property-wide.</p>
            </div>
            <div class="landmark-card">
                <h4><i class="fa-solid fa-map-location-dot"></i> Key Landmarks Nearby</h4>
                <ul class="landmark-list">
                    <li><i class="fa-solid fa-car-side" style="color:var(--primary)"></i> 18 miles from Baba Yara Stadium</li>
                    <li><i class="fa-solid fa-car-side" style="color:var(--primary)"></i> 19 miles from Manhyia Palace</li>
                    <li><i class="fa-solid fa-plane" style="color:var(--primary)"></i> 21 miles from Kumasi International Airport</li>
                    <li><i class="fa-solid fa-tree" style="color:var(--primary)"></i> 28 miles from Owabi Wildlife Sanctuary</li>
                </ul>
            </div>
        </div>
    </section>

    <section class="gallery" id="gallery">
        <h2 class="section-title">Photo Gallery</h2>
        <div class="gallery-grid">
            
            <div class="gallery-item">
                <img src="150401.jpg" alt="Conference Hall Entrance">
                <div class="gallery-overlay">Conference Hall Entrance</div>
            </div>

            <div class="gallery-item">
                <img src="150403.jpg" alt="Main Conference Hall">
                <div class="gallery-overlay">Main Conference Hall (U-Shape)</div>
            </div>

            <div class="gallery-item">
                <img src="150407.jpg" alt="Conference Room Setup View">
                <div class="gallery-overlay">Spacious Event Seating</div>
            </div>

            <div class="gallery-item">
                <img src="150417.jpg" alt="Deluxe Bedroom Bed">
                <div class="gallery-overlay">Deluxe Bedroom Setup</div>
            </div>

            <div class="gallery-item">
                <img src="150415.jpg" alt="Conference Screen Presentation Area">
                <div class="gallery-overlay">Presentation Area & Projector Screen</div>
            </div>

            <div class="gallery-item">
                <img src="150419.jpg" alt="Executive Room Interior">
                <div class="gallery-overlay">Executive Rooms with Fitted Wardrobes</div>
            </div>

            <div class="gallery-item">
                <img src="150433.jpg" alt="Beautiful compound view">
                <div class="gallery-overlay">Paved Compound & Secure Parking Area</div>
            </div>

            <div class="gallery-item">
                <img src="150435.jpg" alt="Chalet exterior building block">
                <div class="gallery-overlay">Vibrant Chalet Exterior Facade</div>
            </div>

            <div class="gallery-item">
                <img src="150431.jpg" alt="Renajoe Roadside Signboard">
                <div class="gallery-overlay">Our Roadside Signage on Accra-Kumasi Highway</div>
            </div>

            <div class="gallery-item">
                <img src="150437.jpg" alt="Gardens Monument">
                <div class="gallery-overlay">Iconic Centerpiece Garden Statue</div>
            </div>

        </div>
    </section>

    <section class="amenities" id="amenities">
        <h2 class="section-title">In-Room & Facility Comforts</h2>
        <div class="amenities-grid">
            <div class="amenity-card">
                <i class="fa-solid fa-snowflake"></i>
                <h3>Air Conditioning</h3>
            </div>
            <div class="amenity-card">
                <i class="fa-solid fa-wifi"></i>
                <h3>Free Property Wi-Fi</h3>
            </div>
            <div class="amenity-card">
                <i class="fa-solid fa-tv"></i>
                <h3>Flat Screen TVs</h3>
            </div>
            <div class="amenity-card">
                <i class="fa-solid fa-temperature-arrow-up"></i>
                <h3>Water Heaters</h3>
            </div>
            <div class="amenity-card">
                <i class="fa-solid fa-kitchen-set"></i>
                <h3>Private Fridge</h3>
            </div>
            <div class="amenity-card">
                <i class="fa-solid fa-soap"></i>
                <h3>Bidets & Fresh Towels</h3>
            </div>
            <div class="amenity-card">
                <i class="fa-solid fa-users-rectangle"></i>
                <h3>Conference Venue</h3>
            </div>
            <div class="amenity-card">
                <i class="fa-solid fa-shield-halved"></i>
                <h3>Tight On-site Security</h3>
            </div>
        </div>
    </section>

    <section class="contact" id="contact">
        <div class="contact-grid">
            <div class="contact-details">
                <h2>Get In Touch</h2>
                <div class="contact-item">
                    <i class="fa-solid fa-location-dot"></i>
                    <div>
                        <strong>Location Address:</strong><br>
                        Accra - Kumasi Highway, Kubease, Ghana
                    </div>
                </div>
                <div class="contact-item">
                    <i class="fa-solid fa-phone"></i>
                    <div>
                        <strong>Booking Enquiries:</strong><br>
                        <a href="tel:0503144885">050 314 4885</a> or <a href="tel:0503144886">050 314 4886</a>
                    </div>
                </div>
                <div class="contact-item">
                    <i class="fa-brands fa-whatsapp"></i>
                    <div>
                        <strong>Instant WhatsApp Chat:</strong><br>
                        <a href="https://wa.me/233503144885" target="_blank">050 314 4885</a>
                    </div>
                </div>
            </div>
            <div class="map-box">
                <img src="150431.jpg" alt="Renajoe Centre Billboard location picture">
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; 2026 Renajoe Exclusive Centre. All rights reserved.</p>
        <p style="font-size: 0.8rem; margin-top: 4px; color: #5d6d7e;">Kubease, Ashanti Region, Ghana</p>
    </footer>

</body>
</html>

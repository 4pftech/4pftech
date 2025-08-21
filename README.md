<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yusuf Milas | Graphic Designer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Base Styles */
        :root {
            --primary: #ff4d5a;
            --secondary: #2d3e50;
            --accent: #ffc107;
            --light: #f8f9fa;
            --dark: #212529;
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        a {
            text-decoration: none;
            color: inherit;
        }
        
        ul {
            list-style: none;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 28px;
            background: var(--primary);
            color: white;
            border-radius: 30px;
            font-weight: 600;
            transition: var(--transition);
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background: #e04450;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        .section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 15px;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--primary);
        }
        
        /* Header */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            padding: 15px 0;
            transition: var(--transition);
        }
        
        header.scrolled {
            padding: 10px 0;
        }
        
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--secondary);
        }
        
        .logo span {
            color: var(--primary);
        }
        
        .nav-menu {
            display: flex;
        }
        
        .nav-item {
            margin: 0 15px;
        }
        
        .nav-link {
            color: var(--secondary);
            font-weight: 500;
            transition: var(--transition);
        }
        
        .nav-link:hover {
            color: var(--primary);
        }
        
        .hamburger {
            display: none;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(135deg, rgba(45,62,80,0.9) 0%, rgba(45,62,80,0.7) 100%), url('https://images.unsplash.com/photo-1519389950473-47ba0277781c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1770&q=80') no-repeat center center/cover;
            color: white;
            text-align: center;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }
        
 .about-content {
    display: flex;
    align-items: flex-start; /* Changed from center to flex-start */
    gap: 50px;
}
        
        .about-img {
            flex: 1.2;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
        }
        
  .about-img img {
    width: 100%;
    height: auto;
    display: block;
    transition: var(--transition);
    border-radius: 10px; /* Added this line */
}
        
        .about-img:hover img {
            transform: scale(1.05);
        }
        
        .about-text {
            flex: 0.8;
        }
        
        .about-text h3 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: var(--secondary);
        }
        
        .info-list {
            margin: 20px 0;
        }
        
        .info-item {
            display: flex;
            margin-bottom: 10px;
        }
        
        .info-title {
            font-weight: 600;
            min-width: 100px;
            color: var(--secondary);
        }
        
        /* Portfolio Section */
        .portfolio {
            background: #f1f5f9;
        }
        
        .portfolio-filters {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 30px;
        }
        
        .filter-btn {
            padding: 8px 20px;
            margin: 5px;
            background: white;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            font-weight: 500;
            transition: var(--transition);
        }
        
        .filter-btn.active, .filter-btn:hover {
            background: var(--primary);
            color: white;
        }
        
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .portfolio-item {
    border-radius: 10px;
    overflow: hidden;
    position: relative;
    box-shadow: 0 10px 20px rgba(0,0,0,0.1);
    height: auto; /* Changed from 250px */
    aspect-ratio: 1/1; /* Added this line */
}
        
       .portfolio-img {
    width: 100%;
    height: 100%;
    object-fit: contain; /* Changed from 'cover' */
    transition: var(--transition);
    background-color: #f5f5f5; /* Added this line */
}
        
        .portfolio-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(45,62,80,0.9);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: var(--transition);
            padding: 20px;
            text-align: center;
            color: white;
        }
        
        .portfolio-item:hover .portfolio-overlay {
            opacity: 1;
        }
        
        .portfolio-item:hover .portfolio-img {
            transform: scale(1.1);
        }
        
        .portfolio-title {
            font-size: 1.5rem;
            margin-bottom: 10px;
            transform: translateY(-20px);
            transition: var(--transition);
        }
        
        .portfolio-desc {
            transform: translateY(20px);
            transition: var(--transition);
            opacity: 0;
        }
        
        .portfolio-item:hover .portfolio-title,
        .portfolio-item:hover .portfolio-desc {
            transform: translateY(0);
            opacity: 1;
        }
        
        /* Contact Section */
        .contact-content {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 50px;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background: var(--primary);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-size: 1.2rem;
        }
        
        .contact-form {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: var(--transition);
        }
        
        .form-control:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(255,77,90,0.2);
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background: var(--secondary);
            color: white;
            padding: 50px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-logo {
            font-size: 1.8rem;
            margin-bottom: 15px;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-link {
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: var(--transition);
        }
        
        .social-link:hover {
            background: var(--primary);
            transform: translateY(-5px);
        }
        
        .footer-heading {
            font-size: 1.2rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-heading::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 2px;
            background: var(--primary);
        }
        
        .footer-links li {
            margin-bottom: 10px;
        }
        
        .footer-links a {
            transition: var(--transition);
        }
        
        .footer-links a:hover {
            color: var(--primary);
            padding-left: 5px;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .about-content,
            .contact-content,
            .footer-content {
                grid-template-columns: 1fr;
            }
            
            .hero h1 {
                font-size: 2.8rem;
            }
        }
        
        @media (max-width: 768px) {
            .nav-menu {
                position: fixed;
                top: 70px;
                right: -100%;
                background: white;
                width: 80%;
                height: calc(100vh - 70px);
                flex-direction: column;
                align-items: center;
                justify-content: center;
                transition: var(--transition);
                box-shadow: -5px 0 15px rgba(0,0,0,0.1);
            }
            
            .nav-menu.active {
                right: 0;
            }
            
            .nav-item {
                margin: 15px 0;
            }
            
            .hamburger {
                display: block;
            }
            
            .hero h1 {
                font-size: 2.3rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }
        
        @media (max-width: 576px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .btn {
                padding: 10px 20px;
            }
            
            .portfolio-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <div class="container">
            <nav class="navbar">
                <a href="#" class="logo">4p.<span>Tech</span></a>
                
                <ul class="nav-menu">
                    <li class="nav-item"><a href="#home" class="nav-link">Home</a></li>
                    <li class="nav-item"><a href="#about" class="nav-link">About</a></li>
                    <li class="nav-item"><a href="#portfolio" class="nav-link">Portfolio</a></li>
                    <li class="nav-item"><a href="#contact" class="nav-link">Contact</a></li>
                </ul>
                
                <div class="hamburger">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Creative Graphic Designer & Visual Artist</h1>
                <p>Transforming ideas into stunning visual experiences through graphic design, poster creation, and music cover art.</p>
                <a href="#portfolio" class="btn">View My Work</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
<section id="about" class="section">
    <div class="container">
        <div class="section-title">
            <h2>About Me</h2>
            <p>Get to know more about my journey and expertise</p>
        </div>
        
        <div class="about-content">
           <div class="about-img">
    <img src="https://i.supaimg.com/eb19158f-0a92-4983-b6c6-9123015a6ed0.jpg" alt="Yusuf Milas">
</div>
            
            <div class="about-text">
                <h3>Professional Graphic Designer</h3>
                <p>Hello! I'm Yusuf Milas, a passionate graphic designer specializing in poster design, music cover art, and visual branding. With years of experience since 2019, I've developed a keen eye for aesthetics and a strong understanding of visual communication.</p>
                
                <div class="info-list">
                    <div class="info-item">
                        <span class="info-title">Name:</span>
                        <span>Yusuf Milas</span>
                    </div>
                    <div class="info-item">
                        <span class="info-title">Email:</span>
                        <span>yusufmilas176@gmail.com</span>
                    </div>
                    <div class="info-item">
                        <span class="info-title">Phone:</span>
                        <span>+255766161342</span>
                    </div>
                    <div class="info-item">
                        <span class="info-title">Location:</span>
                        <span>Kigamboni, Dar es Salaam</span>
                    </div>
                    <div class="info-item">
                        <span class="info-title">Experience:</span>
                        <span>Since 2019</span>
                    </div>
                </div>
                
                <a href="#contact" class="btn">Hire Me</a>
            </div>
        </div>
    </div>
</section>

<!-- Portfolio Section -->
<section id="portfolio" class="section portfolio">
    <div class="container">
        <div class="section-title">
            <h2>My Portfolio</h2>
            <p>Explore my creative works and projects</p>
        </div>
        
        <div class="portfolio-filters">
            <button class="filter-btn active" data-filter="all">All</button>
            <button class="filter-btn" data-filter="posters">Posters</button>
            <button class="filter-btn" data-filter="covers">Music Covers</button>
            <button class="filter-btn" data-filter="graphic">Graphic Design</button>
        </div>
        
        <div class="portfolio-grid">
            <!-- Poster category images -->
            <div class="portfolio-item" data-category="posters">
                <img src="https://i.supaimg.com/50ce702e-9a46-463f-84bb-b6f5407a98f1.png" alt="Poster Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Event Poster</h3>
                    <p class="portfolio-desc">Vibrant promotional design</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="posters">
                <img src="https://i.supaimg.com/6a186127-ee3e-418d-b15d-e10aa1345688.png" alt="Poster Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Promotional Poster</h3>
                    <p class="portfolio-desc">Eye-catching event promotion</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="posters">
                <img src="https://i.supaimg.com/6bb59794-5235-4130-80e2-2f58dbd89975.png" alt="Poster Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Festival Poster</h3>
                    <p class="portfolio-desc">Cultural event design</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="posters">
                <img src="https://i.supaimg.com/78228522-cf1d-4585-b3e3-36adefa8a458.png" alt="Poster Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Concert Poster</h3>
                    <p class="portfolio-desc">Music event promotion</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="posters">
                <img src="https://i.supaimg.com/3480b057-7827-4f67-b740-2fa923ed34dc.png" alt="Poster Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Show Poster</h3>
                    <p class="portfolio-desc">Entertainment event design</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="posters">
                <img src="https://i.supaimg.com/71ab828a-2dd4-4fe2-9433-0a1e38921841.png" alt="Poster Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Party Poster</h3>
                    <p class="portfolio-desc">Nightlife event promotion</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="posters">
                <img src="https://i.supaimg.com/b11f26c4-4b23-43f8-8e01-d02712562302.png" alt="Poster Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Special Event Poster</h3>
                    <p class="portfolio-desc">Unique occasion design</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="posters">
                <img src="https://i.supaimg.com/cae681c3-0584-458d-863d-436316a12a9d.png" alt="Poster Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Event Promotion</h3>
                    <p class="portfolio-desc">Creative poster design</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="posters">
                <img src="https://i.supaimg.com/069aea37-d0ad-4ed3-baa4-b907f08c24f7.png" alt="Poster Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Marketing Poster</h3>
                    <p class="portfolio-desc">Promotional material</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="posters">
                <img src="https://i.supaimg.com/f86b6cb8-4b0b-481e-b9b8-8068d07f7c6a.png" alt="Poster Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Advertising Poster</h3>
                    <p class="portfolio-desc">Brand promotion design</p>
                </div>
            </div>
            
            <!-- Music Covers category images -->
            <div class="portfolio-item" data-category="covers">
                <img src="https://i.supaimg.com/68779af9-7a9f-4658-a2ce-f4052c333bb8.png" alt="Music Cover" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Album Cover Art</h3>
                    <p class="portfolio-desc">Modern design for music album</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="covers">
                <img src="https://i.supaimg.com/1d0529f0-7915-404c-98d8-1fbd0244d46b.png" alt="Music Cover" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Single Cover</h3>
                    <p class="portfolio-desc">Cover for music single release</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="covers">
                <img src="https://i.supaimg.com/74ee61be-c366-4840-a816-806d9bc4f433.png" alt="Music Cover" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Album Artwork</h3>
                    <p class="portfolio-desc">Vibrant music cover design</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="covers">
                <img src="https://i.supaimg.com/0e23dc1e-0b31-4fb9-ab95-739ae2596a45.png" alt="Music Cover" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Music Single</h3>
                    <p class="portfolio-desc">Cover for digital release</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="covers">
                <img src="https://i.supaimg.com/229578f2-2c4b-4f8f-8c03-4f9cc44923c5.png" alt="Music Cover" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">EP Cover</h3>
                    <p class="portfolio-desc">Extended play cover design</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="covers">
                <img src="https://i.supaimg.com/5f9fa95d-843d-4e67-83e8-8058a8dd8866.png" alt="Music Cover" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Single Release</h3>
                    <p class="portfolio-desc">Digital streaming platform cover</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="covers">
                <img src="https://i.supaimg.com/595b22d8-37bc-44b6-8f20-138e672a4c40.png" alt="Music Cover" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Album Cover</h3>
                    <p class="portfolio-desc">Full album artwork design</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="covers">
                <img src="https://i.supaimg.com/076527bc-792f-4574-bb6e-697d01e55ae9.png" alt="Music Cover" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Music Artwork</h3>
                    <p class="portfolio-desc">Creative cover for artist</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="covers">
                <img src="https://i.supaimg.com/0f8cf65a-53c2-451d-8b74-0346b97f45a7.png" alt="Music Cover" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Music Cover Design</h3>
                    <p class="portfolio-desc">Artistic album artwork</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="covers">
                <img src="https://i.supaimg.com/805a0bf7-ea73-4db7-8ce0-d63e1a90b088.png" alt="Music Cover" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Single Artwork</h3>
                    <p class="portfolio-desc">Cover for music release</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="covers">
                <img src="https://i.supaimg.com/bef9b1d2-c2e0-461a-ab4a-81eb48640536.png" alt="Music Cover" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Album Cover Design</h3>
                    <p class="portfolio-desc">Professional music artwork</p>
                </div>
            </div>
            
            <!-- Graphic Design category images -->
            <div class="portfolio-item" data-category="graphic">
                <img src="https://i.supaimg.com/abe48e31-2bff-4775-8878-ff6bb308ba11.png" alt="Graphic Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Graphic Design</h3>
                    <p class="portfolio-desc">Creative visual solution</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="graphic">
                <img src="https://i.supaimg.com/afe7853f-f652-4190-bf10-1a8e926d3070.png" alt="Graphic Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Visual Design</h3>
                    <p class="portfolio-desc">Artistic graphic work</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="graphic">
                <img src="https://i.supaimg.com/e0e90f61-c3e5-4996-9f81-f0ff2097f6a7.png" alt="Graphic Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Brand Design</h3>
                    <p class="portfolio-desc">Visual identity work</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="graphic">
                <img src="https://i.supaimg.com/bc36337f-b4e9-4b20-b0cf-8fcee80ff713.png" alt="Graphic Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Creative Design</h3>
                    <p class="portfolio-desc">Innovative graphic solution</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="graphic">
                <img src="https://i.supaimg.com/f89ecfff-a678-4910-9010-a401bde91685.png" alt="Graphic Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Visual Content</h3>
                    <p class="portfolio-desc">Engaging graphic design</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="graphic">
                <img src="https://i.ibb.co/NdBtryJS/image.jpg" alt="Graphic Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Brand Identity</h3>
                    <p class="portfolio-desc">Complete branding package</p>
                </div>
            </div>
            
            <div class="portfolio-item" data-category="graphic">
                <img src="https://i.ibb.co/pjb7SqJM/image.jpg" alt="Graphic Design" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3 class="portfolio-title">Marketing Design</h3>
                    <p class="portfolio-desc">Promotional graphic work</p>
                </div>
            </div>
        </div>
        
        <div style="text-align: center; margin-top: 40px;">
            <a href="#" class="btn">View More Work</a>
        </div>
    </div>
</section>
    <!-- Contact Section -->
    <section id="contact" class="section">
        <div class="container">
            <div class="section-title">
                <h2>Contact Me</h2>
                <p>Get in touch for collaborations and projects</p>
            </div>
            
            <div class="contact-content">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div>
                            <h3>Location</h3>
                            <p>Kigamboni, Dar es Salaam, Tanzania</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div>
                            <h3>Email</h3>
                            <p>yusufmilas176@gmail.com</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div>
                            <h3>Phone</h3>
                            <p>+255766161342</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-clock"></i>
                        </div>
                        <div>
                            <h3>Working Hours</h3>
                            <p>Monday - Friday: 9AM - 6PM</p>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form id="contactForm">
                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Your Name" required>
                        </div>
                        <div class="form-group">
                            <input type="email" class="form-control" placeholder="Your Email" required>
                        </div>
                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Subject" required>
                        </div>
                        <div class="form-group">
                            <textarea class="form-control" placeholder="Your Message" required></textarea>
                        </div>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-about">
                    <h3 class="footer-logo">Yusuf<span>Milas</span></h3>
                    <p>Creative graphic designer specializing in posters, music covers, and visual branding solutions.</p>
                    <div class="social-links">
                        <a href="#" class="social-link"><i class="fab fa-facebook-f"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-behance"></i></a>
                    </div>
                </div>
                
                <div class="footer-links">
                    <h3 class="footer-heading">Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#portfolio">Portfolio</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                
                <div class="footer-links">
                    <h3 class="footer-heading">Services</h3>
                    <ul>
                        <li><a href="#">Poster Design</a></li>
                        <li><a href="#">Music Cover Art</a></li>
                        <li><a href="#">Graphic Design</a></li>
                        <li><a href="#">Brand Identity</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 Yusuf Milas. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Sticky Header
        window.addEventListener('scroll', function() {
            const header = document.getElementById('header');
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
        
        // Mobile Menu Toggle
        const hamburger = document.querySelector('.hamburger');
        const navMenu = document.querySelector('.nav-menu');
        
        hamburger.addEventListener('click', function() {
            navMenu.classList.toggle('active');
        });
        
        // Close mobile menu when clicking on a nav link
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', () => {
                navMenu.classList.remove('active');
            });
        });
        
        // Portfolio Filtering
        const filterButtons = document.querySelectorAll('.filter-btn');
        const portfolioItems = document.querySelectorAll('.portfolio-item');
        
        filterButtons.forEach(button => {
            button.addEventListener('click', () => {
                // Remove active class from all buttons
                filterButtons.forEach(btn => btn.classList.remove('active'));
                
                // Add active class to clicked button
                button.classList.add('active');
                
                // Get filter value
                const filterValue = button.getAttribute('data-filter');
                
                // Filter portfolio items
                portfolioItems.forEach(item => {
                    if (filterValue === 'all' || item.getAttribute('data-category') === filterValue) {
                        item.style.display = 'block';
                    } else {
                        item.style.display = 'none';
                    }
                });
            });
        });
        
        // Form Submission
        const contactForm = document.getElementById('contactForm');
        
        contactForm.addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! I will get back to you soon.');
            contactForm.reset();
        });
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
<body>
</html>

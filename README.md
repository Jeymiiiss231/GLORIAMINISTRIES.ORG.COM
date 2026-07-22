<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gloria Wamuyu Ministries - Feeding, Clothing & Schooling Children in Kenya</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Open+Sans:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2E7D32;
            --primary-dark: #1B5E20;
            --accent: #FF6F00;
            --accent-light: #FF8F00;
            --warm: #FFF3E0;
            --text-dark: #1a1a1a;
            --text-light: #666;
            --white: #ffffff;
            --shadow: 0 10px 40px rgba(0,0,0,0.1);
            --radius: 16px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Open Sans', sans-serif;
            color: var(--text-dark);
            line-height: 1.7;
            overflow-x: hidden;
        }

        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255,255,255,0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 15px 0;
            box-shadow: 0 2px 20px rgba(0,0,0,0.05);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo i {
            color: var(--accent);
        }

        .nav-links {
            display: flex;
            gap: 35px;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            font-size: 0.95rem;
            transition: color 0.3s;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: width 0.3s;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .donate-nav-btn {
            background: var(--accent);
            color: white !important;
            padding: 10px 25px;
            border-radius: 50px;
            transition: all 0.3s !important;
        }

        .donate-nav-btn:hover {
            background: var(--accent-light);
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(255,111,0,0.3);
        }

        .donate-nav-btn::after {
            display: none !important;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            background: linear-gradient(135deg, rgba(46,125,50,0.85) 0%, rgba(27,94,32,0.9) 100%),
                        url('https://images.unsplash.com/photo-1488521787991-ed7bbaae773c?w=1920&h=1080&fit=crop') center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            padding: 120px 30px 80px;
            position: relative;
        }

        .hero::before {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            height: 150px;
            background: linear-gradient(to top, var(--warm), transparent);
        }

        .hero-content {
            max-width: 900px;
            position: relative;
            z-index: 1;
        }

        .hero-badge {
            display: inline-block;
            background: rgba(255,255,255,0.2);
            backdrop-filter: blur(10px);
            padding: 8px 25px;
            border-radius: 50px;
            font-size: 0.9rem;
            margin-bottom: 25px;
            border: 1px solid rgba(255,255,255,0.3);
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 700;
            margin-bottom: 20px;
            line-height: 1.1;
            text-shadow: 0 2px 20px rgba(0,0,0,0.2);
        }

        .hero h1 span {
            color: var(--accent-light);
        }

        .hero p {
            font-size: 1.3rem;
            opacity: 0.95;
            max-width: 700px;
            margin: 0 auto 40px;
            font-weight: 300;
        }

        .hero-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 16px 40px;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 700;
            text-decoration: none;
            transition: all 0.3s;
            cursor: pointer;
            border: none;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        .btn-primary {
            background: var(--accent);
            color: white;
            box-shadow: 0 10px 30px rgba(255,111,0,0.3);
        }

        .btn-primary:hover {
            background: var(--accent-light);
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(255,111,0,0.4);
        }

        .btn-outline {
            background: transparent;
            color: white;
            border: 2px solid rgba(255,255,255,0.5);
        }

        .btn-outline:hover {
            background: rgba(255,255,255,0.1);
            border-color: white;
        }

        /* Stats Bar */
        .stats-bar {
            background: var(--white);
            padding: 50px 30px;
            margin-top: -50px;
            position: relative;
            z-index: 2;
            max-width: 1000px;
            margin-left: auto;
            margin-right: auto;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            text-align: center;
        }

        .stat-item h3 {
            font-size: 3rem;
            color: var(--primary);
            font-weight: 700;
        }

        .stat-item p {
            color: var(--text-light);
            font-weight: 600;
            margin-top: 5px;
        }

        /* Sections */
        section {
            padding: 100px 30px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-header h2 {
            font-size: 2.8rem;
            color: var(--primary-dark);
            margin-bottom: 15px;
        }

        .section-header p {
            color: var(--text-light);
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto;
        }

        .divider {
            width: 80px;
            height: 4px;
            background: var(--accent);
            margin: 20px auto;
            border-radius: 2px;
        }

        /* About Section */
        .about {
            background: var(--warm);
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .about-image {
            position: relative;
        }

        .about-image img {
            width: 100%;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
        }

        .about-image::before {
            content: '';
            position: absolute;
            top: -20px;
            left: -20px;
            width: 100%;
            height: 100%;
            border: 3px solid var(--accent);
            border-radius: var(--radius);
            z-index: -1;
        }

        .about-content h3 {
            font-size: 2.2rem;
            color: var(--primary-dark);
            margin-bottom: 20px;
        }

        .about-content p {
            color: var(--text-light);
            margin-bottom: 20px;
            font-size: 1.05rem;
        }

        .mission-list {
            list-style: none;
            margin-top: 30px;
        }

        .mission-list li {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 20px;
            font-weight: 600;
            color: var(--text-dark);
        }

        .mission-list i {
            width: 45px;
            height: 45px;
            background: var(--primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.1rem;
            flex-shrink: 0;
        }

        /* Impact Section */
        .impact-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .impact-card {
            background: white;
            border-radius: var(--radius);
            overflow: hidden;
            box-shadow: 0 5px 30px rgba(0,0,0,0.08);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .impact-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.12);
        }

        .impact-card-img {
            height: 220px;
            overflow: hidden;
        }

        .impact-card-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .impact-card:hover .impact-card-img img {
            transform: scale(1.1);
        }

        .impact-card-content {
            padding: 30px;
        }

        .impact-card-content h3 {
            font-size: 1.5rem;
            color: var(--primary-dark);
            margin-bottom: 12px;
        }

        .impact-card-content p {
            color: var(--text-light);
            font-size: 0.95rem;
        }

        .impact-icon {
            width: 60px;
            height: 60px;
            background: var(--warm);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
            font-size: 1.5rem;
            color: var(--accent);
        }

        /* Stories Section */
        .stories {
            background: linear-gradient(135deg, var(--primary-dark) 0%, var(--primary) 100%);
            color: white;
            text-align: center;
        }

        .stories h2 {
            color: white;
        }

        .stories .divider {
            background: var(--accent-light);
        }

        .story-quote {
            max-width: 800px;
            margin: 0 auto;
            font-size: 1.3rem;
            font-style: italic;
            line-height: 1.8;
            position: relative;
            padding: 0 40px;
        }

        .story-quote::before,
        .story-quote::after {
            font-size: 4rem;
            color: var(--accent);
            position: absolute;
            line-height: 1;
        }

        .story-quote::before {
            content: '"';
            top: -20px;
            left: 0;
        }

        .story-quote::after {
            content: '"';
            bottom: -40px;
            right: 0;
        }

        .story-author {
            margin-top: 40px;
            font-weight: 700;
            color: var(--accent-light);
        }

        /* Donation Section */
        .donation {
            background: var(--warm);
        }

        .donation-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: start;
        }

        .donation-info h3 {
            font-size: 2rem;
            color: var(--primary-dark);
            margin-bottom: 20px;
        }

        .donation-info p {
            color: var(--text-light);
            margin-bottom: 30px;
            font-size: 1.05rem;
        }

        .donation-amounts {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
            margin-bottom: 30px;
        }

        .amount-btn {
            padding: 20px;
            background: white;
            border: 2px solid #e0e0e0;
            border-radius: 12px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s;
        }

        .amount-btn:hover,
        .amount-btn.active {
            border-color: var(--accent);
            background: var(--accent);
            color: white;
            transform: scale(1.05);
        }

        .amount-btn .currency {
            font-size: 0.9rem;
            opacity: 0.8;
        }

        .amount-btn .value {
            font-size: 1.8rem;
            font-weight: 700;
            display: block;
            margin-top: 5px;
        }

        .custom-amount {
            width: 100%;
            padding: 18px;
            border: 2px solid #e0e0e0;
            border-radius: 12px;
            font-size: 1.1rem;
            margin-bottom: 20px;
            outline: none;
            transition: border-color 0.3s;
        }

        .custom-amount:focus {
            border-color: var(--accent);
        }

        .donate-btn-main {
            width: 100%;
            padding: 20px;
            background: var(--accent);
            color: white;
            border: none;
            border-radius: 12px;
            font-size: 1.2rem;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }

        .donate-btn-main:hover {
            background: var(--accent-light);
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(255,111,0,0.3);
        }

        /* Donation Steps Card */
        .steps-card {
            background: white;
            border-radius: var(--radius);
            padding: 40px;
            box-shadow: var(--shadow);
            position: sticky;
            top: 100px;
        }

        .steps-card h3 {
            font-size: 1.5rem;
            color: var(--primary-dark);
            margin-bottom: 30px;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .steps-card h3 i {
            color: var(--accent);
        }

        .step {
            display: flex;
            gap: 20px;
            margin-bottom: 30px;
            padding-bottom: 30px;
            border-bottom: 1px solid #eee;
        }

        .step:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }

        .step-number {
            width: 45px;
            height: 45px;
            background: var(--primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            font-size: 1.1rem;
            flex-shrink: 0;
        }

        .step-content h4 {
            font-size: 1.1rem;
            color: var(--text-dark);
            margin-bottom: 8px;
        }

        .step-content p {
            color: var(--text-light);
            font-size: 0.95rem;
            line-height: 1.6;
        }

        .step-content code {
            background: #f5f5f5;
            padding: 2px 8px;
            border-radius: 4px;
            font-family: monospace;
            color: var(--primary-dark);
            font-weight: 600;
        }

        .app-store-badges {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .app-badge {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: var(--text-dark);
            color: white;
            padding: 12px 20px;
            border-radius: 10px;
            text-decoration: none;
            font-size: 0.85rem;
            transition: transform 0.3s;
        }

        .app-badge:hover {
            transform: scale(1.05);
        }

        .app-badge i {
            font-size: 1.5rem;
        }

        .app-badge span {
            display: flex;
            flex-direction: column;
        }

        .app-badge strong {
            font-size: 1rem;
        }

        /* Modal */
        .modal-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0,0,0,0.7);
            z-index: 2000;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .modal-overlay.active {
            display: flex;
        }

        .modal {
            background: white;
            border-radius: var(--radius);
            max-width: 600px;
            width: 100%;
            max-height: 90vh;
            overflow-y: auto;
            padding: 50px;
            position: relative;
            animation: modalIn 0.3s ease;
        }

        @keyframes modalIn {
            from {
                opacity: 0;
                transform: scale(0.9) translateY(20px);
            }
            to {
                opacity: 1;
                transform: scale(1) translateY(0);
            }
        }

        .modal-close {
            position: absolute;
            top: 20px;
            right: 25px;
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--text-light);
            transition: color 0.3s;
        }

        .modal-close:hover {
            color: var(--text-dark);
        }

        .modal h2 {
            font-size: 2rem;
            color: var(--primary-dark);
            margin-bottom: 10px;
        }

        .modal-subtitle {
            color: var(--text-light);
            margin-bottom: 30px;
        }

        .remitly-steps {
            background: #f8f9fa;
            border-radius: 12px;
            padding: 30px;
            margin-bottom: 30px;
        }

        .remitly-step {
            display: flex;
            gap: 15px;
            margin-bottom: 25px;
        }

        .remitly-step:last-child {
            margin-bottom: 0;
        }

        .remitly-step-num {
            width: 35px;
            height: 35px;
            background: var(--accent);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            font-size: 0.9rem;
            flex-shrink: 0;
        }

        .remitly-step-content h4 {
            font-size: 1rem;
            color: var(--text-dark);
            margin-bottom: 5px;
        }

        .remitly-step-content p {
            color: var(--text-light);
            font-size: 0.9rem;
        }

        .details-box {
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
            color: white;
            padding: 30px;
            border-radius: 12px;
            margin-bottom: 25px;
        }

        .details-box h4 {
            font-size: 1.1rem;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .detail-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 0;
            border-bottom: 1px solid rgba(255,255,255,0.2);
        }

        .detail-row:last-child {
            border-bottom: none;
        }

        .detail-label {
            font-size: 0.9rem;
            opacity: 0.9;
        }

        .detail-value {
            font-weight: 700;
            font-size: 1rem;
        }

        .copy-btn {
            background: rgba(255,255,255,0.2);
            border: none;
            color: white;
            padding: 5px 12px;
            border-radius: 6px;
            cursor: pointer;
            font-size: 0.8rem;
            margin-left: 10px;
            transition: background 0.3s;
        }

        .copy-btn:hover {
            background: rgba(255,255,255,0.3);
        }

        .modal-apps {
            text-align: center;
        }

        .modal-apps p {
            color: var(--text-light);
            margin-bottom: 15px;
            font-size: 0.95rem;
        }

        /* Footer */
        footer {
            background: var(--text-dark);
            color: white;
            padding: 60px 30px 30px;
        }

        .footer-grid {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 50px;
            margin-bottom: 50px;
        }

        .footer-brand h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--accent-light);
        }

        .footer-brand p {
            color: #aaa;
            font-size: 0.95rem;
            line-height: 1.7;
        }

        .footer-links h4 {
            font-size: 1.1rem;
            margin-bottom: 20px;
            color: white;
        }

        .footer-links ul {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 12px;
        }

        .footer-links a {
            color: #aaa;
            text-decoration: none;
            transition: color 0.3s;
            font-size: 0.95rem;
        }

        .footer-links a:hover {
            color: var(--accent-light);
        }

        .footer-bottom {
            max-width: 1200px;
            margin: 0 auto;
            padding-top: 30px;
            border-top: 1px solid #333;
            text-align: center;
            color: #666;
            font-size: 0.9rem;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-links a {
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            transition: all 0.3s;
        }

        .social-links a:hover {
            background: var(--accent);
            transform: translateY(-3px);
        }

        /* Mobile Menu */
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--text-dark);
        }

        /* Responsive */
        @media (max-width: 968px) {
            .about-grid,
            .donation-grid {
                grid-template-columns: 1fr;
            }

            .footer-grid {
                grid-template-columns: 1fr 1fr;
            }

            .hero h1 {
                font-size: 2.8rem;
            }

            .nav-links {
                display: none;
            }

            .mobile-menu-btn {
                display: block;
            }
        }

        @media (max-width: 600px) {
            .hero h1 {
                font-size: 2.2rem;
            }

            .hero p {
                font-size: 1.1rem;
            }

            .stats-bar {
                grid-template-columns: 1fr 1fr;
                gap: 20px;
            }

            .stat-item h3 {
                font-size: 2rem;
            }

            .footer-grid {
                grid-template-columns: 1fr;
                gap: 30px;
            }

            .modal {
                padding: 30px 20px;
            }

            .donation-amounts {
                grid-template-columns: 1fr;
            }
        }

        /* Scroll animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s ease, transform 0.8s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* Toast notification */
        .toast {
            position: fixed;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%) translateY(100px);
            background: var(--primary-dark);
            color: white;
            padding: 15px 30px;
            border-radius: 50px;
            font-weight: 600;
            z-index: 3000;
            opacity: 0;
            transition: all 0.4s ease;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        .toast.show {
            opacity: 1;
            transform: translateX(-50%) translateY(0);
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <div class="logo">
                <i class="fas fa-hands-holding-heart"></i>
                Gloria Wamuyu Ministries
            </div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About Us</a></li>
                <li><a href="#impact">Our Impact</a></li>
                <li><a href="#stories">Stories</a></li>
                <li><a href="#donate" class="donate-nav-btn"><i class="fas fa-heart"></i> Donate Now</a></li>
            </ul>
            <button class="mobile-menu-btn" onclick="toggleMobileMenu()">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <div class="hero-badge">
                <i class="fas fa-star"></i> Trusted by Supporters Worldwide
            </div>
            <h1>Every Child Deserves <span>Hope</span>, <span>Food</span> & <span>Education</span></h1>
            <p>Join Gloria Wamuyu Ministries in transforming the lives of over 500 vulnerable children in Kenya. Together, we provide food, clothing, and education — giving them the future they deserve.</p>
            <div class="hero-buttons">
                <a href="#donate" class="btn btn-primary">
                    <i class="fas fa-heart"></i> Make a Donation
                </a>
                <a href="#about" class="btn btn-outline">
                    <i class="fas fa-play-circle"></i> Learn Our Story
                </a>
            </div>
        </div>
    </section>

    <!-- Stats Bar -->
    <div class="stats-bar">
        <div class="stat-item">
            <h3>500+</h3>
            <p>Children Supported</p>
        </div>
        <div class="stat-item">
            <h3>3</h3>
            <p>Core Programs</p>
        </div>
        <div class="stat-item">
            <h3>100%</h3>
            <p>Goes to the Children</p>
        </div>
        <div class="stat-item">
            <h3>Kenya</h3>
            <p>Based in East Africa</p>
        </div>
    </div>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <div class="about-grid fade-in">
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1509099836639-18ba1795216d?w=800&h=600&fit=crop" alt="Children in Kenya">
                </div>
                <div class="about-content">
                    <h3>Who We Are</h3>
                    <p>Gloria Wamuyu Ministries is a faith-based charitable organization dedicated to uplifting vulnerable children across Kenya. Founded with a heart of compassion, we believe every child — regardless of their background — deserves access to life's basic necessities.</p>
                    <p>Through the generous support of donors like you, we have been able to reach over 500 children, providing them not just with survival, but with dignity, hope, and a pathway to a brighter future.</p>

                    <ul class="mission-list">
                        <li>
                            <i class="fas fa-utensils"></i>
                            <span><strong>Feeding Program</strong> — Nutritious daily meals for children who would otherwise go hungry</span>
                        </li>
                        <li>
                            <i class="fas fa-tshirt"></i>
                            <span><strong>Clothing Support</strong> — Clean, warm clothing and school uniforms for dignity and comfort</span>
                        </li>
                        <li>
                            <i class="fas fa-graduation-cap"></i>
                            <span><strong>Education Access</strong> — School fees, supplies, and resources to keep children in school</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Impact Section -->
    <section id="impact">
        <div class="container">
            <div class="section-header fade-in">
                <h2>Our Impact</h2>
                <div class="divider"></div>
                <p>See how your contributions directly transform lives across our three core programs</p>
            </div>
            <div class="impact-cards">
                <div class="impact-card fade-in">
                    <div class="impact-card-img">
                        <img src="https://images.unsplash.com/photo-1542810634-71277d95dcbb?w=600&h=400&fit=crop" alt="Feeding Program">
                    </div>
                    <div class="impact-card-content">
                        <div class="impact-icon">
                            <i class="fas fa-utensils"></i>
                        </div>
                        <h3>Daily Feeding Program</h3>
                        <p>We provide nutritious, balanced meals to over 500 children every single day. For many, this is their only guaranteed meal. Your donation ensures no child goes to bed hungry.</p>
                    </div>
                </div>
                <div class="impact-card fade-in">
                    <div class="impact-card-img">
                        <img src="https://images.unsplash.com/photo-1516627145497-ae6968895b74?w=600&h=400&fit=crop" alt="Clothing Support">
                    </div>
                    <div class="impact-card-content">
                        <div class="impact-icon">
                            <i class="fas fa-tshirt"></i>
                        </div>
                        <h3>Clothing & Uniforms</h3>
                        <p>Clean clothing and school uniforms restore dignity and confidence. We distribute seasonal clothing, shoes, and required school attire so children can attend class with pride.</p>
                    </div>
                </div>
                <div class="impact-card fade-in">
                    <div class="impact-card-img">
                        <img src="https://images.unsplash.com/photo-1497633762265-9d179a990aa6?w=600&h=400&fit=crop" alt="Education">
                    </div>
                    <div class="impact-card-content">
                        <div class="impact-icon">
                            <i class="fas fa-graduation-cap"></i>
                        </div>
                        <h3>Education & Schooling</h3>
                        <p>Education breaks the cycle of poverty. We pay school fees, provide books, stationery, and learning materials — giving over 500 children the chance to learn, grow, and dream.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Stories Section -->
    <section class="stories" id="stories">
        <div class="container">
            <div class="section-header fade-in">
                <h2>Stories of Hope</h2>
                <div class="divider"></div>
            </div>
            <div class="story-quote fade-in">
                Before Gloria Wamuyu Ministries found me, I used to miss school because I had no uniform and no food to eat. Today, I have both — and I am one of the top students in my class. This ministry didn't just feed me; it gave me a future.
            </div>
            <div class="story-author fade-in">— A Child Beneficiary, Kenya</div>
        </div>
    </section>

    <!-- Donation Section -->
    <section class="donation" id="donate">
        <div class="container">
            <div class="section-header fade-in">
                <h2>Make a Difference Today</h2>
                <div class="divider"></div>
                <p>Your generous donation goes directly to feeding, clothing, and educating children in Kenya. Every contribution counts.</p>
            </div>
            <div class="donation-grid">
                <div class="donation-info fade-in">
                    <h3>Choose Your Impact</h3>
                    <p>Select a donation amount or enter a custom amount. Your gift will be sent securely via Remitly to our M-Pesa account in Kenya.</p>

                    <div class="donation-amounts">
                        <div class="amount-btn" onclick="selectAmount(this, 25)">
                            <span class="currency">USD</span>
                            <span class="value">$25</span>
                        </div>
                        <div class="amount-btn" onclick="selectAmount(this, 50)">
                            <span class="currency">USD</span>
                            <span class="value">$50</span>
                        </div>
                        <div class="amount-btn" onclick="selectAmount(this, 100)">
                            <span class="currency">USD</span>
                            <span class="value">$100</span>
                        </div>
                        <div class="amount-btn" onclick="selectAmount(this, 250)">
                            <span class="currency">USD</span>
                            <span class="value">$250</span>
                        </div>
                    </div>

                    <input type="number" class="custom-amount" id="customAmount" placeholder="Or enter a custom amount (USD)" oninput="clearSelection()">

                    <button class="donate-btn-main" onclick="openDonationModal()">
                        <i class="fas fa-heart"></i> Proceed to Donate
                    </button>
                </div>

                <div class="steps-card fade-in">
                    <h3><i class="fas fa-mobile-alt"></i> How to Donate via Remitly</h3>

                    <div class="step">
                        <div class="step-number">1</div>
                        <div class="step-content">
                            <h4>Download Remitly</h4>
                            <p>Get the Remitly app from the App Store or Google Play. It's free to download and trusted by millions worldwide.</p>
                            <div class="app-store-badges">
                                <a href="https://apps.apple.com/us/app/remitly-send-money-transfer/id969229981" target="_blank" class="app-badge">
                                    <i class="fab fa-apple"></i>
                                    <span>Download on the <strong>App Store</strong></span>
                                </a>
                            </div>
                        </div>
                    </div>

                    <div class="step">
                        <div class="step-number">2</div>
                        <div class="step-content">
                            <h4>Set Up Your Transfer</h4>
                            <p>Select <strong>Kenya</strong> as the destination country. Choose <strong>M-Pesa</strong> as the delivery method and <strong>Express</strong> for fastest delivery.</p>
                        </div>
                    </div>

                    <div class="step">
                        <div class="step-number">3</div>
                        <div class="step-content">
                            <h4>Enter Our Details</h4>
                            <p>Recipient Name: <code>Gloria Wamuyu Ministries</code><br>
                            M-Pesa Number: <code>+254 708 139 104</code><br>
                            Country: <code>Kenya</code></p>
                        </div>
                    </div>

                    <div class="step">
                        <div class="step-number">4</div>
                        <div class="step-content">
                            <h4>Send & Confirm</h4>
                            <p>Review your transfer details, pay securely, and your donation reaches us instantly. You'll receive a confirmation receipt.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Donation Modal -->
    <div class="modal-overlay" id="donationModal">
        <div class="modal">
            <button class="modal-close" onclick="closeDonationModal()">
                <i class="fas fa-times"></i>
            </button>

            <h2><i class="fas fa-heart" style="color: var(--accent);"></i> Complete Your Donation</h2>
            <p class="modal-subtitle">Follow these simple steps to send your gift securely via Remitly</p>

            <div class="remitly-steps">
                <div class="remitly-step">
                    <div class="remitly-step-num">1</div>
                    <div class="remitly-step-content">
                        <h4>Download the Remitly App</h4>
                        <p>Visit the App Store or Google Play and search for "Remitly". Install the free app and create your account in minutes.</p>
                    </div>
                </div>
                <div class="remitly-step">
                    <div class="remitly-step-num">2</div>
                    <div class="remitly-step-content">
                        <h4>Go to Remitly.com or Open the App</h4>
                        <p>Select <strong>Kenya</strong> as your destination country. Choose <strong>Mobile Money (M-Pesa)</strong> as the delivery method.</p>
                    </div>
                </div>
                <div class="remitly-step">
                    <div class="remitly-step-num">3</div>
                    <div class="remitly-step-content">
                        <h4>Choose Express Speed</h4>
                        <p>Select <strong>Express</strong> delivery for instant transfer. Your donation will reach us within minutes.</p>
                    </div>
                </div>
                <div class="remitly-step">
                    <div class="remitly-step-num">4</div>
                    <div class="remitly-step-content">
                        <h4>Enter Recipient Details</h4>
                        <p>Use the exact details below to ensure your donation reaches us safely.</p>
                    </div>
                </div>
            </div>

            <div class="details-box">
                <h4><i class="fas fa-info-circle"></i> Our Donation Details</h4>
                <div class="detail-row">
                    <span class="detail-label">Ministry Name</span>
                    <span class="detail-value">Gloria Wamuyu Ministries <button class="copy-btn" onclick="copyText('Gloria Wamuyu Ministries')">Copy</button></span>
                </div>
                <div class="detail-row">
                    <span class="detail-label">Country</span>
                    <span class="detail-value">Kenya <button class="copy-btn" onclick="copyText('Kenya')">Copy</button></span>
                </div>
                <div class="detail-row">
                    <span class="detail-label">M-Pesa Number</span>
                    <span class="detail-value">+254 708 139 104 <button class="copy-btn" onclick="copyText('+254708139104')">Copy</button></span>
                </div>
                <div class="detail-row">
                    <span class="detail-label">Delivery Method</span>
                    <span class="detail-value">M-Pesa (Mobile Money) <button class="copy-btn" onclick="copyText('M-Pesa')">Copy</button></span>
                </div>
                <div class="detail-row">
                    <span class="detail-label">Speed</span>
                    <span class="detail-value">Express (Instant) <button class="copy-btn" onclick="copyText('Express')">Copy</button></span>
                </div>
            </div>

            <div class="modal-apps">
                <p>Don't have the app yet?</p>
                <div class="app-store-badges" style="justify-content: center;">
                    <a href="https://apps.apple.com/us/app/remitly-send-money-transfer/id969229981" target="_blank" class="app-badge">
                        <i class="fab fa-apple"></i>
                        <span>Download on the <strong>App Store</strong></span>
                    </a>
                    <a href="https://play.google.com/store/apps/details?id=com.remitly.androidapp" target="_blank" class="app-badge">
                        <i class="fab fa-google-play"></i>
                        <span>Get it on <strong>Google Play</strong></span>
                    </a>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="footer-grid">
            <div class="footer-brand">
                <h3><i class="fas fa-hands-holding-heart"></i> Gloria Wamuyu Ministries</h3>
                <p>A charitable ministry dedicated to feeding, clothing, and educating vulnerable children in Kenya. Together, we can give every child the future they deserve.</p>
                <div class="social-links">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-youtube"></i></a>
                </div>
            </div>
            <div class="footer-links">
                <h4>Quick Links</h4>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#impact">Our Impact</a></li>
                    <li><a href="#stories">Stories</a></li>
                    <li><a href="#donate">Donate</a></li>
                </ul>
            </div>
            <div class="footer-links">
                <h4>Our Programs</h4>
                <ul>
                    <li><a href="#impact">Feeding Program</a></li>
                    <li><a href="#impact">Clothing Support</a></li>
                    <li><a href="#impact">Education Access</a></li>
                </ul>
            </div>
            <div class="footer-links">
                <h4>Contact</h4>
                <ul>
                    <li><a href="#"><i class="fas fa-phone"></i> +254 708 139 104</a></li>
                    <li><a href="#"><i class="fas fa-envelope"></i> info@gloriawamuyuministries.org</a></li>
                    <li><a href="#"><i class="fas fa-map-marker-alt"></i> Kenya, East Africa</a></li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2026 Gloria Wamuyu Ministries. All rights reserved. | Registered Charitable Organization in Kenya</p>
        </div>
    </footer>

    <!-- Toast -->
    <div class="toast" id="toast">Copied to clipboard!</div>

    <script>
        // Scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));

        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Amount selection
        let selectedAmount = null;

        function selectAmount(element, amount) {
            document.querySelectorAll('.amount-btn').forEach(btn => btn.classList.remove('active'));
            element.classList.add('active');
            selectedAmount = amount;
            document.getElementById('customAmount').value = '';
        }

        function clearSelection() {
            document.querySelectorAll('.amount-btn').forEach(btn => btn.classList.remove('active'));
            selectedAmount = null;
        }

        // Modal functions
        function openDonationModal() {
            const customVal = document.getElementById('customAmount').value;
            if (!selectedAmount && !customVal) {
                showToast('Please select or enter a donation amount first');
                return;
            }
            document.getElementById('donationModal').classList.add('active');
            document.body.style.overflow = 'hidden';
        }

        function closeDonationModal() {
            document.getElementById('donationModal').classList.remove('active');
            document.body.style.overflow = '';
        }

        // Close modal on overlay click
        document.getElementById('donationModal').addEventListener('click', function(e) {
            if (e.target === this) {
                closeDonationModal();
            }
        });

        // Copy function
        function copyText(text) {
            navigator.clipboard.writeText(text).then(() => {
                showToast('Copied: ' + text);
            }).catch(() => {
                // Fallback
                const textarea = document.createElement('textarea');
                textarea.value = text;
                document.body.appendChild(textarea);
                textarea.select();
                document.execCommand('copy');
                document.body.removeChild(textarea);
                showToast('Copied: ' + text);
            });
        }

        // Toast
        function showToast(message) {
            const toast = document.getElementById('toast');
            toast.textContent = message;
            toast.classList.add('show');
            setTimeout(() => {
                toast.classList.remove('show');
            }, 3000);
        }

        // Mobile menu
        function toggleMobileMenu() {
            const navLinks = document.querySelector('.nav-links');
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
            navLinks.style.position = 'absolute';
            navLinks.style.top = '70px';
            navLinks.style.left = '0';
            navLinks.style.right = '0';
            navLinks.style.background = 'white';
            navLinks.style.flexDirection = 'column';
            navLinks.style.padding = '20px';
            navLinks.style.boxShadow = '0 10px 30px rgba(0,0,0,0.1)';
        }

        // Navbar scroll effect
        window.addEventListener('scroll', () => {
            const nav = document.querySelector('nav');
            if (window.scrollY > 50) {
                nav.style.boxShadow = '0 2px 20px rgba(0,0,0,0.1)';
            } else {
                nav.style.boxShadow = '0 2px 20px rgba(0,0,0,0.05)';
            }
        });
    </script>
</body>
</html>

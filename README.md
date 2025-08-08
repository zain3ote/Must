<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Paisey Kamaye - Online Earning Platform</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #25D366;
            --secondary: #128C7E;
            --dark: #075E54;
            --light: #DCF8C6;
            --accent: #FFC107;
            --text: #333333;
            --white: #ffffff;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f9f9f9;
            color: var(--text);
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(135deg, var(--secondary), var(--dark));
            color: var(--white);
            padding: 1.5rem;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80') center/cover;
            opacity: 0.3;
            z-index: 0;
        }
        
        header h1, header p {
            position: relative;
            z-index: 1;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.3);
        }
        
        header h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }
        
        nav {
            display: flex;
            justify-content: center;
            background-color: var(--dark);
            padding: 1rem;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        nav a {
            color: var(--white);
            text-decoration: none;
            padding: 0.7rem 1.5rem;
            margin: 0 0.5rem;
            border-radius: 30px;
            transition: all 0.3s ease;
            font-weight: 500;
            display: flex;
            align-items: center;
        }
        
        nav a i {
            margin-right: 8px;
        }
        
        nav a:hover, nav a.active {
            background-color: var(--primary);
            color: var(--dark);
            transform: translateY(-2px);
        }
        
        .hero {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1521791136064-7986c2920216?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1469&q=80');
            height: 70vh;
            background-size: cover;
            background-position: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: var(--white);
            text-align: center;
            padding: 0 2rem;
        }
        
        .hero-content {
            max-width: 800px;
            animation: fadeIn 1s ease;
        }
        
        .hero h2 {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--primary);
            color: var(--dark);
            border: none;
            padding: 0.8rem 2rem;
            font-size: 1.1rem;
            border-radius: 30px;
            cursor: pointer;
            margin: 0.5rem;
            font-weight: 600;
            transition: all 0.3s ease;
            text-decoration: none;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .btn:hover {
            background-color: var(--accent);
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0,0,0,0.15);
        }
        
        .btn-secondary {
            background-color: transparent;
            color: var(--white);
            border: 2px solid var(--white);
        }
        
        .btn-secondary:hover {
            background-color: rgba(255,255,255,0.1);
            color: var(--white);
        }
        
        .container {
            max-width: 1200px;
            margin: 3rem auto;
            padding: 0 2rem;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
        }
        
        .section-title h2 {
            font-size: 2.2rem;
            color: var(--dark);
            display: inline-block;
            padding-bottom: 0.5rem;
        }
        
        .section-title h2::after {
            content: "";
            position: absolute;
            width: 80px;
            height: 3px;
            background-color: var(--primary);
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .earning-methods {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .method-card {
            background-color: var(--white);
            border-radius: 12px;
            padding: 2rem;
            box-shadow: 0 8px 20px rgba(0,0,0,0.08);
            transition: all 0.3s ease;
            text-align: center;
            border-top: 4px solid var(--primary);
        }
        
        .method-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 12px 25px rgba(0,0,0,0.12);
        }
        
        .method-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }
        
        .method-card h3 {
            color: var(--dark);
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }
        
        .method-card p {
            margin-bottom: 1.5rem;
            color: #666;
        }
        
        .method-card .earn-amount {
            display: inline-block;
            background-color: var(--light);
            color: var(--dark);
            padding: 0.3rem 1rem;
            border-radius: 20px;
            font-weight: 600;
            margin-bottom: 1.5rem;
        }
        
        .testimonials {
            margin-top: 5rem;
            background-color: var(--white);
            padding: 3rem 2rem;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .testimonial {
            background-color: var(--light);
            padding: 1.5rem;
            border-radius: 10px;
            position: relative;
            transition: all 0.3s ease;
        }
        
        .testimonial:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .testimonial::before {
            content: """;
            position: absolute;
            top: 10px;
            left: 15px;
            font-size: 4rem;
            color: rgba(0,0,0,0.05);
            font-family: Georgia, serif;
            line-height: 1;
        }
        
        .testimonial p {
            margin-bottom: 1rem;
            font-style: italic;
            position: relative;
            z-index: 1;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .testimonial-author img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            object-fit: cover;
            margin-right: 1rem;
            border: 3px solid var(--primary);
        }
        
        .author-info h4 {
            color: var(--dark);
            margin-bottom: 0.2rem;
        }
        
        .author-info p {
            color: #666;
            font-size: 0.9rem;
            font-style: normal;
        }
        
        .payment-methods {
            background-color: var(--white);
            padding: 3rem 2rem;
            border-radius: 12px;
            margin-top: 3rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            text-align: center;
        }
        
        .payment-icons {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .payment-icon {
            font-size: 3rem;
            color: var(--dark);
            transition: all 0.3s ease;
        }
        
        .payment-icon:hover {
            color: var(--primary);
            transform: scale(1.1);
        }
        
        .payment-icon img {
            height: 50px;
            width: auto;
            object-fit: contain;
        }
        
        .how-it-works {
            margin-top: 5rem;
        }
        
        .steps {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin-top: 3rem;
        }
        
        .step {
            flex: 1;
            min-width: 250px;
            text-align: center;
            padding: 0 1.5rem;
            margin-bottom: 2rem;
            position: relative;
        }
        
        .step-number {
            width: 60px;
            height: 60px;
            background-color: var(--primary);
            color: var(--white);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            font-weight: bold;
            margin: 0 auto 1.5rem;
            position: relative;
            z-index: 1;
        }
        
        .step:nth-child(1) .step-number {
            background-color: #FF5722;
        }
        
        .step:nth-child(2) .step-number {
            background-color: #2196F3;
        }
        
        .step:nth-child(3) .step-number {
            background-color: #9C27B0;
        }
        
        .step h3 {
            color: var(--dark);
            margin-bottom: 1rem;
        }
        
        .step p {
            color: #666;
        }
        
        footer {
            background: linear-gradient(135deg, var(--dark), #000);
            color: var(--white);
            padding: 3rem 2rem 1.5rem;
            margin-top: 5rem;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 1.5rem;
            position: relative;
            display: inline-block;
        }
        
        .footer-column h3::after {
            content: "";
            position: absolute;
            width: 50px;
            height: 2px;
            background-color: var(--primary);
            bottom: -8px;
            left: 0;
        }
        
        .footer-column p, .footer-column a {
            color: #ccc;
            margin-bottom: 1rem;
            display: block;
            transition: all 0.3s ease;
            text-decoration: none;
        }
        
        .footer-column a:hover {
            color: var(--primary);
            padding-left: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .social-links a {
            width: 40px;
            height: 40px;
            background-color: rgba(255,255,255,0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background-color: var(--primary);
            color: var(--dark);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 2rem;
            margin-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #aaa;
            font-size: 0.9rem;
        }
        
        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.5);
            animation: fadeIn 0.3s;
        }
        
        .modal-content {
            background-color: var(--white);
            margin: 5% auto;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.2);
            max-width: 500px;
            width: 90%;
            position: relative;
            animation: slideDown 0.4s;
        }
        
        .close-btn {
            position: absolute;
            top: 15px;
            right: 20px;
            font-size: 1.5rem;
            color: #aaa;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .close-btn:hover {
            color: var(--dark);
            transform: rotate(90deg);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--dark);
            font-weight: 500;
        }
        
        .form-group input, .form-group select, .form-group textarea {
            width: 100%;
            padding: 0.8rem 1rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: all 0.3s;
        }
        
        .form-group input:focus, .form-group select:focus, .form-group textarea:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(37, 211, 102, 0.2);
        }
        
        .submit-btn {
            width: 100%;
            padding: 0.8rem;
            background-color: var(--primary);
            color: var(--white);
            border: none;
            border-radius: 5px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .submit-btn:hover {
            background-color: var(--secondary);
        }
        
        /* Owner Photo Styles */
        .owner-photo-container {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
        }
        
        .owner-photo {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--primary);
            margin-right: 1rem;
        }
        
        .owner-info h4 {
            color: var(--white);
            margin-bottom: 0.2rem;
        }
        
        .owner-info p {
            color: #ccc;
            font-size: 0.9rem;
        }
        
        /* Method Fields */
        .method-fields {
            display: none;
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes slideDown {
            from { 
                opacity: 0;
                transform: translateY(-50px);
            }
            to { 
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        /* Responsive Styles */
        @media (max-width: 992px) {
            .hero h2 {
                font-size: 2.5rem;
            }
            
            .steps {
                justify-content: center;
            }
            
            .step {
                flex: 0 0 50%;
                margin-bottom: 3rem;
            }
        }
        
        @media (max-width: 768px) {
            header h1 {
                font-size: 2rem;
            }
            
            .hero {
                height: 60vh;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            nav {
                flex-wrap: wrap;
            }
            
            nav a {
                padding: 0.5rem 1rem;
                margin: 0.2rem;
                font-size: 0.9rem;
            }
            
            .method-card {
                padding: 1.5rem;
            }
            
            .step {
                flex: 0 0 100%;
            }
        }
        
        @media (max-width: 576px) {
            .hero {
                height: 70vh;
                padding: 0 1rem;
            }
            
            .hero h2 {
                font-size: 1.8rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .btn {
                padding: 0.7rem 1.5rem;
                font-size: 1rem;
            }
            
            .section-title h2 {
                font-size: 1.8rem;
            }
            
            .earning-methods {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1><i class="fas fa-coins"></i> Paisey Kamaye</h1>
        <p>Ghar baithe paise kamayein - Aasan tareeqay se!</p>
    </header>
    
    <nav>
        <a href="#home" class="active"><i class="fas fa-home"></i> Home</a>
        <a href="#methods"><i class="fas fa-money-bill-wave"></i> Earning Methods</a>
        <a href="#withdraw"><i class="fas fa-wallet"></i> Withdraw</a>
        <a href="#testimonials"><i class="fas fa-star"></i> Success Stories</a>
        <a href="#contact"><i class="fas fa-envelope"></i> Contact</a>
    </nav>
    
    <section class="hero" id="home">
        <div class="hero-content">
            <h2>Start Earning Money Online Today!</h2>
            <p>Join our platform and start making real money from home with simple tasks. No investment required!</p>
            <div class="hero-buttons">
                <a href="#" class="btn" id="signup-btn"><i class="fas fa-user-plus"></i> Sign Up Now - It's Free!</a>
                <a href="#methods" class="btn btn-secondary"><i class="fas fa-search"></i> Explore Methods</a>
            </div>
        </div>
    </section>
    
    <div class="container">
        <section id="methods">
            <div class="section-title">
                <h2>Popular Earning Methods</h2>
            </div>
            <div class="earning-methods">
                <div class="method-card">
                    <div class="method-icon">
                        <i class="fas fa-poll"></i>
                    </div>
                    <h3>Online Surveys</h3>
                    <p>Share your opinion and earn money by completing simple surveys from top brands.</p>
                    <div class="earn-amount">Earn Rs. 50 - Rs. 500 per survey</div>
                    <a href="#" class="btn start-method" data-method="surveys"><i class="fas fa-play"></i> Start Now</a>
                </div>
                
                <div class="method-card">
                    <div class="method-icon">
                        <i class="fas fa-ad"></i>
                    </div>
                    <h3>Watch Ads</h3>
                    <p>Earn money by watching short video advertisements from our partners.</p>
                    <div class="earn-amount">Earn Rs. 5 - Rs. 50 per ad</div>
                    <a href="#" class="btn start-method" data-method="watch-ads"><i class="fas fa-play"></i> Start Now</a>
                </div>
                
                <div class="method-card">
                    <div class="method-icon">
                        <i class="fas fa-user-friends"></i>
                    </div>
                    <h3>Refer Friends</h3>
                    <p>Invite your friends and earn 20% commission on their earnings for life!</p>
                    <div class="earn-amount">Unlimited earning potential</div>
                    <a href="#" class="btn start-method" data-method="refer-friends"><i class="fas fa-play"></i> Start Now</a>
                </div>
                
                <div class="method-card">
                    <div class="method-icon">
                        <i class="fas fa-keyboard"></i>
                    </div>
                    <h3>Data Entry</h3>
                    <p>Simple online data entry jobs that anyone can do. No special skills required.</p>
                    <div class="earn-amount">Earn Rs. 100 - Rs. 1000 per task</div>
                    <a href="#" class="btn start-method" data-method="data-entry"><i class="fas fa-play"></i> Start Now</a>
                </div>
                
                <div class="method-card">
                    <div class="method-icon">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3>App Testing</h3>
                    <p>Test new apps and websites and get paid for your valuable feedback.</p>
                    <div class="earn-amount">Earn Rs. 200 - Rs. 2000 per test</div>
                    <a href="#" class="btn start-method" data-method="app-testing"><i class="fas fa-play"></i> Start Now</a>
                </div>
                
                <div class="method-card">
                    <div class="method-icon">
                        <i class="fas fa-laptop-code"></i>
                    </div>
                    <h3>Freelancing</h3>
                    <p>Offer your skills and services to clients worldwide and earn big money.</p>
                    <div class="earn-amount">Earn Rs. 1000 - Rs. 50,000+ per project</div>
                    <a href="#" class="btn start-method" data-method="freelancing"><i class="fas fa-play"></i> Start Now</a>
                </div>
            </div>
        </section>
        
        <section class="how-it-works">
            <div class="section-title">
                <h2>How It Works</h2>
            </div>
            <div class="steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <h3>Sign Up Free</h3>
                    <p>Create your free account in just 2 minutes. No payment required.</p>
                </div>
                
                <div class="step">
                    <div class="step-number">2</div>
                    <h3>Choose Tasks</h3>
                    <p>Select from various earning methods that suit your skills and time.</p>
                </div>
                
                <div class="step">
                    <div class="step-number">3</div>
                    <h3>Earn & Withdraw</h3>
                    <p>Complete tasks and withdraw your earnings via multiple payment methods.</p>
                </div>
            </div>
        </section>
        
        <section class="testimonials" id="testimonials">
            <div class="section-title">
                <h2>Success Stories</h2>
            </div>
            <div class="testimonial-grid">
                <div class="testimonial">
                    <p>"I earned Rs. 25,000 in my first month just by completing surveys and watching ads. This platform changed my financial situation completely!"</p>
                    <div class="testimonial-author">
                        <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Ali">
                        <div class="author-info">
                            <h4>Ali Ahmed</h4>
                            <p>Karachi, 3 months with us</p>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial">
                    <p>"After losing my job, this website helped me earn enough to support my family. Last month I made Rs. 45,000!"</p>
                    <div class="testimonial-author">
                        <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Sana">
                        <div class="author-info">
                            <h4>Sana Khan</h4>
                            <p>Lahore, 6 months with us</p>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial">
                    <p>"I refer friends and earn passive income. Last month I made Rs. 35,000 without much effort. Highly recommended!"</p>
                    <div class="testimonial-author">
                        <img src="https://randomuser.me/api/portraits/men/75.jpg" alt="Ahmed">
                        <div class="author-info">
                            <h4>Ahmed Raza</h4>
                            <p>Islamabad, 1 year with us</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <section class="payment-methods" id="withdraw">
            <div class="section-title">
                <h2>Easy Withdrawal Methods</h2>
            </div>
            <p>Get your earnings quickly through these secure payment methods</p>
            <div class="payment-icons">
                <div class="payment-icon" title="Google Pay">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/53/Google_%22G%22_Logo.svg/2048px-Google_%22G%22_Logo.svg.png" alt="Google Pay">
                </div>
                <div class="payment-icon" title="JazzCash">
                    <img src="https://www.jazz.com.pk/images/jazzcash-logo.png" alt="JazzCash">
                </div>
                <div class="payment-icon" title="EasyPaisa">
                    <img src="https://www.easypaisa.com.pk/wp-content/themes/easypaisa/images/logo.svg" alt="EasyPaisa">
                </div>
                <div class="payment-icon" title="PayPal">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b5/PayPal.svg/2560px-PayPal.svg.png" alt="PayPal">
                </div>
                <div class="payment-icon" title="Bank Transfer">
                    <i class="fas fa-university"></i>
                </div>
            </div>
            <a href="#" class="btn" id="withdraw-btn" style="margin-top: 2rem;"><i class="fas fa-wallet"></i> Withdraw Now</a>
        </section>
        
        <section id="contact-form" style="margin-top: 5rem;">
            <div class="section-title">
                <h2>Direct Contact</h2>
            </div>
            <div style="background: white; padding: 2rem; border-radius: 10px; box-shadow: 0 5px 15px rgba(0,0,0,0.05);">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="contact-name">Your Name</label>
                        <input type="text" id="contact-name" name="contact-name" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="contact-email">Your Email</label>
                        <input type="email" id="contact-email" name="contact-email" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="contact-subject">Subject</label>
                        <input type="text" id="contact-subject" name="contact-subject" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="contact-message">Message</label>
                        <textarea id="contact-message" name="contact-message" rows="5" required></textarea>
                    </div>
                    
                    <button type="submit" class="submit-btn">
                        <i class="fas fa-paper-plane"></i> Send Message
                    </button>
                </form>
            </div>
        </section>
    </div>
    
    <footer id="contact">
        <div class="footer-content">
            <div class="footer-column">
                <h3>About Us</h3>
                <p>Paisey Kamaye is Pakistan's leading online earning platform, helping thousands of people make money from home since 2020.</p>
                <div class="social-links">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-youtube"></i></a>
                    <a href="#"><i class="fab fa-whatsapp"></i></a>
                </div>
            </div>
            
            <div class="footer-column">
                <h3>Quick Links</h3>
                <a href="#home"><i class="fas fa-chevron-right"></i> Home</a>
                <a href="#methods"><i class="fas fa-chevron-right"></i> Earning Methods</a>
                <a href="#withdraw"><i class="fas fa-chevron-right"></i> Withdraw Money</a>
                <a href="#testimonials"><i class="fas fa-chevron-right"></i> Success Stories</a>
                <a href="#"><i class="fas fa-chevron-right"></i> FAQ</a>
            </div>
            
            <div class="footer-column">
                <h3>Contact Us</h3>
                <p><i class="fas fa-envelope"></i> imamz9691@gmail.com</p>
                <p><i class="fas fa-phone"></i> 0300-1234567</p>
                <p><i class="fas fa-map-marker-alt"></i> Office #10, Commercial Area, Karachi, Pakistan</p>
                
                <div class="owner-photo-container" style="margin-top: 1.5rem;">
                    <img src="https://via.placeholder.com/80" alt="Owner Photo" class="owner-photo" id="owner-photo">
                    <div class="owner-info">
                        <h4>Syed Muhammad Zain Imam</h4>
                        <p>Founder & CEO</p>
                        <p style="font-size: 0.8rem;">Made in the United Kingdom | 2017-2020</p>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="copyright">
            <p>&copy; 2023 Paisey Kamaye. All Rights Reserved.</p>
        </div>
    </footer>
    
    <!-- Signup Modal -->
    <div id="signup-modal" class="modal">
        <div class="modal-content">
            <span class="close-btn">&times;</span>
            <h2 style="color: var(--dark); margin-bottom: 1.5rem; text-align: center;">Create Your Free Account</h2>
            <form id="signup-form">
                <div class="form-group">
                    <label for="name">Full Name</label>
                    <input type="text" id="name" name="name" required>
                </div>
                
                <div class="form-group">
                    <label for="email">Email Address</label>
                    <input type="email" id="email" name="email" required>
                </div>
                
                <div class="form-group">
                    <label for="phone">Phone Number</label>
                    <input type="tel" id="phone" name="phone" required>
                </div>
                
                <div class="form-group">
                    <label for="password">Create Password</label>
                    <input type="password" id="password" name="password" required>
                </div>
                
                <div class="form-group">
                    <label for="referral">Referral Code (Optional)</label>
                    <input type="text" id="referral" name="referral">
                </div>
                
                <button type="submit" class="submit-btn">Sign Up & Start Earning</button>
            </form>
        </div>
    </div>
    
    <!-- Withdraw Modal -->
    <div id="withdraw-modal" class="modal">
        <div class="modal-content">
            <span class="close-btn">&times;</span>
            <h2 style="color: var(--dark); margin-bottom: 1.5rem; text-align: center;">Withdraw Your Earnings</h2>
            <form id="withdraw-form">
                <div class="form-group">
                    <label for="withdraw-method">Payment Method</label>
                    <select id="withdraw-method" name="withdraw-method" required>
                        <option value="">Select Payment Method</option>
                        <option value="jazzcash">JazzCash (Recommended)</option>
                        <option value="google-pay">Google Pay</option>
                        <option value="easypaisa">EasyPaisa</option>
                        <option value="paypal">PayPal</option>
                        <option value="bank">Bank Transfer</option>
                    </select>
                </div>
                
                <div id="jazzcash-fields" class="method-fields">
                    <div class="form-group">
                        <label for="jazzcash-number">JazzCash Number</label>
                        <input type="text" id="jazzcash-number" name="jazzcash-number" placeholder="03020679993" value="03020679993" readonly>
                        <small style="color: var(--primary);">Note: All withdrawals go to this JazzCash number

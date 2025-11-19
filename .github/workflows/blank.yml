<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Elegant Lady - Damen-Sommerbekleidung</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #e75480;
            --secondary-color: #f8c8dc;
            --accent-color: #ffb6c1;
            --dark-color: #333;
            --light-color: #f9f9f9;
            --text-color: #555;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--light-color);
            color: var(--text-color);
            overflow-x: hidden;
            position: relative;
        }

        /* 3D Hintergrund */
        #bg-canvas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.7;
        }

        /* Header & Navigation */
        header {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            padding: 1rem 2rem;
            box-shadow: var(--shadow);
            position: relative;
            z-index: 100;
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 2.5rem;
            font-weight: bold;
            color: white;
            text-shadow: 3px 3px 5px rgba(0, 0, 0, 0.3);
            transform: perspective(500px) rotateX(10deg);
            transition: var(--transition);
        }

        .logo:hover {
            transform: perspective(500px) rotateX(0deg) scale(1.05);
            text-shadow: 5px 5px 10px rgba(0, 0, 0, 0.4);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 1.5rem;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            transition: var(--transition);
            position: relative;
            overflow: hidden;
        }

        nav ul li a:before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.2);
            transition: var(--transition);
        }

        nav ul li a:hover:before {
            left: 100%;
        }

        nav ul li a:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: translateY(-3px);
        }

        .header-actions {
            display: flex;
            gap: 1rem;
        }

        .cart-toggle, .favorites-toggle {
            background: rgba(255, 255, 255, 0.2);
            border: none;
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            position: relative;
            transition: var(--transition);
            transform: perspective(500px) rotateY(5deg);
        }

        .cart-toggle:hover, .favorites-toggle:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: perspective(500px) rotateY(0deg) scale(1.1);
        }

        #cart-count {
            position: absolute;
            top: -5px;
            right: -5px;
            background: var(--accent-color);
            color: white;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
            font-weight: bold;
        }

        /* Login-Bereich */
        .login-container {
            position: fixed;
            top: 20px;
            left: 20px;
            z-index: 1000;
        }

        .login-toggle {
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            color: white;
            border: none;
            border-radius: 50%;
            width: 60px;
            height: 60px;
            font-size: 1.5rem;
            cursor: pointer;
            box-shadow: var(--shadow);
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            transform: perspective(500px) rotateY(10deg);
        }

        .login-toggle:hover {
            transform: perspective(500px) rotateY(0deg) scale(1.1);
        }

        .login-form {
            position: absolute;
            top: 70px;
            left: 0;
            background: white;
            padding: 1.5rem;
            border-radius: 10px;
            box-shadow: var(--shadow);
            width: 300px;
            display: none;
            transform: perspective(500px) rotateX(-5deg);
            transition: var(--transition);
        }

        .login-form.active {
            display: block;
            transform: perspective(500px) rotateX(0deg);
        }

        .login-form h3 {
            margin-bottom: 1rem;
            color: var(--primary-color);
            text-align: center;
        }

        .login-form input {
            width: 100%;
            padding: 0.8rem;
            margin-bottom: 1rem;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        .login-form button {
            width: 100%;
            padding: 0.8rem;
            background: var(--primary-color);
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: var(--transition);
        }

        .login-form button:hover {
            background: var(--accent-color);
        }

        .login-form p {
            text-align: center;
            margin-top: 1rem;
            font-size: 0.9rem;
        }

        .login-form p a {
            color: var(--primary-color);
            text-decoration: none;
        }

        .user-profile {
            display: none;
            align-items: center;
            background: white;
            padding: 0.5rem 1rem;
            border-radius: 30px;
            box-shadow: var(--shadow);
        }

        .user-profile img {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            margin-right: 10px;
            object-fit: cover;
        }

        .user-profile span {
            font-weight: 600;
            color: var(--primary-color);
        }

        /* Hauptinhalt */
        main {
            padding: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            margin-bottom: 2rem;
            color: var(--primary-color);
            font-size: 2rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
            transform: perspective(500px) rotateX(5deg);
        }

        /* Produktbereich */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .product-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            position: relative;
            transform: perspective(500px) rotateY(5deg);
        }

        .product-card:hover {
            transform: perspective(500px) rotateY(0deg) translateY(-10px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
        }

        .product-image {
            height: 250px;
            width: 100%;
            background-size: cover;
            background-position: center;
            position: relative;
        }

        .product-actions {
            position: absolute;
            top: 10px;
            right: 10px;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .product-actions button {
            background: white;
            border: none;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .product-actions button:hover {
            background: var(--primary-color);
            color: white;
        }

        .product-info {
            padding: 1.5rem;
        }

        .product-title {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            color: var(--dark-color);
        }

        .product-price {
            font-weight: bold;
            color: var(--primary-color);
            font-size: 1.3rem;
            margin-bottom: 1rem;
        }

        .color-selector {
            display: flex;
            gap: 10px;
            margin-bottom: 1rem;
        }

        .color-option {
            width: 25px;
            height: 25px;
            border-radius: 50%;
            cursor: pointer;
            border: 2px solid transparent;
            transition: var(--transition);
        }

        .color-option.active {
            border-color: var(--dark-color);
            transform: scale(1.2);
        }

        .size-selector {
            display: flex;
            gap: 10px;
            margin-bottom: 1rem;
        }

        .size-option {
            width: 35px;
            height: 35px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: var(--light-color);
            cursor: pointer;
            transition: var(--transition);
            font-weight: 600;
        }

        .size-option.active {
            background: var(--primary-color);
            color: white;
            transform: scale(1.1);
        }

        .add-to-cart {
            width: 100%;
            padding: 0.8rem;
            background: var(--primary-color);
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: var(--transition);
            font-weight: 600;
        }

        .add-to-cart:hover {
            background: var(--accent-color);
            transform: translateY(-3px);
        }

        /* Warenkorb */
        .cart-container {
            position: fixed;
            top: 0;
            right: -400px;
            width: 400px;
            height: 100vh;
            background: white;
            box-shadow: -5px 0 15px rgba(0, 0, 0, 0.1);
            transition: var(--transition);
            z-index: 1000;
            padding: 2rem;
            overflow-y: auto;
        }

        .cart-container.active {
            right: 0;
        }

        .cart-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid #eee;
        }

        .cart-header h2 {
            color: var(--primary-color);
        }

        .close-cart {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--text-color);
        }

        .cart-items {
            margin-bottom: 2rem;
        }

        .cart-item {
            display: flex;
            margin-bottom: 1.5rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid #eee;
        }

        .cart-item-image {
            width: 80px;
            height: 80px;
            background-size: cover;
            background-position: center;
            border-radius: 5px;
            margin-right: 1rem;
        }

        .cart-item-details {
            flex: 1;
        }

        .cart-item-title {
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .cart-item-price {
            color: var(--primary-color);
            font-weight: 600;
        }

        .cart-item-actions {
            display: flex;
            align-items: center;
            margin-top: 0.5rem;
        }

        .quantity-btn {
            width: 30px;
            height: 30px;
            background: var(--light-color);
            border: none;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
        }

        .quantity {
            margin: 0 10px;
        }

        .remove-item {
            margin-left: auto;
            color: var(--primary-color);
            background: none;
            border: none;
            cursor: pointer;
        }

        .cart-total {
            display: flex;
            justify-content: space-between;
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 2rem;
            padding-top: 1rem;
            border-top: 1px solid #eee;
        }

        .checkout-btn {
            width: 100%;
            padding: 1rem;
            background: var(--primary-color);
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
        }

        .checkout-btn:hover {
            background: var(--accent-color);
        }

        /* Favoriten */
        .favorites-container {
            position: fixed;
            top: 0;
            right: -400px;
            width: 400px;
            height: 100vh;
            background: white;
            box-shadow: -5px 0 15px rgba(0, 0, 0, 0.1);
            transition: var(--transition);
            z-index: 1000;
            padding: 2rem;
            overflow-y: auto;
        }

        .favorites-container.active {
            right: 0;
        }

        /* Zahlungsmethoden */
        .payment-methods {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 1rem;
            margin-bottom: 2rem;
        }

        .payment-method {
            background: white;
            border-radius: 10px;
            padding: 1.5rem;
            text-align: center;
            cursor: pointer;
            transition: var(--transition);
            box-shadow: var(--shadow);
            transform: perspective(500px) rotateY(5deg);
            border: 2px solid transparent;
        }

        .payment-method:hover {
            transform: perspective(500px) rotateY(0deg) translateY(-5px);
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
        }

        .payment-method.active {
            border-color: var(--primary-color);
            transform: perspective(500px) rotateY(0deg) scale(1.05);
        }

        .payment-icon {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
            color: var(--primary-color);
        }

        .payment-name {
            font-weight: 600;
            color: var(--dark-color);
        }

        /* Zahlungsformular */
        .payment-form {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: var(--shadow);
            margin-bottom: 3rem;
            transform: perspective(500px) rotateX(5deg);
            transition: var(--transition);
        }

        .payment-form.active {
            transform: perspective(500px) rotateX(0deg);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
        }

        .form-group input {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
        }

        .payment-submit {
            width: 100%;
            padding: 1rem;
            background: var(--primary-color);
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
        }

        .payment-submit:hover {
            background: var(--accent-color);
        }

        /* Bewertungssystem */
        .reviews-section {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: var(--shadow);
            margin-bottom: 3rem;
        }

        .review-form {
            margin-bottom: 2rem;
            padding: 1.5rem;
            background: var(--light-color);
            border-radius: 10px;
        }

        .review-form h3 {
            margin-bottom: 1rem;
            color: var(--primary-color);
        }

        .rating-stars {
            display: flex;
            gap: 5px;
            margin-bottom: 1rem;
        }

        .star {
            color: #ddd;
            cursor: pointer;
            font-size: 1.5rem;
            transition: var(--transition);
        }

        .star.active {
            color: gold;
        }

        .review-form textarea {
            width: 100%;
            padding: 1rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            margin-bottom: 1rem;
            resize: vertical;
            min-height: 100px;
        }

        .review-form button {
            padding: 0.8rem 1.5rem;
            background: var(--primary-color);
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: var(--transition);
        }

        .review-form button:hover {
            background: var(--accent-color);
        }

        .reviews-list {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .review-item {
            padding: 1.5rem;
            background: var(--light-color);
            border-radius: 10px;
        }

        .review-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
        }

        .review-author {
            font-weight: 600;
            color: var(--primary-color);
        }

        .review-rating {
            color: gold;
        }

        .review-date {
            color: #999;
            font-size: 0.9rem;
        }

        /* Serviceanfrage */
        .service-request {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: var(--shadow);
            margin-bottom: 3rem;
        }

        .service-request h2 {
            margin-bottom: 1.5rem;
            color: var(--primary-color);
            text-align: center;
        }

        .service-form {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
        }

        .form-group {
            margin-bottom: 1rem;
        }

        .form-group.full-width {
            grid-column: 1 / -1;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        .submit-btn {
            grid-column: 1 / -1;
            padding: 1rem;
            background: var(--primary-color);
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
        }

        .submit-btn:hover {
            background: var(--accent-color);
        }

        /* Footer */
        footer {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 3rem 2rem;
            text-align: center;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .footer-section h3 {
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
        }

        .footer-section p,
        .footer-section a {
            color: rgba(255, 255, 255, 0.8);
            margin-bottom: 0.5rem;
            display: block;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-section a:hover {
            color: white;
        }

        .social-icons {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 1rem;
        }

        .social-icons a {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
        }

        .social-icons a:hover {
            background: white;
            color: var(--primary-color);
        }

        .copyright {
            margin-top: 2rem;
            padding-top: 1rem;
            border-top: 1px solid rgba(255, 255, 255, 0.2);
        }

        /* Overlay */
        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            z-index: 999;
            display: none;
        }

        .overlay.active {
            display: block;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                gap: 1rem;
            }

            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }

            .login-container {
                position: static;
                margin-top: 1rem;
            }

            .cart-container,
            .favorites-container {
                width: 100%;
                right: -100%;
            }

            .service-form {
                grid-template-columns: 1fr;
            }

            .payment-methods {
                grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            }

            .form-row {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- 3D Hintergrund -->
    <canvas id="bg-canvas"></canvas>

    <!-- Overlay für modale Fenster -->
    <div class="overlay" id="overlay"></div>

    <!-- Header -->
    <header>
        <div class="header-container">
            <div class="logo">Elegant Lady</div>
            <nav>
                <ul>
                    <li><a href="#home">Startseite</a></li>
                    <li><a href="#products">Produkte</a></li>
                    <li><a href="#reviews">Bewertungen</a></li>
                    <li><a href="#service">Service</a></li>
                </ul>
            </nav>
            <div class="header-actions">
                <button id="favorites-toggle" class="favorites-toggle">
                    <i class="fas fa-heart"></i>
                </button>
                <button id="cart-toggle" class="cart-toggle">
                    <i class="fas fa-shopping-cart"></i>
                    <span id="cart-count">0</span>
                </button>
            </div>
        </div>
    </header>

    <!-- Login-Bereich -->
    <div class="login-container">
        <button class="login-toggle" id="login-toggle">
            <i class="fas fa-user"></i>
        </button>
        <div class="login-form" id="login-form">
            <h3>Anmelden</h3>
            <input type="text" placeholder="Benutzername oder E-Mail">
            <input type="password" placeholder="Passwort">
            <button>Anmelden</button>
            <p>Noch kein Konto? <a href="#" id="show-register">Registrieren</a></p>
        </div>
        <div class="login-form" id="register-form">
            <h3>Registrieren</h3>
            <input type="text" placeholder="Vollständiger Name">
            <input type="email" placeholder="E-Mail">
            <input type="password" placeholder="Passwort">
            <input type="password" placeholder="Passwort bestätigen">
            <button>Registrieren</button>
            <p>Bereits ein Konto? <a href="#" id="show-login">Anmelden</a></p>
        </div>
        <div class="user-profile" id="user-profile">
            <img src="https://i.pravatar.cc/150?img=12" alt="Profilbild">
            <span>Anna Müller</span>
        </div>
    </div>

    <!-- Hauptinhalt -->
    <main>
        <!-- Produktbereich -->
        <section id="products">
            <h2 class="section-title">Unsere Sommerkollektion</h2>
            <div class="products-grid" id="products-grid">
                <!-- Produkte werden per JavaScript hinzugefügt -->
            </div>
        </section>

        <!-- Zahlungsmethoden -->
        <section id="payment">
            <h2 class="section-title">Zahlungsmethoden</h2>
            <div class="payment-methods">
                <div class="payment-method" data-method="credit-card">
                    <div class="payment-icon">
                        <i class="far fa-credit-card"></i>
                    </div>
                    <div class="payment-name">Kreditkarte</div>
                </div>
                <div class="payment-method" data-method="paypal">
                    <div class="payment-icon">
                        <i class="fab fa-paypal"></i>
                    </div>
                    <div class="payment-name">PayPal</div>
                </div>
                <div class="payment-method" data-method="klarna">
                    <div class="payment-icon">
                        <i class="fas fa-shopping-bag"></i>
                    </div>
                    <div class="payment-name">Klarna</div>
                </div>
                <div class="payment-method" data-method="sofort">
                    <div class="payment-icon">
                        <i class="fas fa-university"></i>
                    </div>
                    <div class="payment-name">Sofortüberweisung</div>
                </div>
                <div class="payment-method" data-method="apple-pay">
                    <div class="payment-icon">
                        <i class="fab fa-apple-pay"></i>
                    </div>
                    <div class="payment-name">Apple Pay</div>
                </div>
                <div class="payment-method" data-method="google-pay">
                    <div class="payment-icon">
                        <i class="fab fa-google-pay"></i>
                    </div>
                    <div class="payment-name">Google Pay</div>
                </div>
            </div>

            <!-- Zahlungsformular -->
            <div class="payment-form" id="credit-card-form">
                <h3>Kreditkartenzahlung</h3>
                <div class="form-group">
                    <label for="card-number">Kartennummer</label>
                    <input type="text" id="card-number" placeholder="1234 5678 9012 3456">
                </div>
                <div class="form-row">
                    <div class="form-group">
                        <label for="card-expiry">Ablaufdatum</label>
                        <input type="text" id="card-expiry" placeholder="MM/JJ">
                    </div>
                    <div class="form-group">
                        <label for="card-cvc">CVC</label>
                        <input type="text" id="card-cvc" placeholder="123">
                    </div>
                </div>
                <div class="form-group">
                    <label for="card-name">Name auf der Karte</label>
                    <input type="text" id="card-name" placeholder="Max Mustermann">
                </div>
                <button class="payment-submit">Zahlung bestätigen</button>
            </div>

            <div class="payment-form" id="paypal-form">
                <h3>PayPal-Zahlung</h3>
                <p>Sie werden zu PayPal weitergeleitet, um Ihre Zahlung abzuschließen.</p>
                <button class="payment-submit">Mit PayPal bezahlen</button>
            </div>

            <div class="payment-form" id="klarna-form">
                <h3>Klarna-Zahlung</h3>
                <p>Wählen Sie Ihre bevorzugte Zahlungsoption:</p>
                <div class="form-group">
                    <input type="radio" id="klarna-now" name="klarna-option" checked>
                    <label for="klarna-now">Sofort bezahlen</label>
                </div>
                <div class="form-group">
                    <input type="radio" id="klarna-later" name="klarna-option">
                    <label for="klarna-later">Später bezahlen (30 Tage)</label>
                </div>
                <div class="form-group">
                    <input type="radio" id="klarna-installments" name="klarna-option">
                    <label for="klarna-installments">In Raten bezahlen</label>
                </div>
                <button class="payment-submit">Weiter mit Klarna</button>
            </div>

            <div class="payment-form" id="sofort-form">
                <h3>Sofortüberweisung</h3>
                <p>Sie werden zu Ihrem Online-Banking weitergeleitet, um die Zahlung sofort zu bestätigen.</p>
                <button class="payment-submit">Jetzt bezahlen</button>
            </div>

            <div class="payment-form" id="apple-pay-form">
                <h3>Apple Pay</h3>
                <p>Verwenden Sie Apple Pay für eine schnelle und sichere Zahlung.</p>
                <button class="payment-submit">Mit Apple Pay bezahlen</button>
            </div>

            <div class="payment-form" id="google-pay-form">
                <h3>Google Pay</h3>
                <p>Verwenden Sie Google Pay für eine schnelle und sichere Zahlung.</p>
                <button class="payment-submit">Mit Google Pay bezahlen</button>
            </div>
        </section>

        <!-- Bewertungssystem -->
        <section id="reviews">
            <h2 class="section-title">Kundenbewertungen</h2>
            <div class="reviews-section">
                <div class="review-form">
                    <h3>Schreiben Sie eine Bewertung</h3>
                    <div class="rating-stars" id="rating-stars">
                        <span class="star" data-rating="1"><i class="fas fa-star"></i></span>
                        <span class="star" data-rating="2"><i class="fas fa-star"></i></span>
                        <span class="star" data-rating="3"><i class="fas fa-star"></i></span>
                        <span class="star" data-rating="4"><i class="fas fa-star"></i></span>
                        <span class="star" data-rating="5"><i class="fas fa-star"></i></span>
                    </div>
                    <textarea placeholder="Teilen Sie Ihre Erfahrungen mit diesem Produkt..."></textarea>
                    <button id="submit-review">Bewertung absenden</button>
                </div>
                <div class="reviews-list" id="reviews-list">
                    <!-- Bewertungen werden per JavaScript hinzugefügt -->
                </div>
            </div>
        </section>

        <!-- Serviceanfrage -->
        <section id="service">
            <h2 class="section-title">Serviceanfrage</h2>
            <div class="service-request">
                <form class="service-form">
                    <div class="form-group">
                        <label for="name">Name</label>
                        <input type="text" id="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">E-Mail</label>
                        <input type="email" id="email" required>
                    </div>
                    <div class="form-group">
                        <label for="phone">Telefon</label>
                        <input type="tel" id="phone">
                    </div>
                    <div class="form-group">
                        <label for="subject">Betreff</label>
                        <select id="subject">
                            <option value="">Bitte wählen</option>
                            <option value="return">Rückgabe</option>
                            <option value="exchange">Umtausch</option>
                            <option value="complaint">Reklamation</option>
                            <option value="other">Sonstiges</option>
                        </select>
                    </div>
                    <div class="form-group full-width">
                        <label for="message">Nachricht</label>
                        <textarea id="message" required></textarea>
                    </div>
                    <button type="submit" class="submit-btn">Anfrage senden</button>
                </form>
            </div>
        </section>
    </main>

    <!-- Warenkorb -->
    <div class="cart-container" id="cart-container">
        <div class="cart-header">
            <h2>Ihr Warenkorb</h2>
            <button class="close-cart" id="close-cart">
                <i class="fas fa-times"></i>
            </button>
        </div>
        <div class="cart-items" id="cart-items">
            <!-- Warenkorb-Items werden per JavaScript hinzugefügt -->
        </div>
        <div class="cart-total">
            <span>Gesamt:</span>
            <span id="cart-total-price">€0.00</span>
        </div>
        <button class="checkout-btn">Zur Kasse</button>
    </div>

    <!-- Favoriten -->
    <div class="favorites-container" id="favorites-container">
        <div class="cart-header">
            <h2>Ihre Favoriten</h2>
            <button class="close-cart" id="close-favorites">
                <i class="fas fa-times"></i>
            </button>
        </div>
        <div class="cart-items" id="favorites-items">
            <!-- Favoriten-Items werden per JavaScript hinzugefügt -->
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h3>Elegant Lady</h3>
                <p>Ihr Online-Shop für elegante Damen-Sommerbekleidung. Wir bieten hochwertige Mode zu fairen Preisen.</p>
                <div class="social-icons">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-pinterest-p"></i></a>
                </div>
            </div>
            <div class="footer-section">
                <h3>Kontakt</h3>
                <p><i class="fas fa-map-marker-alt"></i> Musterstraße 123, 10115 Berlin</p>
                <p><i class="fas fa-phone"></i> +49 30 12345678</p>
                <p><i class="fas fa-envelope"></i> info@elegant-lady.de</p>
            </div>
            <div class="footer-section">
                <h3>Informationen</h3>
                <a href="#">Über uns</a>
                <a href="#">Versand & Rückgabe</a>
                <a href="#">AGB</a>
                <a href="#">Datenschutz</a>
                <a href="#">Impressum</a>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2023 Elegant Lady. Alle Rechte vorbehalten.</p>
        </div>
    </footer>

    <script>
        // Produktdaten
        const products = [
            {
                id: 1,
                name: "Sommerkleid mit Blumenmuster",
                price: 49.99,
                image: "https://images.unsplash.com/photo-1595777457583-95e059d581b8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=500&q=80",
                colors: ["#e75480", "#f8c8dc", "#ffb6c1", "#98d8e8"],
                sizes: ["XS", "S", "M", "L", "XL"]
            },
            {
                id: 2,
                name: "Leinenhose in Beige",
                price: 39.99,
                image: "https://images.unsplash.com/photo-1582418702059-97ebafb35d09?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=500&q=80",
                colors: ["#d2b48c", "#f5f5dc", "#a0522d", "#8b4513"],
                sizes: ["S", "M", "L", "XL"]
            },
            {
                id: 3,
                name: "Bluse mit Spitzenbesatz",
                price: 34.99,
                image: "https://images.unsplash.com/photo-1581044777550-4cfa60707c03?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=500&q=80",
                colors: ["#ffffff", "#f0f8ff", "#fff0f5", "#f5f5f5"],
                sizes: ["XS", "S", "M", "L"]
            },
            {
                id: 4,
                name: "Strand-Sarong mit Tropenmuster",
                price: 24.99,
                image: "https://images.unsplash.com/photo-1518623489648-a173ef7824f3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=500&q=80",
                colors: ["#ff6347", "#32cd32", "#1e90ff", "#ffd700"],
                sizes: ["One Size"]
            },
            {
                id: 5,
                name: "Sommer-Sandalen mit Keilabsatz",
                price: 59.99,
                image: "https://images.unsplash.com/photo-1543163521-1bf539c55dd2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=500&q=80",
                colors: ["#8b4513", "#000000", "#ffffff", "#daa520"],
                sizes: ["36", "37", "38", "39", "40"]
            },
            {
                id: 6,
                name: "Strandtasche aus Stroh",
                price: 29.99,
                image: "https://images.unsplash.com/photo-1553062407-98eeb64c6a62?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=500&q=80",
                colors: ["#daa520", "#f5deb3", "#8b4513", "#d2691e"],
                sizes: ["One Size"]
            }
        ];

        // Bewertungsdaten
        const reviews = [
            {
                id: 1,
                author: "Maria Schmidt",
                rating: 5,
                date: "15.06.2023",
                text: "Das Sommerkleid ist wunderschön! Die Qualität ist hervorragend und die Passform perfekt. Werde definitiv wieder bestellen."
            },
            {
                id: 2,
                author: "Julia Weber",
                rating: 4,
                date: "10.06.2023",
                text: "Die Leinenhose sitzt gut und ist sehr bequem. Einziger Nachteil: Sie knittern etwas schnell. Ansonsten top!"
            },
            {
                id: 3,
                author: "Sabine Hoffmann",
                rating: 5,
                date: "05.06.2023",
                text: "Die Bluse ist einfach traumhaft. Der Spitzenbesatz verleiht ihr einen eleganten Touch. Perfekt für den Sommer!"
            }
        ];

        // Warenkorb und Favoriten
        let cart = [];
        let favorites = [];

        // DOM-Elemente
        const productsGrid = document.getElementById('products-grid');
        const cartContainer = document.getElementById('cart-container');
        const favoritesContainer = document.getElementById('favorites-container');
        const cartItems = document.getElementById('cart-items');
        const favoritesItems = document.getElementById('favorites-items');
        const cartCount = document.getElementById('cart-count');
        const cartTotalPrice = document.getElementById('cart-total-price');
        const cartToggle = document.getElementById('cart-toggle');
        const closeCart = document.getElementById('close-cart');
        const favoritesToggle = document.getElementById('favorites-toggle');
        const closeFavorites = document.getElementById('close-favorites');
        const overlay = document.getElementById('overlay');
        const loginToggle = document.getElementById('login-toggle');
        const loginForm = document.getElementById('login-form');
        const registerForm = document.getElementById('register-form');
        const showRegister = document.getElementById('show-register');
        const showLogin = document.getElementById('show-login');
        const userProfile = document.getElementById('user-profile');
        const reviewsList = document.getElementById('reviews-list');
        const ratingStars = document.getElementById('rating-stars');
        const submitReview = document.getElementById('submit-review');
        const paymentMethods = document.querySelectorAll('.payment-method');
        const paymentForms = document.querySelectorAll('.payment-form');

        // Produkte anzeigen
        function displayProducts() {
            productsGrid.innerHTML = '';
            products.forEach(product => {
                const productCard = document.createElement('div');
                productCard.className = 'product-card';
                productCard.innerHTML = `
                    <div class="product-image" style="background-image: url('${product.image}')">
                        <div class="product-actions">
                            <button class="favorite-btn" data-id="${product.id}">
                                <i class="far fa-heart"></i>
                            </button>
                            <button class="quick-view-btn" data-id="${product.id}">
                                <i class="far fa-eye"></i>
                            </button>
                        </div>
                    </div>
                    <div class="product-info">
                        <h3 class="product-title">${product.name}</h3>
                        <div class="product-price">€${product.price.toFixed(2)}</div>
                        <div class="color-selector">
                            ${product.colors.map(color => `
                                <div class="color-option ${color === product.colors[0] ? 'active' : ''}" 
                                     style="background-color: ${color}" 
                                     data-color="${color}"></div>
                            `).join('')}
                        </div>
                        <div class="size-selector">
                            ${product.sizes.map(size => `
                                <div class="size-option ${size === product.sizes[0] ? 'active' : ''}" 
                                     data-size="${size}">${size}</div>
                            `).join('')}
                        </div>
                        <button class="add-to-cart" data-id="${product.id}">In den Warenkorb</button>
                    </div>
                `;
                productsGrid.appendChild(productCard);
            });

            // Event-Listener für Produktaktionen
            document.querySelectorAll('.add-to-cart').forEach(button => {
                button.addEventListener('click', addToCart);
            });

            document.querySelectorAll('.favorite-btn').forEach(button => {
                button.addEventListener('click', toggleFavorite);
            });

            document.querySelectorAll('.color-option').forEach(option => {
                option.addEventListener('click', selectColor);
            });

            document.querySelectorAll('.size-option').forEach(option => {
                option.addEventListener('click', selectSize);
            });
        }

        // Farbe auswählen
        function selectColor(e) {
            const colorOptions = e.target.parentElement.querySelectorAll('.color-option');
            colorOptions.forEach(option => option.classList.remove('active'));
            e.target.classList.add('active');
        }

        // Größe auswählen
        function selectSize(e) {
            const sizeOptions = e.target.parentElement.querySelectorAll('.size-option');
            sizeOptions.forEach(option => option.classList.remove('active'));
            e.target.classList.add('active');
        }

        // Zum Warenkorb hinzufügen
        function addToCart(e) {
            const productId = parseInt(e.target.getAttribute('data-id'));
            const product = products.find(p => p.id === productId);
            
            // Ausgewählte Farbe und Größe ermitteln
            const productCard = e.target.closest('.product-card');
            const selectedColor = productCard.querySelector('.color-option.active').style.backgroundColor;
            const selectedSize = productCard.querySelector('.size-option.active').textContent;
            
            // Prüfen, ob Produkt bereits im Warenkorb ist
            const existingItem = cart.find(item => 
                item.id === productId && 
                item.color === selectedColor && 
                item.size === selectedSize
            );
            
            if (existingItem) {
                existingItem.quantity += 1;
            } else {
                cart.push({
                    id: productId,
                    name: product.name,
                    price: product.price,
                    image: product.image,
                    color: selectedColor,
                    size: selectedSize,
                    quantity: 1
                });
            }
            
            updateCart();
            showNotification(`${product.name} wurde zum Warenkorb hinzugefügt`);
        }

        // Favoriten hinzufügen/entfernen
        function toggleFavorite(e) {
            const productId = parseInt(e.target.closest('.favorite-btn').getAttribute('data-id'));
            const product = products.find(p => p.id === productId);
            const favoriteBtn = e.target.closest('.favorite-btn');
            
            const existingIndex = favorites.findIndex(item => item.id === productId);
            
            if (existingIndex !== -1) {
                favorites.splice(existingIndex, 1);
                favoriteBtn.innerHTML = '<i class="far fa-heart"></i>';
                showNotification(`${product.name} wurde von den Favoriten entfernt`);
            } else {
                // Ausgewählte Farbe und Größe ermitteln
                const productCard = e.target.closest('.product-card');
                const selectedColor = productCard.querySelector('.color-option.active').style.backgroundColor;
                const selectedSize = productCard.querySelector('.size-option.active').textContent;
                
                favorites.push({
                    id: productId,
                    name: product.name,
                    price: product.price,
                    image: product.image,
                    color: selectedColor,
                    size: selectedSize
                });
                favoriteBtn.innerHTML = '<i class="fas fa-heart"></i>';
                showNotification(`${product.name} wurde zu den Favoriten hinzugefügt`);
            }
            
            updateFavorites();
        }

        // Warenkorb aktualisieren
        function updateCart() {
            cartItems.innerHTML = '';
            let total = 0;
            let count = 0;
            
            cart.forEach(item => {
                const cartItem = document.createElement('div');
                cartItem.className = 'cart-item';
                cartItem.innerHTML = `
                    <div class="cart-item-image" style="background-image: url('${item.image}')"></div>
                    <div class="cart-item-details">
                        <div class="cart-item-title">${item.name}</div>
                        <div class="cart-item-color">Farbe: <span style="display: inline-block; width: 15px; height: 15px; background-color: ${item.color}; border-radius: 50%; vertical-align: middle;"></span></div>
                        <div class="cart-item-size">Größe: ${item.size}</div>
                        <div class="cart-item-price">€${(item.price * item.quantity).toFixed(2)}</div>
                        <div class="cart-item-actions">
                            <button class="quantity-btn minus" data-id="${item.id}" data-color="${item.color}" data-size="${item.size}">-</button>
                            <span class="quantity">${item.quantity}</span>
                            <button class="quantity-btn plus" data-id="${item.id}" data-color="${item.color}" data-size="${item.size}">+</button>
                            <button class="remove-item" data-id="${item.id}" data-color="${item.color}" data-size="${item.size}">
                                <i class="fas fa-trash"></i>
                            </button>
                        </div>
                    </div>
                `;
                cartItems.appendChild(cartItem);
                
                total += item.price * item.quantity;
                count += item.quantity;
            });
            
            cartTotalPrice.textContent = `€${total.toFixed(2)}`;
            cartCount.textContent = count;
            
            // Event-Listener für Warenkorb-Aktionen
            document.querySelectorAll('.quantity-btn.minus').forEach(button => {
                button.addEventListener('click', decreaseQuantity);
            });
            
            document.querySelectorAll('.quantity-btn.plus').forEach(button => {
                button.addEventListener('click', increaseQuantity);
            });
            
            document.querySelectorAll('.remove-item').forEach(button => {
                button.addEventListener('click', removeFromCart);
            });
        }

        // Menge erhöhen
        function increaseQuantity(e) {
            const productId = parseInt(e.target.getAttribute('data-id'));
            const color = e.target.getAttribute('data-color');
            const size = e.target.getAttribute('data-size');
            
            const item = cart.find(item => 
                item.id === productId && 
                item.color === color && 
                item.size === size
            );
            
            if (item) {
                item.quantity += 1;
                updateCart();
            }
        }

        // Menge verringern
        function decreaseQuantity(e) {
            const productId = parseInt(e.target.getAttribute('data-id'));
            const color = e.target.getAttribute('data-color');
            const size = e.target.getAttribute('data-size');
            
            const item = cart.find(item => 
                item.id === productId && 
                item.color === color && 
                item.size === size
            );
            
            if (item) {
                if (item.quantity > 1) {
                    item.quantity -= 1;
                } else {
                    // Wenn Menge 1 ist, Artikel entfernen
                    const index = cart.findIndex(i => 
                        i.id === productId && 
                        i.color === color && 
                        i.size === size
                    );
                    if (index !== -1) {
                        cart.splice(index, 1);
                    }
                }
                updateCart();
            }
        }

        // Aus Warenkorb entfernen
        function removeFromCart(e) {
            const productId = parseInt(e.target.closest('.remove-item').getAttribute('data-id'));
            const color = e.target.closest('.remove-item').getAttribute('data-color');
            const size = e.target.closest('.remove-item').getAttribute('data-size');
            
            const index = cart.findIndex(item => 
                item.id === productId && 
                item.color === color && 
                item.size === size
            );
            
            if (index !== -1) {
                const product = products.find(p => p.id === productId);
                cart.splice(index, 1);
                updateCart();
                showNotification(`${product.name} wurde aus dem Warenkorb entfernt`);
            }
        }

        // Favoriten aktualisieren
        function updateFavorites() {
            favoritesItems.innerHTML = '';
            
            if (favorites.length === 0) {
                favoritesItems.innerHTML = '<p>Ihre Favoritenliste ist leer.</p>';
                return;
            }
            
            favorites.forEach(item => {
                const favoriteItem = document.createElement('div');
                favoriteItem.className = 'cart-item';
                favoriteItem.innerHTML = `
                    <div class="cart-item-image" style="background-image: url('${item.image}')"></div>
                    <div class="cart-item-details">
                        <div class="cart-item-title">${item.name}</div>
                        <div class="cart-item-color">Farbe: <span style="display: inline-block; width: 15px; height: 15px; background-color: ${item.color}; border-radius: 50%; vertical-align: middle;"></span></div>
                        <div class="cart-item-size">Größe: ${item.size}</div>
                        <div class="cart-item-price">€${item.price.toFixed(2)}</div>
                        <div class="cart-item-actions">
                            <button class="add-to-cart-from-favorites" data-id="${item.id}" data-color="${item.color}" data-size="${item.size}">In den Warenkorb</button>
                            <button class="remove-from-favorites" data-id="${item.id}" data-color="${item.color}" data-size="${item.size}">
                                <i class="fas fa-trash"></i>
                            </button>
                        </div>
                    </div>
                `;
                favoritesItems.appendChild(favoriteItem);
            });
            
            // Event-Listener für Favoriten-Aktionen
            document.querySelectorAll('.add-to-cart-from-favorites').forEach(button => {
                button.addEventListener('click', addToCartFromFavorites);
            });
            
            document.querySelectorAll('.remove-from-favorites').forEach(button => {
                button.addEventListener('click', removeFromFavorites);
            });
        }

        // Von Favoriten zum Warenkorb hinzufügen
        function addToCartFromFavorites(e) {
            const productId = parseInt(e.target.getAttribute('data-id'));
            const color = e.target.getAttribute('data-color');
            const size = e.target.getAttribute('data-size');
            const product = products.find(p => p.id === productId);
            
            // Prüfen, ob Produkt bereits im Warenkorb ist
            const existingItem = cart.find(item => 
                item.id === productId && 
                item.color === color && 
                item.size === size
            );
            
            if (existingItem) {
                existingItem.quantity += 1;
            } else {
                cart.push({
                    id: productId,
                    name: product.name,
                    price: product.price,
                    image: product.image,
                    color: color,
                    size: size,
                    quantity: 1
                });
            }
            
            updateCart();
            showNotification(`${product.name} wurde zum Warenkorb hinzugefügt`);
        }

        // Aus Favoriten entfernen
        function removeFromFavorites(e) {
            const productId = parseInt(e.target.closest('.remove-from-favorites').getAttribute('data-id'));
            const color = e.target.closest('.remove-from-favorites').getAttribute('data-color');
            const size = e.target.closest('.remove-from-favorites').getAttribute('data-size');
            
            const index = favorites.findIndex(item => 
                item.id === productId && 
                item.color === color && 
                item.size === size
            );
            
            if (index !== -1) {
                const product = products.find(p => p.id === productId);
                favorites.splice(index, 1);
                updateFavorites();
                
                // Auch das Herz-Symbol in der Produktliste aktualisieren
                const favoriteBtn = document.querySelector(`.favorite-btn[data-id="${productId}"]`);
                if (favoriteBtn) {
                    favoriteBtn.innerHTML = '<i class="far fa-heart"></i>';
                }
                
                showNotification(`${product.name} wurde von den Favoriten entfernt`);
            }
        }

        // Zahlungsmethode auswählen
        function selectPaymentMethod(e) {
            const method = e.currentTarget.getAttribute('data-method');
            
            // Alle Zahlungsmethoden deaktivieren
            paymentMethods.forEach(pm => pm.classList.remove('active'));
            paymentForms.forEach(form => form.classList.remove('active'));
            
            // Ausgewählte Zahlungsmethode aktivieren
            e.currentTarget.classList.add('active');
            document.getElementById(`${method}-form`).classList.add('active');
        }

        // Bewertungen anzeigen
        function displayReviews() {
            reviewsList.innerHTML = '';
            
            reviews.forEach(review => {
                const reviewItem = document.createElement('div');
                reviewItem.className = 'review-item';
                reviewItem.innerHTML = `
                    <div class="review-header">
                        <div class="review-author">${review.author}</div>
                        <div class="review-rating">
                            ${'★'.repeat(review.rating)}${'☆'.repeat(5 - review.rating)}
                        </div>
                    </div>
                    <div class="review-date">${review.date}</div>
                    <div class="review-text">${review.text}</div>
                `;
                reviewsList.appendChild(reviewItem);
            });
        }

        // Benachrichtigung anzeigen
        function showNotification(message) {
            const notification = document.createElement('div');
            notification.style.cssText = `
                position: fixed;
                top: 20px;
                right: 20px;
                background: var(--primary-color);
                color: white;
                padding: 1rem 1.5rem;
                border-radius: 5px;
                box-shadow: var(--shadow);
                z-index: 10000;
                transform: translateX(150%);
                transition: transform 0.3s ease;
            `;
            notification.textContent = message;
            document.body.appendChild(notification);
            
            setTimeout(() => {
                notification.style.transform = 'translateX(0)';
            }, 100);
            
            setTimeout(() => {
                notification.style.transform = 'translateX(150%)';
                setTimeout(() => {
                    document.body.removeChild(notification);
                }, 300);
            }, 3000);
        }

        // 3D Hintergrund mit Canvas
        function initBackground() {
            const canvas = document.getElementById('bg-canvas');
            const ctx = canvas.getContext('2d');
            
            function resizeCanvas() {
                canvas.width = window.innerWidth;
                canvas.height = window.innerHeight;
            }
            
            resizeCanvas();
            window.addEventListener('resize', resizeCanvas);
            
            const particles = [];
            const particleCount = 50;
            
            // Partikel erstellen
            for (let i = 0; i < particleCount; i++) {
                particles.push({
                    x: Math.random() * canvas.width,
                    y: Math.random() * canvas.height,
                    radius: Math.random() * 3 + 1,
                    color: `rgba(${Math.floor(Math.random() * 50 + 200)}, ${Math.floor(Math.random() * 100 + 150)}, ${Math.floor(Math.random() * 100 + 150)}, ${Math.random() * 0.5 + 0.2})`,
                    speed: Math.random() * 0.5 + 0.1,
                    angle: Math.random() * Math.PI * 2
                });
            }
            
            // Animation
            function animate() {
                ctx.clearRect(0, 0, canvas.width, canvas.height);
                
                particles.forEach(particle => {
                    // Partikel bewegen
                    particle.x += Math.cos(particle.angle) * particle.speed;
                    particle.y += Math.sin(particle.angle) * particle.speed;
                    
                    // Wenn Partikel den Rand erreicht, zurücksetzen
                    if (particle.x < 0 || particle.x > canvas.width || particle.y < 0 || particle.y > canvas.height) {
                        particle.x = Math.random() * canvas.width;
                        particle.y = Math.random() * canvas.height;
                    }
                    
                    // Partikel zeichnen
                    ctx.beginPath();
                    ctx.arc(particle.x, particle.y, particle.radius, 0, Math.PI * 2);
                    ctx.fillStyle = particle.color;
                    ctx.fill();
                    
                    // Verbindungen zwischen nahen Partikeln zeichnen
                    particles.forEach(otherParticle => {
                        const dx = particle.x - otherParticle.x;
                        const dy = particle.y - otherParticle.y;
                        const distance = Math.sqrt(dx * dx + dy * dy);
                        
                        if (distance < 100) {
                            ctx.beginPath();
                            ctx.moveTo(particle.x, particle.y);
                            ctx.lineTo(otherParticle.x, otherParticle.y);
                            ctx.strokeStyle = `rgba(231, 84, 128, ${0.1 * (1 - distance / 100)})`;
                            ctx.lineWidth = 0.5;
                            ctx.stroke();
                        }
                    });
                });
                
                requestAnimationFrame(animate);
            }
            
            animate();
        }

        // Event-Listener für UI-Elemente
        cartToggle.addEventListener('click', () => {
            cartContainer.classList.add('active');
            overlay.classList.add('active');
        });

        closeCart.addEventListener('click', () => {
            cartContainer.classList.remove('active');
            overlay.classList.remove('active');
        });

        favoritesToggle.addEventListener('click', () => {
            favoritesContainer.classList.add('active');
            overlay.classList.add('active');
        });

        closeFavorites.addEventListener('click', () => {
            favoritesContainer.classList.remove('active');
            overlay.classList.remove('active');
        });

        overlay.addEventListener('click', () => {
            cartContainer.classList.remove('active');
            favoritesContainer.classList.remove('active');
            overlay.classList.remove('active');
        });

        loginToggle.addEventListener('click', () => {
            loginForm.classList.toggle('active');
            registerForm.classList.remove('active');
        });

        showRegister.addEventListener('click', (e) => {
            e.preventDefault();
            loginForm.classList.remove('active');
            registerForm.classList.add('active');
        });

        showLogin.addEventListener('click', (e) => {
            e.preventDefault();
            registerForm.classList.remove('active');
            loginForm.classList.add('active');
        });

        // Zahlungsmethoden Event-Listener
        paymentMethods.forEach(method => {
            method.addEventListener('click', selectPaymentMethod);
        });

        // Bewertungssterne
        ratingStars.addEventListener('click', (e) => {
            if (e.target.classList.contains('star') || e.target.parentElement.classList.contains('star')) {
                const star = e.target.classList.contains('star') ? e.target : e.target.parentElement;
                const rating = parseInt(star.getAttribute('data-rating'));
                
                const stars = ratingStars.querySelectorAll('.star');
                stars.forEach((s, index) => {
                    if (index < rating) {
                        s.classList.add('active');
                    } else {
                        s.classList.remove('active');
                    }
                });
            }
        });

        // Bewertung absenden
        submitReview.addEventListener('click', () => {
            const activeStars = ratingStars.querySelectorAll('.star.active');
            const reviewText = document.querySelector('.review-form textarea').value;
            
            if (activeStars.length === 0) {
                alert('Bitte geben Sie eine Bewertung ab, indem Sie auf die Sterne klicken.');
                return;
            }
            
            if (!reviewText.trim()) {
                alert('Bitte geben Sie einen Bewertungstext ein.');
                return;
            }
            
            const newReview = {
                id: reviews.length + 1,
                author: "Sie",
                rating: activeStars.length,
                date: new Date().toLocaleDateString('de-DE'),
                text: reviewText
            };
            
            reviews.unshift(newReview);
            displayReviews();
            
            // Formular zurücksetzen
            ratingStars.querySelectorAll('.star').forEach(star => {
                star.classList.remove('active');
            });
            document.querySelector('.review-form textarea').value = '';
            
            showNotification('Vielen Dank für Ihre Bewertung!');
        });

        // Service-Formular
        document.querySelector('.service-form').addEventListener('submit', (e) => {
            e.preventDefault();
            showNotification('Ihre Serviceanfrage wurde erfolgreich gesendet!');
            document.querySelector('.service-form').reset();
        });

        // Zahlungsformulare
        document.querySelectorAll('.payment-submit').forEach(button => {
            button.addEventListener('click', (e) => {
                e.preventDefault();
                showNotification('Zahlung wurde erfolgreich verarbeitet!');
            });
        });

        // Initialisierung
        displayProducts();
        displayReviews();
        initBackground();

        // Standard-Zahlungsmethode auswählen
        document.querySelector('.payment-method[data-method="credit-card"]').click();

        // Simuliertes Login (für Demo-Zwecke)
        document.querySelector('#login-form button').addEventListener('click', (e) => {
            e.preventDefault();
            loginForm.classList.remove('active');
            userProfile.style.display = 'flex';
            showNotification('Erfolgreich angemeldet!');
        });

        document.querySelector('#register-form button').addEventListener('click', (e) => {
            e.preventDefault();
            registerForm.classList.remove('active');
            userProfile.style.display = 'flex';
            showNotification('Registrierung erfolgreich! Sie sind jetzt angemeldet.');
        });
    </script>
</body>
</html>

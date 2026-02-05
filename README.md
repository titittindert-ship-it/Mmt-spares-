# Mmt-spares-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MMT - Premium 2Wheeler Spares</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Rajdhani:wght@300;500;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-red: #c41e3a;
            --primary-blue: #1e3a8a;
            --white: #ffffff;
            --light-gray: #f8fafc;
            --dark-blue: #0f172a;
            --accent-blue: #3b82f6;
        }

        body {
            font-family: 'Rajdhani', sans-serif;
            background: var(--white);
            color: var(--dark-blue);
            overflow-x: hidden;
        }

        /* Animated Background */
        .bg-pattern {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                radial-gradient(circle at 20% 50%, rgba(30, 58, 138, 0.05) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(196, 30, 58, 0.05) 0%, transparent 50%);
            z-index: -1;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 15px 30px;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            border-bottom: 3px solid var(--primary-blue);
            box-shadow: 0 2px 20px rgba(30, 58, 138, 0.1);
        }

        .nav-container {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo-img {
            height: 70px;
            width: auto;
            filter: drop-shadow(0 2px 4px rgba(0,0,0,0.2));
        }

        .nav-links {
            display: flex;
            gap: 40px;
            list-style: none;
        }

        .nav-links a {
            color: var(--primary-blue);
            text-decoration: none;
            font-weight: 700;
            font-size: 1.1rem;
            position: relative;
            transition: color 0.3s;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 3px;
            background: var(--primary-red);
            transition: width 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary-red);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            margin-top: 100px;
            background: linear-gradient(135deg, var(--white) 0%, var(--light-gray) 100%);
        }

        .hero-content {
            text-align: center;
            z-index: 2;
            max-width: 900px;
            padding: 40px 20px;
        }

        .hero-logo {
            width: 300px;
            height: auto;
            margin-bottom: 30px;
            filter: drop-shadow(0 10px 30px rgba(30, 58, 138, 0.3));
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .hero h1 {
            font-family: 'Orbitron', sans-serif;
            font-size: 3.5rem;
            font-weight: 900;
            margin-bottom: 20px;
            color: var(--primary-blue);
            text-transform: uppercase;
            letter-spacing: 3px;
        }

        .hero h1 span {
            color: var(--primary-red);
        }

        .hero p {
            font-size: 1.5rem;
            margin-bottom: 40px;
            color: var(--dark-blue);
            font-weight: 500;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 18px 50px;
            font-family: 'Orbitron', sans-serif;
            font-size: 1rem;
            font-weight: 700;
            border: none;
            cursor: pointer;
            position: relative;
            overflow: hidden;
            transition: all 0.3s;
            text-transform: uppercase;
            letter-spacing: 2px;
            border-radius: 5px;
        }

        .btn-primary {
            background: var(--primary-red);
            color: var(--white);
            box-shadow: 0 4px 15px rgba(196, 30, 58, 0.4);
        }

        .btn-secondary {
            background: var(--primary-blue);
            color: var(--white);
            box-shadow: 0 4px 15px rgba(30, 58, 138, 0.4);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
        }

        .btn-primary:hover {
            background: #a01830;
        }

        .btn-secondary:hover {
            background: #152c5b;
        }

        /* Decorative Elements */
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary-blue), var(--primary-red), var(--primary-blue));
        }

        /* Features Section */
        .features {
            padding: 100px 30px;
            background: var(--white);
            position: relative;
        }

        .section-title {
            font-family: 'Orbitron', sans-serif;
            font-size: 2.8rem;
            text-align: center;
            margin-bottom: 60px;
            color: var(--primary-blue);
            text-transform: uppercase;
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--primary-red);
        }

        .features-grid {
            max-width: 1400px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 40px;
        }

        .feature-card {
            background: var(--white);
            border: 2px solid var(--primary-blue);
            padding: 40px 30px;
            position: relative;
            overflow: hidden;
            transition: all 0.3s;
            text-align: center;
            border-radius: 10px;
        }

        .feature-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: var(--primary-red);
            transform: scaleX(0);
            transition: transform 0.3s;
        }

        .feature-card:hover::before {
            transform: scaleX(1);
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(30, 58, 138, 0.15);
            border-color: var(--primary-red);
        }

        .feature-icon {
            width: 80px;
            height: 80px;
            margin: 0 auto 25px;
            background: linear-gradient(135deg, var(--primary-blue), var(--accent-blue));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            color: var(--white);
            border: 3px solid var(--primary-red);
        }

        .feature-card h3 {
            font-family: 'Orbitron', sans-serif;
            font-size: 1.4rem;
            margin-bottom: 15px;
            color: var(--primary-blue);
            text-transform: uppercase;
        }

        .feature-card p {
            color: #64748b;
            line-height: 1.6;
            font-size: 1.05rem;
        }

        /* Products Section */
        .products {
            padding: 100px 30px;
            background: linear-gradient(180deg, var(--light-gray) 0%, var(--white) 100%);
        }

        .products-grid {
            max-width: 1400px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 30px;
        }

        .product-card {
            background: var(--white);
            border: 2px solid #e2e8f0;
            padding: 30px;
            text-align: center;
            position: relative;
            overflow: hidden;
            transition: all 0.3s;
            border-radius: 10px;
        }

        .product-card:hover {
            transform: translateY(-5px);
            border-color: var(--primary-blue);
            box-shadow: 0 15px 30px rgba(30, 58, 138, 0.1);
        }

        .product-img {
            width: 100%;
            height: 180px;
            background: linear-gradient(135deg, var(--primary-blue), var(--accent-blue));
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            border-radius: 8px;
            color: var(--white);
            border-bottom: 4px solid var(--primary-red);
        }

        .product-card h4 {
            font-family: 'Orbitron', sans-serif;
            color: var(--primary-blue);
            margin-bottom: 12px;
            font-size: 1.3rem;
            text-transform: uppercase;
        }

        .product-card p {
            color: #64748b;
            font-size: 1rem;
            line-height: 1.5;
        }

        .product-tag {
            display: inline-block;
            background: var(--primary-red);
            color: var(--white);
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 700;
            margin-top: 15px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Contact Section */
        .contact {
            padding: 100px 30px;
            background: var(--primary-blue);
            position: relative;
            color: var(--white);
        }

        .contact::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: var(--primary-red);
        }

        .contact-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .contact-info h2 {
            font-family: 'Orbitron', sans-serif;
            font-size: 2.5rem;
            color: var(--white);
            margin-bottom: 20px;
            text-transform: uppercase;
        }

        .contact-info h2 span {
            color: var(--primary-red);
        }

        .contact-info > p {
            font-size: 1.2rem;
            line-height: 1.8;
            color: rgba(255, 255, 255, 0.9);
            margin-bottom: 40px;
        }

        .contact-details {
            margin-top: 30px;
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            gap: 20px;
            margin-bottom: 30px;
            font-size: 1.1rem;
        }

        .contact-item .icon {
            width: 50px;
            height: 50px;
            background: var(--primary-red);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            flex-shrink: 0;
            color: var(--white);
        }

        .contact-item div strong {
            display: block;
            color: var(--white);
            font-size: 1.2rem;
            margin-bottom: 5px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .contact-item div {
            color: rgba(255, 255, 255, 0.9);
        }

        .contact-form {
            background: var(--white);
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.3);
        }

        .form-group {
            margin-bottom: 25px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: var(--primary-blue);
            font-weight: 700;
            text-transform: uppercase;
            font-size: 0.9rem;

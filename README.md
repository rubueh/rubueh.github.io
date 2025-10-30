# rubueh.github.io

[sanibrau-pitch-site(1).html](https://github.com/user-attachments/files/23223283/sanibrau-pitch-site.1.html)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SaniBrau - Modular CIP Innovation for Craft Breweries</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-navy: #0f2537;
            --accent-teal: #00a896;
            --accent-orange: #ff6b35;
            --light-gray: #f8f9fa;
            --dark-gray: #2c3e50;
            --text-gray: #5a6c7d;
            --success-green: #27ae60;
            --water-blue: #3498db;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            line-height: 1.6;
            color: var(--dark-gray);
            overflow-x: hidden;
        }

        /* Header */
        header {
            background: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
            background: rgba(255, 255, 255, 0.98);
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary-navy);
        }

        .logo-icon {
            width: 40px;
            height: 40px;
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
            list-style: none;
            align-items: center;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark-gray);
            font-weight: 500;
            transition: all 0.3s;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -3px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent-teal);
            transition: width 0.3s;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-cta {
            background: var(--accent-teal);
            color: white !important;
            padding: 0.6rem 1.5rem;
            border-radius: 25px;
            transition: all 0.3s;
        }

        .nav-cta:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(0, 168, 150, 0.3);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary-navy) 0%, #1a3d4d 100%);
            color: white;
            padding: 5rem 2rem;
            position: relative;
            min-height: 600px;
            display: flex;
            align-items: center;
        }

        .hero-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .hero-left h1 {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }

        .hero-left .highlight {
            color: var(--accent-teal);
        }

        .hero-left p {
            font-size: 1.25rem;
            margin-bottom: 2rem;
            opacity: 0.95;
            line-height: 1.8;
        }

        .hero-ctas {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .btn-primary {
            background: var(--accent-orange);
            color: white;
            padding: 1rem 2rem;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            display: inline-block;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(255, 107, 53, 0.4);
        }

        .btn-secondary {
            background: transparent;
            color: white;
            padding: 1rem 2rem;
            border: 2px solid white;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            display: inline-block;
        }

        .btn-secondary:hover {
            background: white;
            color: var(--primary-navy);
        }

        .hero-metrics {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 2.5rem;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .metrics-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
        }

        .metric {
            text-align: center;
        }

        .metric-value {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--accent-teal);
            display: block;
        }

        .metric-label {
            font-size: 0.9rem;
            opacity: 0.9;
            margin-top: 0.5rem;
        }

        /* Trust Bar */
        .trust-bar {
            background: var(--light-gray);
            padding: 2rem;
            border-bottom: 1px solid #e0e0e0;
        }

        .trust-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 2rem;
        }

        .trust-item {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            font-size: 0.95rem;
            color: var(--text-gray);
        }

        .trust-icon {
            width: 24px;
            height: 24px;
            color: var(--accent-teal);
        }

        /* Problem Section */
        #problem {
            padding: 5rem 2rem;
            background: white;
        }

        .section-header {
            text-align: center;
            max-width: 800px;
            margin: 0 auto 3rem;
        }

        .section-header h2 {
            font-size: 2.5rem;
            color: var(--primary-navy);
            margin-bottom: 1rem;
        }

        .section-header p {
            font-size: 1.15rem;
            color: var(--text-gray);
            line-height: 1.8;
        }

        .problem-cards {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .problem-card {
            background: linear-gradient(135deg, #fff 0%, #f8f9fa 100%);
            padding: 2rem;
            border-radius: 15px;
            border-left: 4px solid var(--accent-orange);
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }

        .problem-card::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 100px;
            height: 100px;
            background: var(--accent-orange);
            opacity: 0.05;
            border-radius: 50%;
            transform: translate(30px, -30px);
        }

        .problem-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .problem-card h3 {
            color: var(--primary-navy);
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 0.75rem;
        }

        .problem-icon {
            width: 32px;
            height: 32px;
            color: var(--accent-orange);
        }

        .problem-stat {
            font-size: 2rem;
            font-weight: 700;
            color: var(--accent-orange);
            display: block;
            margin: 1rem 0;
        }

        /* Solution Section */
        #solution {
            padding: 5rem 2rem;
            background: var(--light-gray);
            position: relative;
        }

        .solution-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        .solution-visual {
            margin: 3rem 0;
            padding: 3rem;
            background: white;
            border-radius: 20px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.08);
        }

        .solution-diagram {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            align-items: center;
            text-align: center;
        }

        .solution-step {
            padding: 1.5rem;
            position: relative;
        }

        .solution-step::after {
            content: '→';
            position: absolute;
            right: -2rem;
            top: 50%;
            transform: translateY(-50%);
            font-size: 2rem;
            color: var(--accent-teal);
            opacity: 0.5;
        }

        .solution-step:last-child::after {
            display: none;
        }

        .step-icon {
            width: 80px;
            height: 80px;
            margin: 0 auto 1rem;
            background: linear-gradient(135deg, var(--accent-teal) 0%, #00796b 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 2rem;
        }

        .solution-features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .feature-card {
            background: white;
            padding: 2rem;
            border-radius: 12px;
            text-align: center;
            transition: all 0.3s;
            border: 2px solid transparent;
        }

        .feature-card:hover {
            border-color: var(--accent-teal);
            transform: translateY(-3px);
            box-shadow: 0 5px 20px rgba(0,168,150,0.15);
        }

        .feature-icon {
            width: 60px;
            height: 60px;
            margin: 0 auto 1rem;
            color: var(--accent-teal);
        }

        /* Market Section */
        #market {
            padding: 5rem 2rem;
            background: white;
        }

        .market-visual {
            max-width: 1000px;
            margin: 3rem auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .market-chart {
            position: relative;
            height: 400px;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            border-radius: 20px;
            padding: 2rem;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .tam-sam-som {
            position: relative;
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .market-circle {
            position: absolute;
            border-radius: 50%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            transition: all 0.3s;
        }

        .tam {
            width: 280px;
            height: 280px;
            background: rgba(52, 152, 219, 0.1);
            border: 3px solid var(--water-blue);
            z-index: 1;
            padding: 20px;
        }

        .sam {
            width: 200px;
            height: 200px;
            background: rgba(0, 168, 150, 0.15);
            border: 3px solid var(--accent-teal);
            z-index: 2;
            padding: 20px;
        }

        .som {
            width: 120px;
            height: 120px;
            background: rgba(255, 107, 53, 0.2);
            border: 3px solid var(--accent-orange);
            z-index: 3;
            padding: 15px;
        }

        .market-circle:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }

        .market-value {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary-navy);
            display: block;
            line-height: 1;
            margin-bottom: 0.25rem;
        }

        .som .market-value {
            font-size: 1.4rem;
        }

        .market-label {
            font-size: 0.75rem;
            color: var(--text-gray);
            line-height: 1.2;
            font-weight: 500;
        }

        .market-details h3 {
            color: var(--primary-navy);
            margin-bottom: 1.5rem;
        }

        .market-list {
            list-style: none;
        }

        .market-list li {
            padding: 1rem 0;
            border-bottom: 1px solid #e0e0e0;
            display: flex;
            align-items: center;
            gap: 0.75rem;
        }

        .market-list li:last-child {
            border-bottom: none;
        }

        .checkmark {
            color: var(--success-green);
            font-size: 1.2rem;
        }

        /* Team Section */
        #team {
            padding: 5rem 2rem;
            background: var(--light-gray);
        }

        .team-grid {
            max-width: 1200px;
            margin: 3rem auto 0;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .team-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            transition: all 0.3s;
            box-shadow: 0 3px 15px rgba(0,0,0,0.08);
        }

        .team-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }

        .team-photo {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, var(--accent-teal) 0%, var(--primary-navy) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: white;
            font-weight: 700;
        }

        .team-info {
            padding: 1.5rem;
        }

        .team-name {
            font-size: 1.25rem;
            font-weight: 700;
            color: var(--primary-navy);
            margin-bottom: 0.25rem;
        }

        .team-role {
            color: var(--accent-teal);
            font-weight: 600;
            margin-bottom: 0.75rem;
        }

        .team-bio {
            font-size: 0.9rem;
            color: var(--text-gray);
            line-height: 1.6;
        }

        .advisor-section {
            margin-top: 4rem;
            padding-top: 3rem;
            border-top: 2px solid #e0e0e0;
        }

        .advisor-section h3 {
            text-align: center;
            color: var(--primary-navy);
            margin-bottom: 2rem;
        }

        /* Progress Timeline */
        #progress {
            padding: 5rem 2rem;
            background: white;
            position: relative;
            overflow: hidden;
        }

        .timeline {
            max-width: 1200px;
            margin: 3rem auto;
            position: relative;
        }

        .timeline-pipe {
            position: absolute;
            left: 0;
            right: 0;
            top: 50%;
            transform: translateY(-50%);
            height: 60px;
            background: linear-gradient(90deg, 
                var(--accent-teal) 0%, 
                var(--accent-teal) 40%, 
                rgba(0, 168, 150, 0.5) 40%,
                rgba(0, 168, 150, 0.5) 100%);
            border-radius: 30px;
            box-shadow: inset 0 -5px 10px rgba(0,0,0,0.1);
        }

        .timeline-pipe::before {
            content: '';
            position: absolute;
            left: 0;
            right: 0;
            top: 10px;
            height: 40px;
            background: linear-gradient(90deg,
                rgba(255,255,255,0.2) 0%,
                rgba(255,255,255,0) 100%);
            border-radius: 20px;
        }

        .timeline-items {
            display: flex;
            justify-content: space-between;
            position: relative;
            z-index: 2;
            padding: 0 2rem;
        }

        .timeline-item {
            flex: 1;
            text-align: center;
            position: relative;
        }

        .timeline-valve {
            width: 80px;
            height: 80px;
            margin: 0 auto 1.5rem;
            background: white;
            border-radius: 50%;
            border: 4px solid var(--accent-teal);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            transition: all 0.3s;
        }

        .timeline-item.completed .timeline-valve {
            background: var(--accent-teal);
            color: white;
        }

        .timeline-item.current .timeline-valve {
            border-color: var(--accent-orange);
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(255, 107, 53, 0.4); }
            70% { box-shadow: 0 0 0 15px rgba(255, 107, 53, 0); }
            100% { box-shadow: 0 0 0 0 rgba(255, 107, 53, 0); }
        }

        .timeline-valve-icon {
            font-size: 2rem;
            font-weight: 700;
        }

        .timeline-content {
            max-width: 200px;
            margin: 0 auto;
        }

        .timeline-date {
            font-size: 0.85rem;
            color: var(--accent-teal);
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .timeline-title {
            font-size: 1.1rem;
            font-weight: 700;
            color: var(--primary-navy);
            margin-bottom: 0.5rem;
        }

        .timeline-description {
            font-size: 0.9rem;
            color: var(--text-gray);
            line-height: 1.4;
            display: none;
        }

        .timeline-item:hover .timeline-description {
            display: block;
        }

        .timeline-item:hover .timeline-valve {
            transform: scale(1.1);
        }

        /* Mobile Timeline */
        @media (max-width: 968px) {
            .timeline-items {
                flex-direction: column;
                padding: 0;
            }

            .timeline-pipe {
                width: 60px;
                height: 100%;
                left: 50%;
                top: 0;
                transform: translateX(-50%);
                background: linear-gradient(180deg, 
                    var(--accent-teal) 0%, 
                    var(--accent-teal) 40%, 
                    rgba(0, 168, 150, 0.5) 40%,
                    rgba(0, 168, 150, 0.5) 100%);
            }

            .timeline-item {
                margin-bottom: 2rem;
            }

            .timeline-content {
                max-width: 300px;
            }

            .timeline-description {
                display: block;
            }
        }

        /* ROI Calculator */
        #roi {
            padding: 5rem 2rem;
            background: linear-gradient(135deg, var(--primary-navy) 0%, #1a3d4d 100%);
            color: white;
        }

        .roi-calculator {
            max-width: 900px;
            margin: 3rem auto;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 3rem;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .calculator-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .calculator-inputs h4 {
            margin-bottom: 1.5rem;
            color: var(--accent-teal);
        }

        .input-group {
            margin-bottom: 1.5rem;
        }

        .input-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-size: 0.9rem;
            opacity: 0.9;
        }

        .input-group input {
            width: 100%;
            padding: 0.75rem;
            border-radius: 8px;
            border: 1px solid rgba(255, 255, 255, 0.3);
            background: rgba(255, 255, 255, 0.1);
            color: white;
            font-size: 1rem;
        }

        .calculator-results {
            background: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: 12px;
        }

        .result-item {
            margin-bottom: 1.5rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .result-item:last-child {
            border-bottom: none;
        }

        .result-label {
            font-size: 0.9rem;
            opacity: 0.8;
            margin-bottom: 0.5rem;
        }

        .result-value {
            font-size: 2rem;
            font-weight: 700;
            color: var(--accent-teal);
        }

        /* CTA Section */
        .cta-section {
            padding: 5rem 2rem;
            background: var(--light-gray);
            text-align: center;
        }

        .cta-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .cta-content h2 {
            font-size: 2.5rem;
            color: var(--primary-navy);
            margin-bottom: 1rem;
        }

        .cta-content p {
            font-size: 1.15rem;
            color: var(--text-gray);
            margin-bottom: 2rem;
            line-height: 1.8;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        /* Footer */
        footer {
            background: var(--primary-navy);
            color: white;
            padding: 3rem 2rem 2rem;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
        }

        .footer-logos {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 3rem;
            margin-bottom: 2rem;
            padding-bottom: 2rem;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .nmsu-badge {
            font-weight: 600;
            opacity: 0.9;
        }

        .footer-contact {
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
            margin-bottom: 1rem;
        }

        .footer-contact a {
            color: white;
            text-decoration: none;
            opacity: 0.8;
            transition: opacity 0.3s;
        }

        .footer-contact a:hover {
            opacity: 1;
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .hero-content {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .metrics-grid {
                grid-template-columns: 1fr;
            }

            .nav-links {
                display: none;
            }

            .timeline::before {
                left: 20px;
            }

            .timeline-item {
                flex-direction: row !important;
            }

            .timeline-content {
                margin-left: 3rem !important;
                text-align: left !important;
            }

            .timeline-dot {
                left: 20px !important;
            }

            .calculator-grid {
                grid-template-columns: 1fr;
            }

            .market-visual {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">
                <svg class="logo-icon" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                    <circle cx="50" cy="50" r="45" fill="none" stroke="currentColor" stroke-width="3"/>
                    <path d="M30 30 Q50 10 70 30 L70 70 Q50 60 30 70 Z" fill="#00a896"/>
                    <circle cx="50" cy="50" r="5" fill="#ff6b35"/>
                </svg>
                <span>SaniBrau</span>
            </div>
            <ul class="nav-links">
                <li><a href="#problem">Problem</a></li>
                <li><a href="#solution">Solution</a></li>
                <li><a href="#market">Market</a></li>
                <li><a href="#team">Team</a></li>
                <li><a href="#roi">ROI</a></li>
                <li><a href="#partner" class="nav-cta">Partner With Us</a></li>
            </ul>
        </nav>
    </header>

    <section class="hero">
        <div class="hero-content">
            <div class="hero-left">
                <h1>Making <span class="highlight">Enterprise CIP</span> Accessible to Every Craft Brewery</h1>
                <p>We're solving the $180M water waste problem in craft brewing with modular Clean-in-Place automation that starts at $15K—not $150K.</p>
                <div class="hero-ctas">
                    <a href="#roi" class="btn-primary">Calculate Your Savings</a>
                    <a href="#solution" class="btn-secondary">See How It Works</a>
                </div>
            </div>
            <div class="hero-metrics">
                <div class="metrics-grid">
                    <div class="metric">
                        <span class="metric-value">70%</span>
                        <span class="metric-label">Water Recovery Rate</span>
                    </div>
                    <div class="metric">
                        <span class="metric-value">$30K</span>
                        <span class="metric-label">Annual Savings per Brewery</span>
                    </div>
                    <div class="metric">
                        <span class="metric-value">18mo</span>
                        <span class="metric-label">Payback Period</span>
                    </div>
                    <div class="metric">
                        <span class="metric-value">50%</span>
                        <span class="metric-label">Cost vs Traditional CIP</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <div class="trust-bar">
        <div class="trust-content">
            <div class="trust-item">
                <svg class="trust-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                    <path d="M19 14c1.49-1.46 3-3.21 3-5.5A5.5 5.5 0 0 0 16.5 3c-1.76 0-3 .5-4.5 2-1.5-1.5-2.74-2-4.5-2A5.5 5.5 0 0 0 2 8.5c0 2.3 1.5 4.05 3 5.5Z"/>
                </svg>
                <span>Developed at NMSU Engineering</span>
            </div>
            <div class="trust-item">
                <svg class="trust-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                    <path d="M12 2L15.09 8.26L22 9.27L17 14.14L18.18 21.02L12 17.77L5.82 21.02L7 14.14L2 9.27L8.91 8.26L12 2Z"/>
                </svg>
                <span>Patent Pending Technology</span>
            </div>
            <div class="trust-item">
                <svg class="trust-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                    <circle cx="12" cy="12" r="10"/>
                    <polyline points="12 6 12 12 16 14"/>
                </svg>
                <span>6 Months Field Testing</span>
            </div>
            <div class="trust-item">
                <svg class="trust-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                    <path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"/>
                    <circle cx="12" cy="7" r="4"/>
                </svg>
                <span>5 Pilot Breweries</span>
            </div>
        </div>
    </div>

    <section id="problem">
        <div class="section-header">
            <h2>The $180M Problem We're Solving</h2>
            <p>9,000+ craft breweries desperately need CIP automation but can't afford the $150K+ entry price. Meanwhile, they're hemorrhaging money on water, labor, and compliance issues.</p>
        </div>
        
        <div class="problem-cards">
            <div class="problem-card">
                <h3>
                    <svg class="problem-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M12 2v10l3 3"/>
                        <circle cx="12" cy="12" r="10"/>
                    </svg>
                    Excessive Water Waste
                </h3>
                <p>Manual cleaning uses 7-10 gallons of water per gallon of beer produced.</p>
                <span class="problem-stat">$15K-30K/year</span>
                <p>Lost to water and sewer charges—money that could fund growth.</p>
            </div>

            <div class="problem-card">
                <h3>
                    <svg class="problem-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <circle cx="12" cy="8" r="7"/>
                        <polyline points="8.21 13.89 7 23 12 20 17 23 15.79 13.88"/>
                    </svg>
                    Labor Drain
                </h3>
                <p>Brewers spend 30% of production time on manual cleaning instead of brewing.</p>
                <span class="problem-stat">2-3 hours/day</span>
                <p>Of skilled brewer time wasted on repetitive cleaning tasks.</p>
            </div>

            <div class="problem-card">
                <h3>
                    <svg class="problem-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8"/>
                    </svg>
                    Priced Out of Solutions
                </h3>
                <p>Traditional CIP systems start at $150K with 6-month installation.</p>
                <span class="problem-stat">2-3 years profit</span>
                <p>Required upfront for enterprise CIP—impossible for most craft breweries.</p>
            </div>
        </div>
    </section>

    <section id="solution">
        <div class="solution-content">
            <div class="section-header">
                <h2>Modular CIP That Grows With You</h2>
                <p>Start with automated cleaning for $15K. Add water recovery, advanced filtration, or multi-vessel control as you scale. No massive upfront investment, no facility renovation required.</p>
            </div>

            <div class="solution-visual">
                <div class="solution-diagram">
                    <div class="solution-step">
                        <div class="step-icon">1</div>
                        <h4>Base Module</h4>
                        <p>Automated cleaning cycles, chemical dosing, temperature control</p>
                    </div>
                    <div class="solution-step">
                        <div class="step-icon">2</div>
                        <h4>Water Recovery</h4>
                        <p>70%+ reclamation through multi-stage filtration</p>
                    </div>
                    <div class="solution-step">
                        <div class="step-icon">3</div>
                        <h4>Full Integration</h4>
                        <p>Multi-vessel control, compliance logging, predictive maintenance</p>
                    </div>
                </div>
            </div>

            <div class="solution-features">
                <div class="feature-card">
                    <svg class="feature-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <rect x="3" y="3" width="18" height="18" rx="2" ry="2"/>
                        <line x1="9" y1="9" x2="15" y2="9"/>
                        <line x1="9" y1="15" x2="15" y2="15"/>
                    </svg>
                    <h4>Plug & Play Design</h4>
                    <p>Installs in 1 day with standard tri-clamp connections</p>
                </div>
                <div class="feature-card">
                    <svg class="feature-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <polyline points="22 12 18 12 15 21 9 3 6 12 2 12"/>
                    </svg>
                    <h4>Smart Monitoring</h4>
                    <p>Real-time tracking of water usage, chemical levels, cycle efficiency</p>
                </div>
                <div class="feature-card">
                    <svg class="feature-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M12 2.69l5.66 5.66a8 8 0 1 1-11.31 0z"/>
                    </svg>
                    <h4>Water Recovery</h4>
                    <p>Multi-stage filtration achieves 70%+ water reclamation</p>
                </div>
                <div class="feature-card">
                    <svg class="feature-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <circle cx="12" cy="12" r="3"/>
                        <path d="M12 1v6m0 6v6m4.22-10.22l4.24-4.24M6.34 6.34L2.1 2.1"/>
                    </svg>
                    <h4>FDA Compliant</h4>
                    <p>Meets all sanitary standards with automated documentation</p>
                </div>
            </div>
        </div>
    </section>

    <section id="market">
        <div class="section-header">
            <h2>A $180M Opportunity in Water Savings Alone</h2>
            <p>The craft brewing industry is ready for accessible CIP innovation. With 9,000+ breweries facing water costs and sustainability pressure, our modular approach addresses a massive underserved market.</p>
        </div>

        <div class="market-visual">
            <div class="market-chart">
                <div class="tam-sam-som">
                    <div class="market-circle tam">
                        <span class="market-value">$2.1B</span>
                        <span class="market-label">Total Market</span>
                    </div>
                    <div class="market-circle sam">
                        <span class="market-value">$180M</span>
                        <span class="market-label">Serviceable Market</span>
                    </div>
                    <div class="market-circle som">
                        <span class="market-value">$15M</span>
                        <span class="market-label">3-Year Target</span>
                    </div>
                </div>
            </div>
            <div class="market-details">
                <h3>Market Validation</h3>
                <ul class="market-list">
                    <li>
                        <span class="checkmark">✓</span>
                        <span>88% of breweries prioritize water efficiency (Brewers Association)</span>
                    </li>
                    <li>
                        <span class="checkmark">✓</span>
                        <span>74% lack budget for traditional CIP systems</span>
                    </li>
                    <li>
                        <span class="checkmark">✓</span>
                        <span>Average brewery spends $30K/year on water & sewer</span>
                    </li>
                    <li>
                        <span class="checkmark">✓</span>
                        <span>5 pilot breweries committed to testing</span>
                    </li>
                    <li>
                        <span class="checkmark">✓</span>
                        <span>30+ brewery operators validated need in interviews</span>
                    </li>
                </ul>
            </div>
        </div>
    </section>

    <section id="team">
        <div class="section-header">
            <h2>Engineers Who Understand Brewing</h2>
            <p>Our team combines deep technical expertise with real-world brewing experience, supported by NMSU's engineering resources and industry advisors.</p>
        </div>

        <div class="team-grid">
            <div class="team-card">
                <div class="team-photo">KB</div>
                <div class="team-info">
                    <div class="team-name">Russell "Kevin" Buehling</div>
                    <div class="team-role">Co-Founder & CTO</div>
                    <div class="team-bio">Senior EE/CompEng with 5+ years in automation and embedded systems. Leading technical architecture and control system development.</div>
                </div>
            </div>

            <div class="team-card">
                <div class="team-photo">NM</div>
                <div class="team-info">
                    <div class="team-name">Nathan Marlin</div>
                    <div class="team-role">Co-Founder & COO</div>
                    <div class="team-bio">10 years naval engineering experience with power and fluid systems. Managing operations, testing, and brewery partnerships.</div>
                </div>
            </div>

            <div class="team-card">
                <div class="team-photo">ST</div>
                <div class="team-info">
                    <div class="team-name">Dr. Stephen Taylor</div>
                    <div class="team-role">Technical Advisor</div>
                    <div class="team-bio">NMSU Chemical Engineering faculty. Director of Brewery Lab with expertise in brewing processes and water treatment systems.</div>
                </div>
            </div>

            <div class="team-card">
                <div class="team-photo">Team</div>
                <div class="team-info">
                    <div class="team-name">Engineering Team</div>
                    <div class="team-role">Development Team</div>
                    <div class="team-bio">5 engineers across ME, EE, and IE disciplines. Combined 15,000+ hours on project with expertise in fluids, controls, and optimization.</div>
                </div>
            </div>
        </div>

        <div class="advisor-section">
            <h3>Industry Advisors</h3>
            <div class="team-grid">
                <div class="team-card">
                    <div class="team-photo">JD</div>
                    <div class="team-info">
                        <div class="team-name">John Doe</div>
                        <div class="team-role">Brewery Operations Advisor</div>
                        <div class="team-bio">Former Head Brewer, 15+ years experience. Advising on operational integration and industry needs.</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="progress">
        <div class="section-header">
            <h2>From Lab to Brewery Floor</h2>
            <p>We've moved from concept to working prototypes in 6 months, with pilot installations starting Q1 2026.</p>
        </div>

        <div class="timeline">
            <div class="timeline-pipe"></div>
            <div class="timeline-items">
                <div class="timeline-item completed">
                    <div class="timeline-valve">
                        <span class="timeline-valve-icon">✓</span>
                    </div>
                    <div class="timeline-content">
                        <div class="timeline-date">Sept-Oct 2025</div>
                        <div class="timeline-title">Market Validation</div>
                        <div class="timeline-description">30+ brewery interviews. Initial funding secured.</div>
                    </div>
                </div>

                <div class="timeline-item completed">
                    <div class="timeline-valve">
                        <span class="timeline-valve-icon">✓</span>
                    </div>
                    <div class="timeline-content">
                        <div class="timeline-date">Nov-Dec 2025</div>
                        <div class="timeline-title">Prototype 1.0</div>
                        <div class="timeline-description">70% water recovery achieved in lab testing.</div>
                    </div>
                </div>

                <div class="timeline-item current">
                    <div class="timeline-valve">
                        <span class="timeline-valve-icon">⚙</span>
                    </div>
                    <div class="timeline-content">
                        <div class="timeline-date">Jan-Feb 2026</div>
                        <div class="timeline-title">System Testing</div>
                        <div class="timeline-description">Full integration testing at NMSU Brewery Lab.</div>
                    </div>
                </div>

                <div class="timeline-item">
                    <div class="timeline-valve">
                        <span class="timeline-valve-icon">🏭</span>
                    </div>
                    <div class="timeline-content">
                        <div class="timeline-date">Mar-Apr 2026</div>
                        <div class="timeline-title">Pilot Installations</div>
                        <div class="timeline-description">3 partner breweries for real-world validation.</div>
                    </div>
                </div>

                <div class="timeline-item">
                    <div class="timeline-valve">
                        <span class="timeline-valve-icon">🚀</span>
                    </div>
                    <div class="timeline-content">
                        <div class="timeline-date">Q3 2026</div>
                        <div class="timeline-title">Commercial Launch</div>
                        <div class="timeline-description">First 10 commercial installations.</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="roi">
        <div class="section-header" style="color: white;">
            <h2 style="color: white;">Your ROI in Real Numbers</h2>
            <p style="color: rgba(255,255,255,0.9);">See exactly how much SaniBrau can save your brewery based on your production volume.</p>
        </div>

        <div class="roi-calculator">
            <div class="calculator-grid">
                <div class="calculator-inputs">
                    <h4>Your Brewery Details</h4>
                    <div class="input-group">
                        <label>Monthly Beer Production (BBL)</label>
                        <input type="number" id="production" value="100" min="10" max="1000">
                    </div>
                    <div class="input-group">
                        <label>Water Cost ($/1000 gal)</label>
                        <input type="number" id="water-cost" value="12" min="5" max="30" step="0.5">
                    </div>
                    <div class="input-group">
                        <label>Sewer Cost ($/1000 gal)</label>
                        <input type="number" id="sewer-cost" value="15" min="5" max="40" step="0.5">
                    </div>
                </div>

                <div class="calculator-results">
                    <h4 style="color: var(--accent-teal); margin-bottom: 1.5rem;">Projected Savings</h4>
                    <div class="result-item">
                        <div class="result-label">Annual Water Savings</div>
                        <div class="result-value" id="water-savings">$18,900</div>
                    </div>
                    <div class="result-item">
                        <div class="result-label">Labor Hours Saved/Year</div>
                        <div class="result-value" id="labor-savings">730 hrs</div>
                    </div>
                    <div class="result-item">
                        <div class="result-label">Total Annual Savings</div>
                        <div class="result-value" id="total-savings">$32,400</div>
                    </div>
                    <div class="result-item">
                        <div class="result-label">Payback Period</div>
                        <div class="result-value" id="payback">14 months</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="cta-section" id="partner">
        <div class="cta-content">
            <h2>Ready to Save Water and Money?</h2>
            <p>Join our pilot program and be among the first breweries to experience modular CIP automation. Limited spots available for Q1 2026 installations.</p>
            <div class="cta-buttons">
                <a href="mailto:rubueh@nmsu.edu" class="btn-primary">Schedule Consultation</a>
                <a href="#" class="btn-secondary" style="color: var(--primary-navy); border-color: var(--primary-navy);">Download One-Pager</a>
            </div>
        </div>
    </section>

    <footer>
        <div class="footer-content">
            <div class="footer-logos">
                <div class="logo" style="color: white;">
                    <svg class="logo-icon" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                        <circle cx="50" cy="50" r="45" fill="none" stroke="currentColor" stroke-width="3"/>
                        <path d="M30 30 Q50 10 70 30 L70 70 Q50 60 30 70 Z" fill="#00a896"/>
                        <circle cx="50" cy="50" r="5" fill="#ff6b35"/>
                    </svg>
                    <span>SaniBrau</span>
                </div>
                <div class="nmsu-badge">
                    Developed at NMSU School of Engineering
                </div>
            </div>
            <div class="footer-contact">
                <a href="mailto:rubueh@nmsu.edu">rubueh@nmsu.edu</a>
                <a href="mailto:nwmarlin@nmsu.edu">nwmarlin@nmsu.edu</a>
                <a href="tel:915-412-8843">(915) 412-8843</a>
            </div>
            <p style="opacity: 0.7; font-size: 0.9rem;">© 2025 SaniBrau Station | Patent Pending</p>
        </div>
    </footer>

    <script>
        // ROI Calculator
        function updateCalculator() {
            const production = parseFloat(document.getElementById('production').value) || 100;
            const waterCost = parseFloat(document.getElementById('water-cost').value) || 12;
            const sewerCost = parseFloat(document.getElementById('sewer-cost').value) || 15;
            
            // Calculations based on industry averages
            const waterUsageRatio = 7; // gallons water per gallon beer
            const beerPerBBL = 31; // gallons
            const annualProduction = production * 12;
            const annualWaterUsage = annualProduction * beerPerBBL * waterUsageRatio;
            
            // 70% water recovery
            const waterSaved = annualWaterUsage * 0.7;
            const waterSavingsValue = (waterSaved / 1000) * (waterCost + sewerCost);
            
            // Labor savings (2 hours/day @ $25/hour)
            const laborHoursSaved = 2 * 365;
            const laborValue = laborHoursSaved * 25;
            
            const totalSavings = waterSavingsValue + laborValue;
            const systemCost = 30000; // Average system cost
            const paybackMonths = Math.round((systemCost / totalSavings) * 12);
            
            // Update display
            document.getElementById('water-savings').textContent = '$' + waterSavingsValue.toLocaleString(undefined, {maximumFractionDigits: 0});
            document.getElementById('labor-savings').textContent = laborHoursSaved.toLocaleString() + ' hrs';
            document.getElementById('total-savings').textContent = '$' + totalSavings.toLocaleString(undefined, {maximumFractionDigits: 0});
            document.getElementById('payback').textContent = paybackMonths + ' months';
        }
        
        // Add event listeners
        document.getElementById('production').addEventListener('input', updateCalculator);
        document.getElementById('water-cost').addEventListener('input', updateCalculator);
        document.getElementById('sewer-cost').addEventListener('input', updateCalculator);
        
        // Initial calculation
        updateCalculator();
        
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
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
        
        // Intersection Observer for animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);
        
        // Observe sections
        document.querySelectorAll('section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(20px)';
            section.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(section);
        });
    </script>
</body>
</html>

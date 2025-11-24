# rubber-flooring-dubai2
Netlify project
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dubai Rubber Flooring | Gym & Commercial Mats</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        header {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            transition: opacity 0.3s;
        }

        .nav-links a:hover {
            opacity: 0.8;
        }

        .hero {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 6rem 2rem;
            text-align: center;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            animation: fadeInUp 1s 0.2s both;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 1s 0.4s both;
        }

        .btn {
            padding: 1rem 2rem;
            border: none;
            border-radius: 50px;
            font-size: 1rem;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
            text-decoration: none;
            display: inline-block;
        }

        .btn-primary {
            background: white;
            color: #667eea;
            font-weight: bold;
        }

        .btn-secondary {
            background: transparent;
            color: white;
            border: 2px solid white;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 4rem 2rem;
        }

        .section-title {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
            color: #1e3c72;
        }

        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 4rem;
        }

        .benefit-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .benefit-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
        }

        .benefit-card h3 {
            color: #667eea;
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        .products-section {
            background: #f8f9fa;
        }

        .product-table {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        table {
            width: 100%;
            border-collapse: collapse;
        }

        th, td {
            padding: 1.5rem;
            text-align: left;
            border-bottom: 1px solid #e0e0e0;
        }

        th {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            font-weight: bold;
        }

        tr:hover {
            background: #f8f9fa;
        }

        .applications-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }

        .application-item {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            transition: transform 0.3s;
        }

        .application-item:hover {
            transform: scale(1.05);
        }

        .process-steps {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        .step {
            display: flex;
            gap: 2rem;
            align-items: center;
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .step-number {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            font-weight: bold;
            flex-shrink: 0;
        }

        .faq-section {
            background: #f8f9fa;
        }

        .faq-item {
            background: white;
            margin-bottom: 1rem;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        .faq-question {
            padding: 1.5rem;
            cursor: pointer;
            font-weight: bold;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: background 0.3s;
        }

        .faq-question:hover {
            background: #f8f9fa;
        }

        .faq-answer {
            padding: 0 1.5rem;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s, padding 0.3s;
        }

        .faq-answer.active {
            max-height: 300px;
            padding: 1.5rem;
        }

        .contact-section {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            text-align: center;
        }

        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .contact-card {
            background: rgba(255,255,255,0.1);
            padding: 2rem;
            border-radius: 15px;
            backdrop-filter: blur(10px);
        }

        .contact-card h3 {
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }

        .contact-card a {
            color: white;
            text-decoration: none;
            transition: opacity 0.3s;
        }

        .contact-card a:hover {
            opacity: 0.8;
        }

        footer {
            background: #1a1a1a;
            color: white;
            text-align: center;
            padding: 2rem;
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

        .maintenance-tips {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .tip-card {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            color: white;
            padding: 2rem;
            border-radius: 15px;
            transition: transform 0.3s;
        }

        .tip-card:hover {
            transform: translateY(-5px);
        }

        .tip-card h3 {
            margin-bottom: 1rem;
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }

            .nav-links {
                display: none;
            }

            .step {
                flex-direction: column;
                text-align: center;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">Dubai Rubber Flooring</div>
            <ul class="nav-links">
                <li><a href="#benefits">Benefits</a></li>
                <li><a href="#products">Products</a></li>
                <li><a href="#process">Process</a></li>
                <li><a href="#faq">FAQ</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section class="hero">
        <h1>Premium Rubber Flooring Solutions in Dubai</h1>
        <p>Durable, Safe & Versatile Flooring for Gyms, Commercial Spaces & More</p>
        <div class="cta-buttons">
            <a href="https://dubairubberflooring.ae/" class="btn btn-primary">Dubai Rubber Flooring</a>
            <a href="tel:+971503900299" class="btn btn-secondary">Call Us Now</a>
        </div>
    </section>

    <section id="benefits" class="container">
        <h2 class="section-title">Why Choose Rubber Flooring?</h2>
        <div class="benefits-grid">
            <div class="benefit-card">
                <h3>🛡️ Shock Absorption & Safety</h3>
                <p>Naturally cushions impact, perfect for gyms with heavy weights. Reduces injury risk by softening falls and provides slip resistance even when wet.</p>
            </div>
            <div class="benefit-card">
                <h3>💪 Durability Under High Use</h3>
                <p>Withstands constant foot traffic, dropped weights, and heavy equipment. Resistant to tears, abrasions, and long-term wear.</p>
            </div>
            <div class="benefit-card">
                <h3>🔇 Noise Reduction</h3>
                <p>Dampens sound from dropping weights or footsteps. Ideal for shared walls or multi-use buildings.</p>
            </div>
            <div class="benefit-card">
                <h3>☀️ Weather & UV Resistance</h3>
                <p>Outdoor rubber flooring handles harsh Dubai sun, rain, and temperature fluctuations. UV-resistant variants prevent fading.</p>
            </div>
            <div class="benefit-card">
                <h3>🧹 Easy Maintenance</h3>
                <p>Simple to clean with sweeping and mopping. Doesn't trap dust or allergens, making it hygienic.</p>
            </div>
            <div class="benefit-card">
                <h3>♻️ Eco-Friendly Options</h3>
                <p>Made from recycled rubber, contributing to sustainable building practices. Long lifespan reduces waste.</p>
            </div>
        </div>
    </section>

    <section id="products" class="products-section">
        <div class="container">
            <h2 class="section-title">Our Product Range</h2>
            <div class="product-table">
                <table>
                    <thead>
                        <tr>
                            <th>Product Type</th>
                            <th>Description & Typical Use</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><strong>Rubber Rolls</strong></td>
                            <td>Continuous sheets ideal for gyms, fitness centers, and large commercial areas. Seamless finish, easy to install.</td>
                        </tr>
                        <tr>
                            <td><strong>Interlocking Rubber Tiles</strong></td>
                            <td>Modular tiles that lock together. Easy to install, replace, or rearrange for gyms and play areas.</td>
                        </tr>
                        <tr>
                            <td><strong>Rubber Pavers</strong></td>
                            <td>Durable thick tiles for outdoor areas, rooftops, driveways, or terraces.</td>
                        </tr>
                        <tr>
                            <td><strong>EPDM Rubber Tiles</strong></td>
                            <td>Color variety, UV-resistance, excellent durability. Perfect for playgrounds and decorative flooring.</td>
                        </tr>
                        <tr>
                            <td><strong>Rubber Mats</strong></td>
                            <td>Anti-fatigue mats, door mats, pool mats, workshop mats. Custom sizes available.</td>
                        </tr>
                        <tr>
                            <td><strong>Commercial Rubber Sheets</strong></td>
                            <td>Heavy-duty sheets for warehouses, kitchens, workshops, and industrial use.</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </section>

    <section id="applications" class="container">
        <h2 class="section-title">Key Applications</h2>
        <div class="applications-grid">
            <div class="application-item">
                <h3>🏋️ Gyms & Fitness Studios</h3>
                <p>Protects floors, reduces noise, prevents damage</p>
            </div>
            <div class="application-item">
                <h3>🎮 Playgrounds & Kids' Areas</h3>
                <p>Soft cushioning, UV-resistant for outdoors</p>
            </div>
            <div class="application-item">
                <h3>🏢 Commercial Offices</h3>
                <p>Durable, quiet, visually appealing</p>
            </div>
            <div class="application-item">
                <h3>🏭 Industrial Workplaces</h3>
                <p>Chemical resistant, comfortable standing</p>
            </div>
            <div class="application-item">
                <h3>🌤️ Outdoor Terraces</h3>
                <p>Weather and slip-resistant</p>
            </div>
            <div class="application-item">
                <h3>🚗 Garages & Workshops</h3>
                <p>Easy to clean, oil-resistant</p>
            </div>
        </div>
    </section>

    <section id="process" class="container" style="background: #f8f9fa; margin: 0; padding: 4rem 2rem; max-width: 100%;">
        <div style="max-width: 1200px; margin: 0 auto;">
            <h2 class="section-title">Our Process</h2>
            <div class="process-steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <div>
                        <h3>Consultation & Site Survey</h3>
                        <p>We understand your space, usage, and requirements with an on-site assessment.</p>
                    </div>
                </div>
                <div class="step">
                    <div class="step-number">2</div>
                    <div>
                        <h3>Material & Design Selection</h3>
                        <p>Choose from different thicknesses, colors, densities, and styles. Request free samples.</p>
                    </div>
                </div>
                <div class="step">
                    <div class="step-number">3</div>
                    <div>
                        <h3>Quotation & Customization</h3>
                        <p>Transparent quotes with options for custom designs including logos and branding.</p>
                    </div>
                </div>
                <div class="step">
                    <div class="step-number">4</div>
                    <div>
                        <h3>Professional Installation</h3>
                        <p>Experienced technicians ensure level, safe, and clean installation.</p>
                    </div>
                </div>
                <div class="step">
                    <div class="step-number">5</div>
                    <div>
                        <h3>Quality Check & Handover</h3>
                        <p>Final inspection to ensure perfect fitting and safety.</p>
                    </div>
                </div>
                <div class="step">
                    <div class="step-number">6</div>
                    <div>
                        <h3>Aftercare & Warranty</h3>
                        <p>Maintenance guidance and performance guarantees.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="maintenance" class="container">
        <h2 class="section-title">Maintenance Tips</h2>
        <div class="maintenance-tips">
            <div class="tip-card">
                <h3>🧹 Routine Cleaning</h3>
                <p>Sweep or vacuum daily. Mop weekly with mild detergent. Avoid harsh chemicals.</p>
            </div>
            <div class="tip-card">
                <h3>✨ Stain Management</h3>
                <p>Wipe spills promptly. Use diluted mild soap for tougher stains.</p>
            </div>
            <div class="tip-card">
                <h3>🛡️ Protective Measures</h3>
                <p>Use furniture pads under heavy equipment. Avoid dragging sharp objects.</p>
            </div>
            <div class="tip-card">
                <h3>🌡️ Temperature Care</h3>
                <p>Leave expansion gaps during installation. Check seams periodically.</p>
            </div>
            <div class="tip-card">
                <h3>🔍 Regular Inspection</h3>
                <p>Check for wear at high-traffic zones. Replace damaged tiles when needed.</p>
            </div>
        </div>
    </section>

    <section id="faq" class="faq-section">
        <div class="container">
            <h2 class="section-title">Frequently Asked Questions</h2>
            <div class="faq-item">
                <div class="faq-question" onclick="toggleFaq(this)">
                    Do you offer free samples?
                    <span>▼</span>
                </div>
                <div class="faq-answer">
                    Yes — you can request free rubber flooring samples from our website to test texture, thickness, and quality.
                </div>
            </div>
            <div class="faq-item">
                <div class="faq-question" onclick="toggleFaq(this)">
                    Can you custom-make rubber mats with logos?
                    <span>▼</span>
                </div>
                <div class="faq-answer">
                    Absolutely. We specialize in custom rubber mats — whether for commercial branding, gyms, or play areas.
                </div>
            </div>
            <div class="faq-item">
                <div class="faq-question" onclick="toggleFaq(this)">
                    Is rubber flooring suitable for outdoor use in Dubai?
                    <span>▼</span>
                </div>
                <div class="faq-answer">
                    Yes. Our outdoor rubber tiles and pavers are UV-resistant and designed to handle Dubai's heat and weather conditions.
                </div>
            </div>
            <div class="faq-item">
                <div class="faq-question" onclick="toggleFaq(this)">
                    How long does installation take?
                    <span>▼</span>
                </div>
                <div class="faq-answer">
                    The timeline depends on the area size and type of flooring, but our installation team works efficiently to minimize disruption.
                </div>
            </div>
            <div class="faq-item">
                <div class="faq-question" onclick="toggleFaq(this)">
                    How durable is the flooring?
                    <span>▼</span>
                </div>
                <div class="faq-answer">
                    With proper installation and maintenance, our rubber flooring can last for many years — even in heavy-use commercial or gym environments.
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="contact-section">
        <div class="container">
            <h2 class="section-title" style="color: white;">Get In Touch</h2>
            <p style="font-size: 1.2rem; margin-bottom: 2rem;">Ready to transform your space with premium rubber flooring?</p>
            <div class="contact-info">
                <div class="contact-card">
                    <h3>📍 Location</h3>
                    <p>Al Quoz First<br>Dubai, UAE</p>
                </div>
                <div class="contact-card">
                    <h3>📞 Phone / WhatsApp</h3>
                    <p><a href="tel:+971503900299">+971 50 390 0299</a></p>
                </div>
                <div class="contact-card">
                    <h3>✉️ Email</h3>
                    <p><a href="mailto:info@dubairubberflooring.ae">info@dubairubberflooring.ae</a></p>
                </div>
                <div class="contact-card">
                    <h3>🌐 Website</h3>
                    <p><a href="https://dubairubberflooring.ae" target="_blank">dubairubberflooring.ae</a></p>
                </div>
            </div>
            <div style="margin-top: 3rem;">
                <a href="tel:+971503900299" class="btn btn-primary" style="margin-right: 1rem;">Call Now</a>
                <a href="mailto:info@dubairubberflooring.ae" class="btn btn-secondary">Send Email</a>
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 Dubai Rubber Flooring. All rights reserved.</p>
        <p style="margin-top: 1rem; opacity: 0.8;">Specialized in Gym Flooring, Commercial Mats, Playground Surfaces & Custom Solutions</p>
    </footer>

    <script>
        function toggleFaq(element) {
            const answer = element.nextElementSibling;
            const icon = element.querySelector('span');
            
            // Close all other FAQs
            document.querySelectorAll('.faq-answer').forEach(item => {
                if (item !== answer) {
                    item.classList.remove('active');
                }
            });
            
            document.querySelectorAll('.faq-question span').forEach(item => {
                if (item !== icon) {
                    item.textContent = '▼';
                }
            });
            
            // Toggle current FAQ
            answer.classList.toggle('active');
            icon.textContent = answer.classList.contains('active') ? '▲' : '▼';
        }

        // Smooth scrolling for navigation links
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

        // Add animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animation = 'fadeInUp 0.8s';
                }
            });
        }, observerOptions);

        document.querySelectorAll('.benefit-card, .step, .application-item, .tip-card').forEach(el => {
            observer.observe(el);
        });
    </script>
</body>
</html>

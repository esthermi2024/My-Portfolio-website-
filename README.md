# My-Portfolio-website-
The link-https://poe.com/AppL5ICIFEVU8


 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aster Mitiku Chali - Full Stack Developer Portfolio</title>
    <style>
        /* Reset and Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        /* Header */
        header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .logo {
            font-size: 1.5rem;
            font-weight: bold;
        }
        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }
        .nav-links a {
            color: white;
            text-decoration: none;
            transition: opacity 0.3s;
        }
        .nav-links a:hover {
            opacity: 0.8;
        }
        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
        }
        .hamburger span {
            width: 25px;
            height: 3px;
            background: white;
            margin: 3px 0;
            transition: 0.3s;
        }
        /* Hero Section */
        #hero {
            padding: 120px 0 80px;
            text-align: center;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }
        .hero-content h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
        }
        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease 0.2s both;
        }
        .location-badge {
            display: inline-block;
            background: rgba(255,255,255,0.2);
            padding: 8px 16px;
            border-radius: 20px;
            margin-bottom: 1rem;
            font-size: 0.9rem;
        }
        .cta-button {
            display: inline-block;
            background: #ff6b6b;
            color: white;
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 50px;
            transition: transform 0.3s, box-shadow 0.3s;
            animation: fadeInUp 1s ease 0.4s both;
        }
        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(255,107,107,0.4);
        }
        /* Sections */
        section {
            padding: 80px 0;
        }
        section h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
        }
        /* About Section */
        #about {
            background: white;
        }
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }
        .about-text p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
        }
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 1rem;
            margin-top: 2rem;
        }
        .skill-tag {
            background: #e9ecef;
            padding: 8px 16px;
            border-radius: 20px;
            text-align: center;
            font-weight: 500;
        }
        /* Projects Section */
        #projects {
            background: #f8f9fa;
        }
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        .project-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 30px rgba(0,0,0,0.15);
        }
        .project-image {
            height: 200px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
            position: relative;
        }
        .project-image::after {
            content: '📱';
            font-size: 3rem;
        }
        .project-content {
            padding: 1.5rem;
        }
        .project-content h3 {
            margin-bottom: 0.5rem;
            color: #333;
        }
        .project-content p {
            color: #666;
            margin-bottom: 1rem;
        }
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }
        .tech-tag {
            background: #667eea;
            color: white;
            padding: 4px 12px;
            border-radius: 12px;
            font-size: 0.85rem;
        }
        /* Contact Section */
        #contact {
            background: white;
        }
        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: start;
        }
        .contact-info h3 {
            margin-bottom: 1rem;
            color: #333;
        }
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
            gap: 1rem;
            padding: 12px;
            background: #f8f9fa;
            border-radius: 8px;
            border-left: 4px solid #667eea;
        }
        .contact-item.phone::before {
            content: '📞';
            font-size: 1.2rem;
        }
        .contact-item.email::before {
            content: '📧';
            font-size: 1.2rem;
        }
        .contact-item.location::before {
            content: '📍';
            font-size: 1.2rem;
        }
        .contact-form {
            background: #f8f9fa;
            padding: 2rem;
            border-radius: 12px;
        }
        .form-group {
            margin-bottom: 1.5rem;
        }
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
        }
        .form-group textarea {
            height: 120px;
            resize: vertical;
        }
        .submit-btn {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1rem;
            transition: transform 0.3s;
            width: 100%;
        }
        .submit-btn:hover {
            transform: translateY(-2px);
        }
        /* Footer */
        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 2rem 0;
        }
        /* Animations */
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
        /* Mobile Responsiveness */
        @media (max-width: 768px) {
            .hamburger {
                display: flex;
            }
            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background: rgba(102, 126, 234, 0.95);
                flex-direction: column;
                padding: 1rem;
                gap: 1rem;
            }
            .nav-links.active {
                display: flex;
            }
            .hero-content h1 {
                font-size: 2rem;
            }
            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
                gap: 2rem;
            }
            .projects-grid {
                grid-template-columns: 1fr;
            }
            section {
                padding: 60px 0;
            }
            #hero {
                padding: 100px 0 60px;
            }
            .contact-item {
                justify-content: space-between;
                font-size: 0.9rem;
            }
        }
        @media (max-width: 480px) {
            .container {
                padding: 0 15px;
            }
            .hero-content h1 {
                font-size: 1.8rem;
            }
            section h2 {
                font-size: 2rem;
            }
            .location-badge {
                font-size: 0.8rem;
                padding: 6px 12px;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <div class="logo">Aster Mitiku Chali</div>
            <ul class="nav-links">
                <li><a href="#hero">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="hamburger">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </nav>
    </header>

    <section id="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Full Stack Developer</h1>
                <div class="location-badge">Based in Ethiopia 🇪🇹</div>
                <p>Building modern web applications with clean code and exceptional user experiences. Passionate about creating innovative solutions that drive impact.</p>
                <a href="#contact" class="cta-button">Get In Touch</a>
            </div>
        </div>
    </section>

    <section id="about">
        <div class="container">
            <h2>About Me</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>I'm a dedicated Full Stack Developer based in Ethiopia with 5+ years of experience creating scalable web applications. I specialize in modern JavaScript frameworks and love turning complex problems into elegant, efficient solutions.</p>
                    <p>From crafting beautiful user interfaces to architecting robust backend systems, I enjoy every aspect of development. Currently focused on React, Node.js, and cloud-native architectures. Passionate about contributing to Ethiopia's growing tech ecosystem.</p>
                    <div class="skills-grid">
                        <div class="skill-tag">React</div>
                        <div class="skill-tag">Node.js</div>
                        <div class="skill-tag">JavaScript</div>
                        <div class="skill-tag">TypeScript</div>
                        <div class="skill-tag">Python</div>
                        <div class="skill-tag">MongoDB</div>
                        <div class="skill-tag">PostgreSQL</div>
                        <div class="skill-tag">AWS</div>
                        <div class="skill-tag">Docker</div>
                        <div class="skill-tag">Git</div>
                    </div>
                </div>
                <div style="text-align: center;">
                    <div style="width: 250px; height: 250px; background: linear-gradient(135deg, #667eea, #764ba2); border-radius: 50%; margin: 0 auto; display: flex; align-items: center; justify-content: center; color: white; font-size: 4rem;">👨‍💻</div>
                </div>
            </div>
        </div>
    </section>

    <section id="projects">
        <div class="container">
            <h2>Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-image"></div>
                    <div class="project-content">
                        <h3>E-Commerce Platform</h3>
                        <p>A full-stack e-commerce solution built with React, Node.js, and MongoDB. Features real-time inventory management, secure payments, and responsive design tailored for African markets.</p>
                        <div class="project-tech">
                            <span class="tech-tag">React</span>
                            <span class="tech-tag">Node.js</span>
                            <span class="tech-tag">MongoDB</span>
                            <span class="tech-tag">Stripe</span>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-image" style="background: linear-gradient(45deg, #f093fb, #f5576c);"></div>
                    <div class="project-content">
                        <h3>Social Media Dashboard</h3>
                        <p>Analytics dashboard for social media performance. Built with Next.js and integrated with multiple social media APIs for real-time data visualization and insights.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Next.js</span>
                            <span class="tech-tag">Chart.js</span>
                            <span class="tech-tag">APIs</span>
                            <span class="tech-tag">TypeScript</span>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-image" style="background: linear-gradient(45deg, #4facfe, #00f2fe);"></div>
                    <div class="project-content">
                        <h3>Task Management App</h3>
                        <p>Collaborative task management application with real-time updates using WebSockets. Features drag-and-drop interface and team collaboration tools for remote teams.</p>
                        <div class="project-tech">
                            <span class="tech-tag">React</span>
                            <span class="tech-tag">Socket.io</span>
                            <span class="tech-tag">Express</span>
                            <span class="tech-tag">PostgreSQL</span>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-image" style="background: linear-gradient(45deg, #43e97b, #38f9d7);"></div>
                    <div class="project-content">
                        <h3>Local Business Directory</h3>
                        <p>Digital directory for Ethiopian businesses featuring location-based search, reviews, and multilingual support. Built to support local commerce and digital transformation.</p>
                        <div class="project-tech">
                            <span class="tech-tag">React Native</span>
                            <span class="tech-tag">Firebase</span>
                            <span class="tech-tag">Google Maps</span>
                            <span class="tech-tag">Amharic Support</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <h2>Let's Work Together</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Get In Touch</h3>
                    <div class="contact-item phone">+251 90 280 2169</div>
                    <div class="contact-item email">astermitiku2018@gmail.com</div>
                    <div class="contact-item location">Addis Ababa, Ethiopia</div>
                    <div class="contact-item" style="border-left-color: #ff6b6b; background: rgba(255,107,107,0.1);">
                        Available for freelance & full-time opportunities
                    </div>
                    <div style="margin-top: 2rem; padding: 1rem; background: #e8f5e8; border-radius: 8px; border-left: 4px solid #28a745;">
                        <strong>Time Zone:</strong> EAT (UTC+3) - Ready to collaborate across time zones!
                    </div>
                </div>
                <form class="contact-form" id="contactForm">
                    <div class="form-group">
                        <label for="name">Your Name</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Your Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="subject">Subject</label>
                        <input type="text" id="subject" name="subject" placeholder="Project collaboration, job opportunity, etc." required>
                    </div>
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" name="message" placeholder="Tell me about your project or opportunity..." required></textarea>
                    </div>
                    <button type="submit" class="submit-btn">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2024 Aster Mitiku Chali. All rights reserved. | Building the future of tech from Ethiopia with ❤️</p>
        </div>
    </footer>

    <script>
        // Mobile Navigation Toggle
        const hamburger = document.querySelector('.hamburger');
        const navLinks = document.querySelector('.nav-links');

        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Smooth Scrolling for Navigation Links
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
                // Close mobile menu if open
                navLinks.classList.remove('active');
            });
        });

        // Contact Form Handling
        const contactForm = document.getElementById('contactForm');
        contactForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form data
            const formData = new FormData(contactForm);
            const name = formData.get('name');
            const email = formData.get('email');
            const subject = formData.get('subject');
            const message = formData.get('message');
            
            // Simple form validation
            if (!name || !email || !subject || !message) {
                // Custom modal simulation since alert() is disabled in Poe Canvas
                const notification = document.createElement('div');
                notification.style.cssText = `
                    position: fixed; top: 20px; right: 20px; background: #ff6b6b; 
                    color: white; padding: 15px 20px; border-radius: 8px; 
                    z-index: 10000; box-shadow: 0 4px 12px rgba(0,0,0,0.15);
                    animation: slideIn 0.3s ease;
                `;
                notification.textContent = 'Please fill in all fields.';
                document.body.appendChild(notification);
                
                setTimeout(() => {
                    notification.remove();
                }, 3000);
                return;
            }
            
            // Simulate form submission
            const submitBtn = contactForm.querySelector('.submit-btn');
            const originalText = submitBtn.textContent;
            submitBtn.textContent = 'Sending...';
            submitBtn.disabled = true;
            
            // Simulate API call
            setTimeout(() => {
                submitBtn.textContent = 'Message Sent! 🎉';
                submitBtn.style.background = 'linear-gradient(135deg, #28a745, #20c997)';
                
                // Show success notification
                const successNotification = document.createElement('div');
                successNotification.style.cssText = `
                    position: fixed; top: 20px; right: 20px; background: #28a745; 
                    color: white; padding: 15px 20px; border-radius: 8px; 
                    z-index: 10000; box-shadow: 0 4px 12px rgba(0,0,0,0.15);
                    animation: slideIn 0.3s ease;
                `;
                successNotification.innerHTML = `
                    <strong>Success!</strong><br>
                    Your message has been sent to Aster. You'll hear back soon!
                `;
                document.body.appendChild(successNotification);
                
                contactForm.reset();
                setTimeout(() => {
                    submitBtn.textContent = originalText;
                    submitBtn.disabled = false;
                    submitBtn.style.background = 'linear-gradient(135deg, #667eea 0%, #764ba2 100%)';
                    successNotification.remove();
                }, 3000);
            }, 1500);
        });

        // Add slideIn animation
        const style = document.createElement('style');
        style.textContent = `
            @keyframes slideIn {
                from { transform: translateX(100%); opacity: 0; }
                to { transform: translateX(0); opacity: 1; }
            }
        `;
        document.head.appendChild(style);

        // Add scroll effect to header
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(102, 126, 234, 0.95)';
                header.style.backdropFilter = 'blur(10px)';
            } else {
                header.style.background = 'linear-gradient(135deg, #667eea 0%, #764ba2 100%)';
                header.style.backdropFilter = 'none';
            }
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

        // Observe project cards and sections
        document.querySelectorAll('.project-card, section').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(20px)';
            el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(el);
        });

        // Phone number click handler (for copying)
        document.querySelector('.contact-item.phone').addEventListener('click', function() {
            const phone = this.textContent.trim();
            navigator.clipboard.writeText(phone).then(() => {
                const originalText = this.textContent;
                this.textContent = 'Copied to clipboard! 📋';
                setTimeout(() => {
                    this.textContent = originalText;
                }, 2000);
            });
        });

        // Email click handler (for copying)
        document.querySelector('.contact-item.email').addEventListener('click', function() {
            const email = this.textContent.trim();
            navigator.clipboard.writeText(email).then(() => {
                const originalText = this.textContent;
                this.textContent = 'Copied to clipboard! 📧';
                setTimeout(() => {
                    this.textContent = originalText;
                }, 2000);
            });
        });
    </script>
</body>
</html>


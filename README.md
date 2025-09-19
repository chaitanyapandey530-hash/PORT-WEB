# PORT-WEB
THIS IS MY PORTFOLIO WEBSITE THAT SHOWCASE MY SKILLS AND ALL
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio Website</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        background: "hsl(var(--background))",
                        foreground: "hsl(var(--foreground))",
                        primary: {
                            DEFAULT: "hsl(var(--primary))",
                            foreground: "hsl(var(--primary-foreground))"
                        },
                        secondary: {
                            DEFAULT: "hsl(var(--secondary))",
                            foreground: "hsl(var(--secondary-foreground))"
                        },
                        muted: {
                            DEFAULT: "hsl(var(--muted))",
                            foreground: "hsl(var(--muted-foreground))"
                        },
                        accent: {
                            DEFAULT: "hsl(var(--accent))",
                            foreground: "hsl(var(--accent-foreground))"
                        },
                        destructive: {
                            DEFAULT: "hsl(var(--destructive))",
                            foreground: "hsl(var(--destructive-foreground))"
                        },
                        border: "hsl(var(--border))",
                        input: "hsl(var(--input))",
                        ring: "hsl(var(--ring))",
                    }
                }
            }
        }
    </script>
    <style>
        :root {
            --background: 0 0% 100%;
            --foreground: 222.2 84% 4.9%;
            --primary: 222.2 47.4% 11.2%;
            --primary-foreground: 210 40% 98%;
            --secondary: 210 40% 96%;
            --secondary-foreground: 222.2 84% 4.9%;
            --muted: 210 40% 96%;
            --muted-foreground: 215.4 16.3% 46.9%;
            --accent: 210 40% 96%;
            --accent-foreground: 222.2 84% 4.9%;
            --destructive: 0 84.2% 60.2%;
            --destructive-foreground: 210 40% 98%;
            --border: 214.3 31.8% 91.4%;
            --input: 214.3 31.8% 91.4%;
            --ring: 222.2 84% 4.9%;
        }

        .dark {
            --background: 222.2 84% 4.9%;
            --foreground: 210 40% 98%;
            --primary: 210 40% 98%;
            --primary-foreground: 222.2 47.4% 11.2%;
            --secondary: 217.2 32.6% 17.5%;
            --secondary-foreground: 210 40% 98%;
            --muted: 217.2 32.6% 17.5%;
            --muted-foreground: 215 20.2% 65.1%;
            --accent: 217.2 32.6% 17.5%;
            --accent-foreground: 210 40% 98%;
            --destructive: 0 62.8% 30.6%;
            --destructive-foreground: 210 40% 98%;
            --border: 217.2 32.6% 17.5%;
            --input: 217.2 32.6% 17.5%;
            --ring: 212.7 26.8% 83.9%;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: hsl(var(--foreground));
            background-color: hsl(var(--background));
        }

        .section {
            padding: 5rem 1rem;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        .btn {
            display: inline-block;
            padding: 0.75rem 1.5rem;
            border-radius: 0.375rem;
            font-weight: 500;
            text-align: center;
            transition: all 0.2s;
            cursor: pointer;
        }

        .btn-primary {
            background-color: hsl(var(--primary));
            color: hsl(var(--primary-foreground));
        }

        .btn-primary:hover {
            background-color: hsl(var(--primary) / 0.9);
        }

        .btn-secondary {
            background-color: hsl(var(--secondary));
            color: hsl(var(--secondary-foreground));
            border: 1px solid hsl(var(--border));
        }

        .btn-secondary:hover {
            background-color: hsl(var(--secondary) / 0.8);
        }

        .card {
            background-color: hsl(var(--background));
            border: 1px solid hsl(var(--border));
            border-radius: 0.5rem;
            padding: 1.5rem;
            transition: transform 0.2s, box-shadow 0.2s;
        }

        .card:hover {
            transform: translateY(-4px);
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1);
        }

        .nav-link {
            position: relative;
            padding: 0.5rem 0;
            color: hsl(var(--foreground));
            transition: color 0.2s;
        }

        .nav-link:hover {
            color: hsl(var(--primary));
        }

        .nav-link::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: hsl(var(--primary));
            transition: width 0.3s;
        }

        .nav-link:hover::after {
            width: 100%;
        }

        .skill-badge {
            display: inline-flex;
            align-items: center;
            padding: 0.25rem 0.75rem;
            border-radius: 9999px;
            background-color: hsl(var(--secondary));
            color: hsl(var(--secondary-foreground));
            font-size: 0.875rem;
            margin: 0.25rem;
        }

        .project-image {
            border-radius: 0.5rem;
            overflow: hidden;
            height: 200px;
            background-color: hsl(var(--muted));
            display: flex;
            align-items: center;
            justify-content: center;
        }

        input, textarea {
            width: 100%;
            padding: 0.75rem;
            border: 1px solid hsl(var(--border));
            border-radius: 0.375rem;
            background-color: hsl(var(--background));
            color: hsl(var(--foreground));
        }

        input:focus, textarea:focus {
            outline: none;
            border-color: hsl(var(--ring));
            box-shadow: 0 0 0 2px hsl(var(--ring) / 0.2);
        }
    </style>
</head>
<body class="bg-background text-foreground">
    <!-- Navigation -->
    <header class="sticky top-0 z-50 w-full border-b bg-background/95 backdrop-blur supports-[backdrop-filter]:bg-background/60">
        <div class="container flex h-16 items-center justify-between">
            <div class="text-xl font-bold">Portfolio</div>
            <nav class="hidden md:flex space-x-8">
                <a href="#home" class="nav-link">Home</a>
                <a href="#about" class="nav-link">About</a>
                <a href="#skills" class="nav-link">Skills</a>
                <a href="#projects" class="nav-link">Projects</a>
                <a href="#contact" class="nav-link">Contact</a>
            </nav>
            <button class="md:hidden" id="mobile-menu-btn">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                    <line x1="4" x2="20" y1="12" y2="12"></line>
                    <line x1="4" x2="20" y1="6" y2="6"></line>
                    <line x1="4" x2="20" y1="18" y2="18"></line>
                </svg>
            </button>
        </div>
        <div class="md:hidden hidden bg-background border-b" id="mobile-menu">
            <div class="container py-4 flex flex-col space-y-4">
                <a href="#home" class="nav-link">Home</a>
                <a href="#about" class="nav-link">About</a>
                <a href="#skills" class="nav-link">Skills</a>
                <a href="#projects" class="nav-link">Projects</a>
                <a href="#contact" class="nav-link">Contact</a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="section min-h-screen flex items-center">
        <div class="container">
            <div class="max-w-2xl mx-auto text-center">
                <h1 class="text-4xl md:text-6xl font-bold mb-6">Hi, I'm <span class="text-primary">John Doe</span></h1>
                <p class="text-xl md:text-2xl text-muted-foreground mb-8">Frontend Developer & UI Designer</p>
                <p class="text-lg mb-10">I create beautiful, functional websites and applications with modern technologies.</p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center">
                    <a href="#projects" class="btn btn-primary">View My Work</a>
                    <a href="#contact" class="btn btn-secondary">Contact Me</a>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section bg-muted">
        <div class="container">
            <h2 class="text-3xl font-bold text-center mb-12">About Me</h2>
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div>
                    <img src="https://placeholder-image-service.onrender.com/image/400x400?prompt=Professional headshot of a web developer with friendly expression&id=c186a61b-335a-441b-99e5-dbff73aa3ae5" alt="Professional headshot of John Doe" class="rounded-lg shadow-lg w-full">
                </div>
                <div>
                    <h3 class="text-2xl font-semibold mb-4">My Journey</h3>
                    <p class="text-muted-foreground mb-6">
                        I'm a passionate frontend developer with 5 years of experience creating responsive and accessible web applications. 
                        I specialize in React, JavaScript, and modern CSS frameworks.
                    </p>
                    <p class="text-muted-foreground mb-6">
                        My approach combines technical expertise with an eye for design, ensuring that every project 
                        I work on is both functional and visually appealing.
                    </p>
                    <div class="flex flex-wrap gap-4">
                        <div class="text-center">
                            <div class="text-2xl font-bold text-primary">50+</div>
                            <div class="text-sm text-muted-foreground">Projects</div>
                        </div>
                        <div class="text-center">
                            <div class="text-2xl font-bold text-primary">25+</div>
                            <div class="text-sm text-muted-foreground">Clients</div>
                        </div>
                        <div class="text-center">
                            <div class="text-2xl font-bold text-primary">5+</div>
                            <div class="text-sm text-muted-foreground">Years Experience</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="section">
        <div class="container">
            <h2 class="text-3xl font-bold text-center mb-12">Skills & Technologies</h2>
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="card text-center">
                    <div class="text-primary mb-4">
                        <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="m12 18 10-6-10-6v12"></path>
                            <path d="m6 18 10-6-10-6v12"></path>
                        </svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Frontend Development</h3>
                    <p class="text-muted-foreground mb-4">Building responsive and interactive user interfaces</p>
                    <div class="flex flex-wrap justify-center">
                        <span class="skill-badge">HTML5</span>
                        <span class="skill-badge">CSS3</span>
                        <span class="skill-badge">JavaScript</span>
                        <span class="skill-badge">React</span>
                        <span class="skill-badge">TypeScript</span>
                        <span class="skill-badge">Tailwind CSS</span>
                    </div>
                </div>

                <div class="card text-center">
                    <div class="text-primary mb-4">
                        <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <rect width="18" height="18" x="3" y="3" rx="2"></rect>
                            <path d="M12 3v18"></path>
                        </svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">UI/UX Design</h3>
                    <p class="text-muted-foreground mb-4">Creating intuitive and beautiful user experiences</p>
                    <div class="flex flex-wrap justify-center">
                        <span class="skill-badge">Figma</span>
                        <span class="skill-badge">Adobe XD</span>
                        <span class="skill-badge">User Research</span>
                        <span class="skill-badge">Wireframing</span>
                        <span class="skill-badge">Prototyping</span>
                    </div>
                </div>

                <div class="card text-center">
                    <div class="text-primary mb-4">
                        <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M14.5 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V7.5L14.5 2z"></path>
                            <polyline points="14 2 14 8 20 8"></polyline>
                        </svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Tools & Technologies</h3>
                    <p class="text-muted-foreground mb-4">Modern development tools and workflows</p>
                    <div class="flex flex-wrap justify-center">
                        <span class="skill-badge">Git</span>
                        <span class="skill-badge">VS Code</span>
                        <span class="skill-badge">Webpack</span>
                        <span class="skill-badge">Jest</span>
                        <span class="skill-badge">Firebase</span>
                        <span class="skill-badge">Netlify</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="section bg-muted">
        <div class="container">
            <h2 class="text-3xl font-bold text-center mb-12">Featured Projects</h2>
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Project 1 -->
                <div class="card">
                    <div class="project-image">
                        <img src="https://placeholder-image-service.onrender.com/image/400x300?prompt=E-commerce website dashboard with product listings and analytics charts&id=c186a61b-335a-441b-99e5-dbff73aa3ae5" alt="E-commerce dashboard interface with product management features">
                    </div>
                    <h3 class="text-xl font-semibold mt-4 mb-2">E-Commerce Dashboard</h3>
                    <p class="text-muted-foreground mb-4">
                        A comprehensive admin dashboard for managing products, orders, and customer data.
                    </p>
                    <div class="flex flex-wrap gap-2 mb-4">
                        <span class="skill-badge">React</span>
                        <span class="skill-badge">TypeScript</span>
                        <span class="skill-badge">Tailwind CSS</span>
                    </div>
                    <div class="flex gap-3">
                        <a href="#" class="text-primary hover:underline">Live Demo</a>
                        <a href="#" class="text-primary hover:underline">GitHub</a>
                    </div>
                </div>

                <!-- Project 2 -->
                <div class="card">
                    <div class="project-image">
                        <img src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Weather application with forecast data and location search&id=c186a61b-335a-441b-99e5-dbff73aa3ae5" alt="Weather application showing current conditions and forecast">
                    </div>
                    <h3 class="text-xl font-semibold mt-4 mb-2">Weather App</h3>
                    <p class="text-muted-foreground mb-4">
                        A responsive weather application with location-based forecasts and beautiful UI.
                    </p>
                    <div class="flex flex-wrap gap-2 mb-4">
                        <span class="skill-badge">JavaScript</span>
                        <span class="skill-badge">API Integration</span>
                        <span class="skill-badge">CSS Animations</span>
                    </div>
                    <div class="flex gap-3">
                        <a href="#" class="text-primary hover:underline">Live Demo</a>
                        <a href="#" class="text-primary hover:underline">GitHub</a>
                    </div>
                </div>

                <!-- Project 3 -->
                <div class="card">
                    <div class="project-image">
                        <img src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Task management application with drag and drop interface&id=c186a61b-335a-441b-99e5-dbff73aa3ae5" alt="Task management app with kanban board interface">
                    </div>
                    <h3 class="text-xl font-semibold mt-4 mb-2">Task Manager</h3>
                    <p class="text-muted-foreground mb-4">
                        A drag-and-drop task management application with team collaboration features.
                    </p>
                    <div class="flex flex-wrap gap-2 mb-4">
                        <span class="skill-badge">React</span>
                        <span class="skill-badge">Firebase</span>
                        <span class="skill-badge">Drag & Drop</span>
                    </div>
                    <div class="flex gap-3">
                        <a href="#" class="text-primary hover:underline">Live Demo</a>
                        <a href="#" class="text-primary hover:underline">GitHub</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">
        <div class="container">
            <h2 class="text-3xl font-bold text-center mb-12">Get In Touch</h2>
            <div class="max-w-md mx-auto">
                <form id="contact-form" class="space-y-6">
                    <div>
                        <label for="name" class="block text-sm font-medium mb-2">Name</label>
                        <input type="text" id="name" name="name" required class="w-full">
                    </div>
                    <div>
                        <label for="email" class="block text-sm font-medium mb-2">Email</label>
                        <input type="email" id="email" name="email" required class="w-full">
                    </div>
                    <div>
                        <label for="message" class="block text-sm font-medium mb-2">Message</label>
                        <textarea id="message" name="message" rows="5" required class="w-full"></textarea>
                    </div>
                    <button type="submit" class="btn btn-primary w-full">Send Message</button>
                </form>
                <div class="mt-12 text-center">
                    <p class="text-muted-foreground mb-4">Or reach out directly at</p>
                    <a href="mailto:john@example.com" class="text-primary text-lg font-medium">john@example.com</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-muted py-12">
        <div class="container">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-6 md:mb-0">
                    <div class="text-xl font-bold">John Doe</div>
                    <p class="text-muted-foreground">Frontend Developer & UI Designer</p>
                </div>
                <div class="flex space-x-6">
                    <a href="#" class="text-muted-foreground hover:text-primary">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M15 22v-4a4.8 4.8 0 0 0-1-3.5c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65-.17.6-.22 1.23-.15 1.85v4"></path>
                            <path d="M9 18c-4.51 2-5-2-7-2"></path>
                        </svg>
                    </a>
                    <a href="#" class="text-muted-foreground hover:text-primary">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path>
                            <rect width="4" height="12" x="2" y="9"></rect>
                            <circle cx="4" cy="4" r="2"></circle>
                        </svg>
                    </a>
                    <a href="#" class="text-muted-foreground hover:text-primary">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <rect width="20" height="16" x="2" y="4" rx="2"></rect>
                            <path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"></path>
                        </svg>
                    </a>
                </div>
            </div>
            <div class="mt-8 text-center text-muted-foreground text-sm">
                <p>© 2023 John Doe. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        document.getElementById('mobile-menu-btn').addEventListener('click', function() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        });

        // Close mobile menu when clicking on links
        document.querySelectorAll('#mobile-menu a').forEach(link => {
            link.addEventListener('click', () => {
                document.getElementById('mobile-menu').classList.add('hidden');
            });
        });

        // Form submission
        document.getElementById('contact-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Simple form validation
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const message = document.getElementById('message').value;
            
            if (!name || !email || !message) {
                alert('Please fill in all fields');
                return;
            }
            
            // In a real application, you would send this data to a server
            alert('Thank you for your message! I\'ll get back to you soon.');
            this.reset();
        });

        // Add smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    targetElement.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
</body>
</html>

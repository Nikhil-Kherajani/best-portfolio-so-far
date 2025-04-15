# best-portfolio-so-far


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alex Carter | Software Developer</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            scroll-behavior: smooth;
        }
        
        .gradient-text {
            background: linear-gradient(90deg, #3b82f6, #8b5cf6);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .card-hover {
            transition: all 0.3s ease;
        }
        
        .card-hover:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        
        .skill-pill {
            transition: all 0.2s ease;
        }
        
        .skill-pill:hover {
            transform: scale(1.05);
        }
        
        .project-card {
            perspective: 1000px;
        }
        
        .project-inner {
            transition: transform 0.6s;
            transform-style: preserve-3d;
        }
        
        .project-card:hover .project-inner {
            transform: rotateY(180deg);
        }
        
        .project-front, .project-back {
            backface-visibility: hidden;
            position: absolute;
            width: 100%;
            height: 100%;
        }
        
        .project-back {
            transform: rotateY(180deg);
        }
        
        .nav-link {
            position: relative;
        }
        
        .nav-link::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -2px;
            left: 0;
            background: linear-gradient(90deg, #3b82f6, #8b5cf6);
            transition: width 0.3s ease;
        }
        
        .nav-link:hover::after {
            width: 100%;
        }
        
        .active-nav::after {
            width: 100%;
        }
        
        .timeline-item::before {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            left: -40px;
            background: linear-gradient(135deg, #3b82f6, #8b5cf6);
            border-radius: 50%;
            top: 5px;
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        .floating {
            animation: float 6s ease-in-out infinite;
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800">
    <!-- Navigation -->
    <nav class="fixed w-full bg-white shadow-sm z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16 items-center">
                <div class="flex-shrink-0 flex items-center">
                    <span class="text-xl font-bold gradient-text">Alex Carter</span>
                </div>
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-8">
                        <a href="#home" class="nav-link text-gray-900 px-3 py-2 text-sm font-medium active-nav">Home</a>
                        <a href="#about" class="nav-link text-gray-900 px-3 py-2 text-sm font-medium">About</a>
                        <a href="#skills" class="nav-link text-gray-900 px-3 py-2 text-sm font-medium">Skills</a>
                        <a href="#projects" class="nav-link text-gray-900 px-3 py-2 text-sm font-medium">Projects</a>
                        <a href="#experience" class="nav-link text-gray-900 px-3 py-2 text-sm font-medium">Experience</a>
                        <a href="#contact" class="nav-link text-gray-900 px-3 py-2 text-sm font-medium">Contact</a>
                    </div>
                </div>
                <div class="md:hidden">
                    <button id="mobile-menu-button" class="text-gray-500 hover:text-gray-900 focus:outline-none">
                        <i class="fas fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>
        
        <!-- Mobile menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white shadow-lg">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
                <a href="#home" class="block px-3 py-2 text-base font-medium text-gray-900 hover:bg-gray-100 rounded-md">Home</a>
                <a href="#about" class="block px-3 py-2 text-base font-medium text-gray-900 hover:bg-gray-100 rounded-md">About</a>
                <a href="#skills" class="block px-3 py-2 text-base font-medium text-gray-900 hover:bg-gray-100 rounded-md">Skills</a>
                <a href="#projects" class="block px-3 py-2 text-base font-medium text-gray-900 hover:bg-gray-100 rounded-md">Projects</a>
                <a href="#experience" class="block px-3 py-2 text-base font-medium text-gray-900 hover:bg-gray-100 rounded-md">Experience</a>
                <a href="#contact" class="block px-3 py-2 text-base font-medium text-gray-900 hover:bg-gray-100 rounded-md">Contact</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="pt-24 pb-16 md:pt-32 md:pb-24 bg-gradient-to-br from-blue-50 to-purple-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-10 md:mb-0">
                    <h1 class="text-4xl md:text-6xl font-bold mb-4">Hi, I'm <span class="gradient-text">Alex Carter</span></h1>
                    <h2 class="text-2xl md:text-3xl font-semibold text-gray-700 mb-6">Software Developer</h2>
                    <p class="text-lg text-gray-600 mb-8 max-w-lg">
                        Passionate about building elegant solutions to complex problems. Currently focused on full-stack development with modern technologies.
                    </p>
                    <div class="flex space-x-4">
                        <a href="#contact" class="px-6 py-3 bg-gradient-to-r from-blue-500 to-purple-600 text-white font-medium rounded-lg shadow-md hover:shadow-lg transition duration-300">
                            Contact Me
                        </a>
                        <a href="#projects" class="px-6 py-3 border border-gray-300 text-gray-700 font-medium rounded-lg hover:bg-gray-100 transition duration-300">
                            View Work
                        </a>
                    </div>
                </div>
                <div class="md:w-1/2 flex justify-center">
                    <div class="relative">
                        <div class="w-64 h-64 md:w-80 md:h-80 rounded-full bg-gradient-to-r from-blue-100 to-purple-100 flex items-center justify-center floating">
                            <img src="https://images.unsplash.com/photo-1573496359142-b8d87734a5cd?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=688&q=80" 
                                 alt="Profile" 
                                 class="w-60 h-60 md:w-72 md:h-72 rounded-full object-cover border-4 border-white shadow-lg">
                        </div>
                        <div class="absolute -bottom-5 -right-5 bg-white p-3 rounded-full shadow-lg">
                            <div class="w-12 h-12 bg-gradient-to-r from-blue-500 to-purple-600 rounded-full flex items-center justify-center">
                                <i class="fas fa-code text-white text-xl"></i>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-16 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-900 mb-2">About <span class="gradient-text">Me</span></h2>
                <div class="w-20 h-1 bg-gradient-to-r from-blue-500 to-purple-600 mx-auto"></div>
            </div>
            
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/3 mb-10 md:mb-0 flex justify-center">
                    <div class="relative">
                        <div class="w-64 h-64 rounded-xl bg-gradient-to-r from-blue-100 to-purple-100 flex items-center justify-center">
                            <img src="https://images.unsplash.com/photo-1573496359142-b8d87734a5cd?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=688&q=80" 
                                 alt="Profile" 
                                 class="w-60 h-60 rounded-xl object-cover border-4 border-white shadow-lg">
                        </div>
                    </div>
                </div>
                <div class="md:w-2/3 md:pl-12">
                    <h3 class="text-2xl font-semibold text-gray-800 mb-4">Who am I?</h3>
                    <p class="text-gray-600 mb-6">
                        I'm a passionate software developer with a Bachelor's degree in Computer Science from Stanford University. 
                        I specialize in building scalable web applications using modern JavaScript frameworks and cloud technologies.
                    </p>
                    <p class="text-gray-600 mb-6">
                        My journey in tech began when I built my first website at 14, and since then I've been obsessed with creating 
                        digital experiences that solve real-world problems. I'm particularly interested in the intersection of 
                        design and engineering, where beautiful interfaces meet robust systems.
                    </p>
                    <p class="text-gray-600 mb-8">
                        When I'm not coding, you can find me hiking, reading sci-fi novels, or contributing to open-source projects. 
                        I'm always eager to learn new technologies and collaborate on exciting projects.
                    </p>
                    <div class="flex flex-wrap gap-4">
                        <div class="flex items-center">
                            <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center mr-3">
                                <i class="fas fa-graduation-cap text-blue-600"></i>
                            </div>
                            <div>
                                <p class="font-semibold">Education</p>
                                <p class="text-sm text-gray-500">B.Sc. Computer Science</p>
                            </div>
                        </div>
                        <div class="flex items-center">
                            <div class="w-12 h-12 bg-purple-100 rounded-full flex items-center justify-center mr-3">
                                <i class="fas fa-briefcase text-purple-600"></i>
                            </div>
                            <div>
                                <p class="font-semibold">Experience</p>
                                <p class="text-sm text-gray-500">2+ Years</p>
                            </div>
                        </div>
                        <div class="flex items-center">
                            <div class="w-12 h-12 bg-indigo-100 rounded-full flex items-center justify-center mr-3">
                                <i class="fas fa-project-diagram text-indigo-600"></i>
                            </div>
                            <div>
                                <p class="font-semibold">Projects</p>
                                <p class="text-sm text-gray-500">15+ Completed</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-16 bg-gray-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-900 mb-2">My <span class="gradient-text">Skills</span></h2>
                <div class="w-20 h-1 bg-gradient-to-r from-blue-500 to-purple-600 mx-auto"></div>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Frontend Skills -->
                <div class="bg-white p-6 rounded-xl shadow-md card-hover">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mr-4">
                            <i class="fas fa-laptop-code text-blue-600 text-xl"></i>
                        </div>
                        <h3 class="text-xl font-semibold">Frontend Development</h3>
                    </div>
                    <p class="text-gray-600 mb-4">
                        Building responsive and interactive user interfaces with modern frameworks and best practices.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="skill-pill px-3 py-1 bg-blue-100 text-blue-800 rounded-full text-sm">React</span>
                        <span class="skill-pill px-3 py-1 bg-blue-100 text-blue-800 rounded-full text-sm">Next.js</span>
                        <span class="skill-pill px-3 py-1 bg-blue-100 text-blue-800 rounded-full text-sm">TypeScript</span>
                        <span class="skill-pill px-3 py-1 bg-blue-100 text-blue-800 rounded-full text-sm">Tailwind CSS</span>
                        <span class="skill-pill px-3 py-1 bg-blue-100 text-blue-800 rounded-full text-sm">Redux</span>
                        <span class="skill-pill px-3 py-1 bg-blue-100 text-blue-800 rounded-full text-sm">GraphQL</span>
                    </div>
                </div>
                
                <!-- Backend Skills -->
                <div class="bg-white p-6 rounded-xl shadow-md card-hover">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 bg-purple-100 rounded-lg flex items-center justify-center mr-4">
                            <i class="fas fa-server text-purple-600 text-xl"></i>
                        </div>
                        <h3 class="text-xl font-semibold">Backend Development</h3>
                    </div>
                    <p class="text-gray-600 mb-4">
                        Creating robust APIs and server-side applications with scalable architecture.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="skill-pill px-3 py-1 bg-purple-100 text-purple-800 rounded-full text-sm">Node.js</span>
                        <span class="skill-pill px-3 py-1 bg-purple-100 text-purple-800 rounded-full text-sm">Express</span>
                        <span class="skill-pill px-3 py-1 bg-purple-100 text-purple-800 rounded-full text-sm">Python</span>
                        <span class="skill-pill px-3 py-1 bg-purple-100 text-purple-800 rounded-full text-sm">Django</span>
                        <span class="skill-pill px-3 py-1 bg-purple-100 text-purple-800 rounded-full text-sm">MongoDB</span>
                        <span class="skill-pill px-3 py-1 bg-purple-100 text-purple-800 rounded-full text-sm">PostgreSQL</span>
                    </div>
                </div>
                
                <!-- DevOps Skills -->
                <div class="bg-white p-6 rounded-xl shadow-md card-hover">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 bg-indigo-100 rounded-lg flex items-center justify-center mr-4">
                            <i class="fas fa-cloud text-indigo-600 text-xl"></i>
                        </div>
                        <h3 class="text-xl font-semibold">DevOps & Cloud</h3>
                    </div>
                    <p class="text-gray-600 mb-4">
                        Deploying and managing applications in cloud environments with CI/CD pipelines.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="skill-pill px-3 py-1 bg-indigo-100 text-indigo-800 rounded-full text-sm">AWS</span>
                        <span class="skill-pill px-3 py-1 bg-indigo-100 text-indigo-800 rounded-full text-sm">Docker</span>
                        <span class="skill-pill px-3 py-1 bg-indigo-100 text-indigo-800 rounded-full text-sm">Kubernetes</span>
                        <span class="skill-pill px-3 py-1 bg-indigo-100 text-indigo-800 rounded-full text-sm">GitHub Actions</span>
                        <span class="skill-pill px-3 py-1 bg-indigo-100 text-indigo-800 rounded-full text-sm">Terraform</span>
                        <span class="skill-pill px-3 py-1 bg-indigo-100 text-indigo-800 rounded-full text-sm">Serverless</span>
                    </div>
                </div>
            </div>
            
            <div class="mt-12">
                <h3 class="text-xl font-semibold text-center mb-6">Other Proficiencies</h3>
                <div class="flex flex-wrap justify-center gap-3">
                    <span class="skill-pill px-4 py-2 bg-gray-100 text-gray-800 rounded-full flex items-center">
                        <i class="fab fa-git-alt mr-2"></i> Git
                    </span>
                    <span class="skill-pill px-4 py-2 bg-gray-100 text-gray-800 rounded-full flex items-center">
                        <i class="fas fa-terminal mr-2"></i> Bash
                    </span>
                    <span class="skill-pill px-4 py-2 bg-gray-100 text-gray-800 rounded-full flex items-center">
                        <i class="fas fa-database mr-2"></i> SQL
                    </span>
                    <span class="skill-pill px-4 py-2 bg-gray-100 text-gray-800 rounded-full flex items-center">
                        <i class="fas fa-shield-alt mr-2"></i> OAuth
                    </span>
                    <span class="skill-pill px-4 py-2 bg-gray-100 text-gray-800 rounded-full flex items-center">
                        <i class="fas fa-mobile-alt mr-2"></i> Responsive Design
                    </span>
                    <span class="skill-pill px-4 py-2 bg-gray-100 text-gray-800 rounded-full flex items-center">
                        <i class="fas fa-bug mr-2"></i> Testing
                    </span>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-16 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-900 mb-2">Featured <span class="gradient-text">Projects</span></h2>
                <div class="w-20 h-1 bg-gradient-to-r from-blue-500 to-purple-600 mx-auto"></div>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Project 1 -->
                <div class="project-card h-80 rounded-xl overflow-hidden shadow-md">
                    <div class="project-inner relative w-full h-full">
                        <div class="project-front absolute w-full h-full bg-gradient-to-br from-blue-50 to-purple-50 p-6 flex flex-col">
                            <div class="w-14 h-14 bg-white rounded-lg flex items-center justify-center shadow-sm mb-4">
                                <i class="fas fa-store text-blue-600 text-xl"></i>
                            </div>
                            <h3 class="text-xl font-semibold mb-2">E-Commerce Platform</h3>
                            <p class="text-gray-600 mb-4">Full-featured online store with payment integration and admin dashboard.</p>
                            <div class="mt-auto">
                                <div class="flex flex-wrap gap-2 mb-4">
                                    <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded-full text-xs">React</span>
                                    <span class="px-2 py-1 bg-purple-100 text-purple-800 rounded-full text-xs">Node.js</span>
                                    <span class="px-2 py-1 bg-green-100 text-green-800 rounded-full text-xs">MongoDB</span>
                                </div>
                                <button class="text-blue-600 font-medium text-sm flex items-center">
                                    View Details <i class="fas fa-arrow-right ml-2"></i>
                                </button>
                            </div>
                        </div>
                        <div class="project-back absolute w-full h-full bg-white p-6">
                            <h3 class="text-xl font-semibold mb-2">E-Commerce Platform</h3>
                            <ul class="text-gray-600 text-sm space-y-2 mb-4">
                                <li class="flex items-start">
                                    <i class="fas fa-check-circle text-green-500 mt-1 mr-2"></i>
                                    <span>Implemented Stripe payment processing with webhooks</span>
                                </li>
                                <li class="flex items-start">
                                    <i class="fas fa-check-circle text-green-500 mt-1 mr-2"></i>
                                    <span>Built custom CMS for product management</span>
                                </li>
                                <li class="flex items-start">
                                    <i class="fas fa-check-circle text-green-500 mt-1 mr-2"></i>
                                    <span>Optimized performance with lazy loading and caching</span>
                                </li>
                            </ul>
                            <div class="absolute bottom-6 left-6 right-6">
                                <div class="flex space-x-3">
                                    <a href="#" class="px-4 py-2 bg-blue-600 text-white rounded-lg text-sm font-medium">Live Demo</a>
                                    <a href="#" class="px-4 py-2 border border-gray-300 rounded-lg text-sm font-medium">Code</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Project 2 -->
                <div class="project-card h-80 rounded-xl overflow-hidden shadow-md">
                    <div class="project-inner relative w-full h-full">
                        <div class="project-front absolute w-full h-full bg-gradient-to-br from-green-50 to-blue-50 p-6 flex flex-col">
                            <div class="w-14 h-14 bg-white rounded-lg flex items-center justify-center shadow-sm mb-4">
                                <i class="fas fa-chart-line text-green-600 text-xl"></i>
                            </div>
                            <h3 class="text-xl font-semibold mb-2">Data Visualization Dashboard</h3>
                            <p class="text-gray-600 mb-4">Interactive dashboard for analyzing large datasets with custom visualizations.</p>
                            <div class="mt-auto">
                                <div class="flex flex-wrap gap-2 mb-4">
                                    <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded-full text-xs">D3.js</span>
                                    <span class="px-2 py-1 bg-purple-100 text-purple-800 rounded-full text-xs">Python</span>
                                    <span class="px-2 py-1 bg-red-100 text-red-800 rounded-full text-xs">Flask</span>
                                </div>
                                <button class="text-green-600 font-medium text-sm flex items-center">
                                    View Details <i class="fas fa-arrow-right ml-2"></i>
                                </button>
                            </div>
                        </div>
                        <div class="project-back absolute w-full h-full bg-white p-6">
                            <h3 class="text-xl font-semibold mb-2">Data Visualization Dashboard</h3>
                            <ul class="text-gray-600 text-sm space-y-2 mb-4">
                                <li class="flex items-start">
                                    <i class="fas fa-check-circle text-green-500 mt-1 mr-2"></i>
                                    <span>Created custom D3.js visualizations for complex data</span>
                                </li>
                                <li class="flex items-start">
                                    <i class="fas fa-check-circle text-green-500 mt-1 mr-2"></i>
                                    <span>Implemented real-time data streaming with WebSockets</span>
                                </li>
                                <li class="flex items-start">
                                    <i class="fas fa-check-circle text-green-500 mt-1 mr-2"></i>
                                    <span>Designed responsive layout for all device sizes</span>
                                </li>
                            </ul>
                            <div class="absolute bottom-6 left-6 right-6">
                                <div class="flex space-x-3">
                                    <a href="#" class="px-4 py-2 bg-green-600 text-white rounded-lg text-sm font-medium">Live Demo</a>
                                    <a href="#" class="px-4 py-2 border border-gray-300 rounded-lg text-sm font-medium">Code</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Project 3 -->
                <div class="project-card h-80 rounded-xl overflow-hidden shadow-md">
                    <div class="project-inner relative w-full h-full">
                        <div class="project-front absolute w-full h-full bg-gradient-to-br from-purple-50 to-pink-50 p-6 flex flex-col">
                            <div class="w-14 h-14 bg-white rounded-lg flex items-center justify-center shadow-sm mb-4">
                                <i class="fas fa-robot text-purple-600 text-xl"></i>
                            </div>
                            <h3 class="text-xl font-semibold mb-2">AI Chatbot</h3>
                            <p class="text-gray-600 mb-4">Conversational AI assistant with natural language processing capabilities.</p>
                            <div class="mt-auto">
                                <div class="flex flex-wrap gap-2 mb-4">
                                    <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded-full text-xs">Python</span>
                                    <span class="px-2 py-1 bg-yellow-100 text-yellow-800 rounded-full text-xs">TensorFlow</span>
                                    <span class="px-2 py-1 bg-red-100 text-red-800 rounded-full text-xs">NLTK</span>
                                </div>
                                <button class="text-purple-600 font-medium text-sm flex items-center">
                                    View Details <i class="fas fa-arrow-right ml-2"></i>
                                </button>
                            </div>
                        </div>
                        <div class="project-back absolute w-full h-full bg-white p-6">
                            <h3 class="text-xl font-semibold mb-2">AI Chatbot</h3>
                            <ul class="text-gray-600 text-sm space-y-2 mb-4">
                                <li class="flex items-start">
                                    <i class="fas fa-check-circle text-green-500 mt-1 mr-2"></i>
                                    <span>Trained custom NLP model on domain-specific data</span>
                                </li>
                                <li class="flex items-start">
                                    <i class="fas fa-check-circle text-green-500 mt-1 mr-2"></i>
                                    <span>Integrated with multiple messaging platforms</span>
                                </li>
                                <li class="flex items-start">
                                    <i class="fas fa-check-circle text-green-500 mt-1 mr-2"></i>
                                    <span>Implemented sentiment analysis for better responses</span>
                                </li>
                            </ul>
                            <div class="absolute bottom-6 left-6 right-6">
                                <div class="flex space-x-3">
                                    <a href="#" class="px-4 py-2 bg-purple-600 text-white rounded-lg text-sm font-medium">Live Demo</a>
                                    <a href="#" class="px-4 py-2 border border-gray-300 rounded-lg text-sm font-medium">Code</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="mt-12 text-center">
                <a href="#" class="inline-flex items-center px-6 py-3 border border-gray-300 text-gray-700 font-medium rounded-lg hover:bg-gray-50 transition duration-300">
                    <i class="fab fa-github mr-2"></i> View All Projects on GitHub
                </a>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="py-16 bg-gray-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-900 mb-2">Work <span class="gradient-text">Experience</span></h2>
                <div class="w-20 h-1 bg-gradient-to-r from-blue-500 to-purple-600 mx-auto"></div>
            </div>
            
            <div class="relative">
                <!-- Timeline -->
                <div class="border-l-2 border-gray-200 absolute h-full top-0 left-8 md:left-1/2"></div>
                
                <!-- Experience 1 -->
                <div class="mb-12">
                    <div class="flex flex-col md:flex-row justify-center">
                        <div class="md:w-5/12 md:text-right pr-8 mb-4 md:mb-0">
                            <h3 class="text-xl font-semibold">Software Engineer Intern</h3>
                            <p class="text-blue-600">Google</p>
                            <p class="text-gray-500 text-sm">Summer 2023</p>
                        </div>
                        <div class="hidden md:block md:w-2/12 flex justify-center">
                            <div class="w-6 h-6 bg-gradient-to-r from-blue-500 to-purple-600 rounded-full"></div>
                        </div>
                        <div class="md:w-5/12 pl-8">
                            <div class="bg-white p-6 rounded-lg shadow-sm">
                                <ul class="list-disc pl-5 space-y-2 text-gray-600">
                                    <li>Worked on the Google Cloud Platform team to optimize container orchestration</li>
                                    <li>Developed features for Kubernetes engine to improve deployment times by 15%</li>
                                    <li>Implemented monitoring solutions using Stackdriver and Prometheus</li>
                                    <li>Collaborated with senior engineers on design and code reviews</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Experience 2 -->
                <div class="mb-12">
                    <div class="flex flex-col md:flex-row justify-center">
                        <div class="md:w-5/12 md:order-last md:text-left pl-8 mb-4 md:mb-0">
                            <h3 class="text-xl font-semibold">Full Stack Developer</h3>
                            <p class="text-purple-600">TechStart Inc.</p>
                            <p class="text-gray-500 text-sm">Jan 2022 - Present</p>
                        </div>
                        <div class="hidden md:block md:w-2/12 flex justify-center">
                            <div class="w-6 h-6 bg-gradient-to-r from-blue-500 to-purple-600 rounded-full"></div>
                        </div>
                        <div class="md:w-5/12 md:order-first md:text-right pr-8">
                            <div class="bg-white p-6 rounded-lg shadow-sm">
                                <ul class="list-disc pl-5 space-y-2 text-gray-600">
                                    <li>Led development of customer portal using React and Node.js</li>
                                    <li>Reduced API response times by 40% through query optimization</li>
                                    <li>Implemented CI/CD pipeline reducing deployment time from 30min to 5min</li>
                                    <li>Mentored junior developers in code best practices</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Experience 3 -->
                <div class="mb-12">
                    <div class="flex flex-col md:flex-row justify-center">
                        <div class="md:w-5/12 md:text-right pr-8 mb-4 md:mb-0">
                            <h3 class="text-xl font-semibold">Web Developer</h3>
                            <p class="text-indigo-600">Freelance</p>
                            <p class="text-gray-500 text-sm">2019 - 2021</p>
                        </div>
                        <div class="hidden md:block md:w-2/12 flex justify-center">
                            <div class="w-6 h-6 bg-gradient-to-r from-blue-500 to-purple-600 rounded-full"></div>
                        </div>
                        <div class="md:w-5/12 pl-8">
                            <div class="bg-white p-6 rounded-lg shadow-sm">
                                <ul class="list-disc pl-5 space-y-2 text-gray-600">
                                    <li>Built custom websites for 20+ clients across various industries</li>
                                    <li>Specialized in WordPress customization and e-commerce solutions</li>
                                    <li>Improved client SEO rankings through technical optimizations</li>
                                    <li>Managed all aspects from design to deployment</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-12">
                <a href="#" class="inline-flex items-center px-6 py-3 border border-gray-300 text-gray-700 font-medium rounded-lg hover:bg-gray-50 transition duration-300">
                    <i class="fas fa-file-pdf mr-2"></i> Download Full Resume
                </a>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-16 bg-gradient-to-br from-blue-50 to-purple-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-900 mb-2">Get In <span class="gradient-text">Touch</span></h2>
                <div class="w-20 h-1 bg-gradient-to-r from-blue-500 to-purple-600 mx-auto"></div>
            </div>
            
            <div class="flex flex-col md:flex-row">
                <div class="md:w-1/2 mb-10 md:mb-0 md:pr-8">
                    <h3 class="text-2xl font-semibold mb-4">Let's talk about your project</h3>
                    <p class="text-gray-600 mb-8">
                        I'm currently looking for new opportunities in software development. Whether you have a question or just want to say hi, I'll try my best to get back to you!
                    </p>
                    
                    <div class="space-y-4">
                        <div class="flex items-center">
                            <div class="w-12 h-12 bg-white rounded-full flex items-center justify-center shadow-sm mr-4">
                                <i class="fas fa-envelope text-blue-600"></i>
                            </div>
                            <div>
                                <p class="font-medium">Email Me</p>
                                <a href="mailto:alex@example.com" class="text-gray-600 hover:text-blue-600">alex@example.com</a>
                            </div>
                        </div>
                        <div class="flex items-center">
                            <div class="w-12 h-12 bg-white rounded-full flex items-center justify-center shadow-sm mr-4">
                                <i class="fas fa-phone-alt text-purple-600"></i>
                            </div>
                            <div>
                                <p class="font-medium">Call Me</p>
                                <a href="tel:+1234567890" class="text-gray-600 hover:text-purple-600">+1 (234) 567-890</a>
                            </div>
                        </div>
                        <div class="flex items-center">
                            <div class="w-12 h-12 bg-white rounded-full flex items-center justify-center shadow-sm mr-4">
                                <i class="fas fa-map-marker-alt text-indigo-600"></i>
                            </div>
                            <div>
                                <p class="font-medium">Location</p>
                                <p class="text-gray-600">San Francisco, CA</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="mt-8">
                        <h4 class="font-medium mb-4">Connect with me</h4>
                        <div class="flex space-x-4">
                            <a href="#" class="w-10 h-10 bg-white rounded-full flex items-center justify-center shadow-sm hover:bg-blue-100">
                                <i class="fab fa-linkedin-in text-blue-600"></i>
                            </a>
                            <a href="#" class="w-10 h-10 bg-white rounded-full flex items-center justify-center shadow-sm hover:bg-gray-100">
                                <i class="fab fa-github text-gray-800"></i>
                            </a>
                            <a href="#" class="w-10 h-10 bg-white rounded-full flex items-center justify-center shadow-sm hover:bg-blue-100">
                                <i class="fab fa-twitter text-blue-400"></i>
                            </a>
                            <a href="#" class="w-10 h-10 bg-white rounded-full flex items-center justify-center shadow-sm hover:bg-red-100">
                                <i class="fab fa-youtube text-red-600"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <div class="md:w-1/2">
                    <form class="bg-white p-8 rounded-xl shadow-md">
                        <div class="mb-6">
                            <label for="name" class="block text-gray-700 font-medium mb-2">Your Name</label>
                            <input type="text" id="name" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
                        </div>
                        <div class="mb-6">
                            <label for="email" class="block text-gray-700 font-medium mb-2">Email Address</label>
                            <input type="email" id="email" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
                        </div>
                        <div class="mb-6">
                            <label for="subject" class="block text-gray-700 font-medium mb-2">Subject</label>
                            <input type="text" id="subject" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
                        </div>
                        <div class="mb-6">
                            <label for="message" class="block text-gray-700 font-medium mb-2">Message</label>
                            <textarea id="message" rows="4" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500"></textarea>
                        </div>
                        <button type="submit" class="w-full bg-gradient-to-r from-blue-500 to-purple-600 text-white py-3 rounded-lg font-medium hover:shadow-lg transition duration-300">
                            Send Message
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-4 md:mb-0">
                    <span class="text-xl font-bold gradient-text">Alex Carter</span>
                    <p class="text-gray-400 mt-2">Building digital experiences that matter.</p>
                </div>
                <div class="flex space-x-6">
                    <a href="#" class="text-gray-400 hover:text-white">
                        <i class="fab fa-linkedin-in"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-white">
                        <i class="fab fa-github"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-white">
                        <i class="fab fa-twitter"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-white">
                        <i class="fab fa-instagram"></i>
                    </a>
                </div>
            </div>
            <div class="mt-8 pt-8 border-t border-gray-800 text-center text-gray-400 text-sm">
                <p>&copy; 2023 Alex Carter. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        document.getElementById('mobile-menu-button').addEventListener('click', function() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                // Close mobile menu if open
                document.getElementById('mobile-menu').classList.add('hidden');
                
                // Scroll to target
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Update active nav link
                    document.querySelectorAll('.nav-link').forEach(link => {
                        link.classList.remove('active-nav');
                    });
                    this.classList.add('active-nav');
                }
            });
        });

        // Update active nav link on scroll
        window.addEventListener('scroll', function() {
            const scrollPosition = window.scrollY + 100;
            
            document.querySelectorAll('section').forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.offsetHeight;
                const sectionId = section.getAttribute('id');
                
                if (scrollPosition >= sectionTop && scrollPosition < sectionTop + sectionHeight) {
                    document.querySelectorAll('.nav-link').forEach(link => {
                        link.classList.remove('active-nav');
                        if (link.getAttribute('href') === `#${sectionId}`) {
                            link.classList.add('active-nav');
                        }
                    });
                }
            });
        });

        // Project card flip on click for mobile
        document.querySelectorAll('.project-card').forEach(card => {
            card.addEventListener('click', function() {
                if (window.innerWidth < 768) { // Only for mobile
                    const inner = this.querySelector('.project-inner');
                    const currentTransform = window.getComputedStyle(inner).getPropertyValue('transform');
                    
                    if (currentTransform === 'none' || currentTransform === 'matrix(1, 0, 0, 1, 0, 0)') {
                        inner.style.transform = 'rotateY(180deg)';
                    } else {
                        inner.style.transform = 'rotateY(0deg)';
                    }
                }
            });
        });

        // Form submission
        const contactForm = document.querySelector('form');
        if (contactForm) {
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                // Get form values
                const name = document.getElementById('name').value;
                const email = document.getElementById('email').value;
                const subject = document.getElementById('subject').value;
                const message = document.getElementById('message').value;
                
                // Here you would typically send the data to a server
                console.log('Form submitted:', { name, email, subject, message });
                
                // Show success message
                alert('Thank you for your message! I will get back to you soon.');
                contactForm.reset();
            });
        }
    </script>
</body>
</html>

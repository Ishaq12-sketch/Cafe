<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Cozy Corner Cafe</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts - Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* Custom Tailwind Colors */
        :root {
            --color-mint: #E0F2F7; /* Light Mint */
            --color-peach: #FFDAB9; /* Light Peach */
            --color-dark-mint: #4ECDC4; /* Accent Mint */
            --color-dark-peach: #FF6B6B; /* Accent Peach */
            --color-text-dark: #333333; /* Dark text for contrast */
        }

        .bg-mint { background-color: var(--color-mint); }
        .bg-peach { background-color: var(--color-peach); }
        .bg-dark-mint { background-color: var(--color-dark-mint); }
        .bg-dark-peach { background-color: var(--color-dark-peach); }
        .text-dark-text { color: var(--color-text-dark); }
        .text-dark-mint { color: var(--color-dark-mint); }
        .text-dark-peach { color: var(--color-dark-peach); }

        body {
            font-family: 'Inter', sans-serif;
            color: var(--color-text-dark);
        }

        /* Custom scrollbar for better aesthetics */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: var(--color-mint);
            border-radius: 10px;
        }
        ::-webkit-scrollbar-thumb {
            background: var(--color-dark-mint);
            border-radius: 10px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: var(--color-dark-peach);
        }

        /* Smooth scroll behavior */
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white">

    <!-- Header & Navigation -->
    <header class="bg-mint shadow-md py-4 sticky top-0 z-50">
        <nav class="container mx-auto px-4 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold text-dark-mint rounded-md p-2 hover:text-dark-peach transition-colors duration-300">The Cozy Corner Cafe</a>
            
            <!-- Mobile Menu Button -->
            <div class="md:hidden">
                <button id="mobile-menu-button" class="text-dark-mint focus:outline-none">
                    <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                    </svg>
                </button>
            </div>

            <!-- Desktop Navigation -->
            <ul id="main-nav" class="hidden md:flex space-x-6">
                <li><a href="#home" class="text-dark-text hover:text-dark-peach font-medium transition-colors duration-300 p-2 rounded-md">Home</a></li>
                <li><a href="#menu" class="text-dark-text hover:text-dark-peach font-medium transition-colors duration-300 p-2 rounded-md">Menu</a></li>
                <li><a href="#about" class="text-dark-text hover:text-dark-peach font-medium transition-colors duration-300 p-2 rounded-md">About Us</a></li>
                <li><a href="#contact" class="text-dark-text hover:text-dark-peach font-medium transition-colors duration-300 p-2 rounded-md">Contact</a></li>
            </ul>
        </nav>

        <!-- Mobile Menu (hidden by default) -->
        <div id="mobile-menu" class="hidden md:hidden bg-mint pt-2 pb-4">
            <ul class="flex flex-col items-center space-y-3">
                <li><a href="#home" class="block text-dark-text hover:text-dark-peach font-medium transition-colors duration-300 p-2 rounded-md w-full text-center">Home</a></li>
                <li><a href="#menu" class="block text-dark-text hover:text-dark-peach font-medium transition-colors duration-300 p-2 rounded-md w-full text-center">Menu</a></li>
                <li><a href="#about" class="block text-dark-text hover:text-dark-peach font-medium transition-colors duration-300 p-2 rounded-md w-full text-center">About Us</a></li>
                <li><a href="#contact" class="block text-dark-text hover:text-dark-peach font-medium transition-colors duration-300 p-2 rounded-md w-full text-center">Contact</a></li>
            </ul>
        </div>
    </header>

    <main>
        <!-- Hero Section -->
        <section id="home" class="relative bg-peach text-dark-text py-20 md:py-32 flex items-center justify-center overflow-hidden min-h-screen">
            <!-- Background image with overlay -->
            <img src="https://placehold.co/1920x1080/FFDAB9/333333?text=Cafe+Interior" alt="Cozy Cafe Interior" class="absolute inset-0 w-full h-full object-cover opacity-60">
            <div class="absolute inset-0 bg-gradient-to-t from-peach to-transparent opacity-80"></div>

            <div class="container mx-auto px-4 text-center relative z-10">
                <h1 class="text-4xl md:text-6xl font-extrabold mb-6 leading-tight text-dark-text drop-shadow-lg">
                    Sip, Relax, Indulge
                </h1>
                <p class="text-lg md:text-xl mb-8 max-w-2xl mx-auto drop-shadow-md">
                    Discover your new favorite spot for artisanal coffee, delightful pastries, and heartwarming moments.
                </p>
                <a href="#menu" class="bg-dark-mint text-white px-8 py-4 rounded-full text-lg font-semibold hover:bg-dark-peach transition-all duration-300 shadow-lg transform hover:scale-105">
                    Explore Our Menu
                </a>
            </div>
        </section>

        <!-- Menu Section -->
        <section id="menu" class="bg-mint py-16 md:py-24">
            <div class="container mx-auto px-4">
                <h2 class="text-4xl font-bold text-center mb-12 text-dark-mint">Our Delicious Offerings</h2>
                
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Coffee & Drinks -->
                    <div class="bg-white p-6 rounded-xl shadow-lg transform hover:scale-105 transition-transform duration-300">
                        <h3 class="text-2xl font-semibold mb-4 text-dark-peach">Coffee & Drinks</h3>
                        <ul class="space-y-3">
                            <li class="flex justify-between items-center border-b border-gray-200 pb-2">
                                <span>Espresso</span><span class="font-medium text-dark-mint">£3.00</span>
                            </li>
                            <li class="flex justify-between items-center border-b border-gray-200 pb-2">
                                <span>Latte</span><span class="font-medium text-dark-mint">£4.50</span>
                            </li>
                            <li class="flex justify-between items-center border-b border-gray-200 pb-2">
                                <span>Cappuccino</span><span class="font-medium text-dark-mint">£4.50</span>
                            </li>
                            <li class="flex justify-between items-center border-b border-gray-200 pb-2">
                                <span>Iced Peach Tea</span><span class="font-medium text-dark-mint">£4.00</span>
                            </li>
                            <li class="flex justify-between items-center">
                                <span>Mint Lemonade</span><span class="font-medium text-dark-mint">£4.25</span>
                            </li>
                        </ul>
                    </div>

                    <!-- Pastries & Sweets -->
                    <div class="bg-white p-6 rounded-xl shadow-lg transform hover:scale-105 transition-transform duration-300">
                        <h3 class="text-2xl font-semibold mb-4 text-dark-peach">Pastries & Sweets</h3>
                        <ul class="space-y-3">
                            <li class="flex justify-between items-center border-b border-gray-200 pb-2">
                                <span>Croissant</span><span class="font-medium text-dark-mint">£3.50</span>
                            </li>
                            <li class="flex justify-between items-center border-b border-gray-200 pb-2">
                                <span>Blueberry Muffin</span><span class="font-medium text-dark-mint">£3.75</span>
                            </li>
                            <li class="flex justify-between items-center border-b border-gray-200 pb-2">
                                <span>Chocolate Chip Cookie</span><span class="font-medium text-dark-mint">£2.50</span>
                            </li>
                            <li class="flex justify-between items-center border-b border-gray-200 pb-2">
                                <span>Peach Danish</span><span class="font-medium text-dark-mint">£4.00</span>
                            </li>
                            <li class="flex justify-between items-center">
                                <span>Mint Chocolate Brownie</span><span class="font-medium text-dark-mint">£4.25</span>
                            </li>
                        </ul>
                    </div>

                    <!-- Light Bites -->
                    <div class="bg-white p-6 rounded-xl shadow-lg transform hover:scale-105 transition-transform duration-300">
                        <h3 class="text-2xl font-semibold mb-4 text-dark-peach">Light Bites</h3>
                        <ul class="space-y-3">
                            <li class="flex justify-between items-center border-b border-gray-200 pb-2">
                                <span>Avocado Toast</span><span class="font-medium text-dark-mint">£7.00</span>
                            </li>
                            <li class="flex justify-between items-center border-b border-gray-200 pb-2">
                                <span>Yogurt Parfait</span><span class="font-medium text-dark-mint">£6.50</span>
                            </li>
                            <li class="flex justify-between items-center">
                                <span>Seasonal Fruit Bowl</span><span class="font-medium text-dark-mint">£5.50</span>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <!-- About Us Section -->
        <section id="about" class="bg-peach py-16 md:py-24">
            <div class="container mx-auto px-4 flex flex-col md:flex-row items-center gap-12">
                <div class="md:w-1/2">
                    <img src="https://placehold.co/600x400/E0F2F7/333333?text=Smiling+Barista" alt="Smiling Barista" class="rounded-xl shadow-lg w-full h-auto object-cover">
                </div>
                <div class="md:w-1/2 text-dark-text">
                    <h2 class="text-4xl font-bold mb-6 text-dark-mint">Our Story</h2>
                    <p class="text-lg leading-relaxed mb-4">
                        Welcome to The Cozy Corner Cafe, where every cup tells a story. Founded with a passion for exceptional coffee and a love for community, we've created a space where you can unwind, connect, and savor life's simple pleasures.
                    </p>
                    <p class="text-lg leading-relaxed">
                        We source the finest beans, bake our pastries fresh daily, and craft each drink with care. Our mission is to provide not just great food and coffee, but a warm, inviting atmosphere that feels like home. Come experience the difference!
                    </p>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="bg-mint py-16 md:py-24">
            <div class="container mx-auto px-4">
                <h2 class="text-4xl font-bold text-center mb-12 text-dark-peach">Get In Touch</h2>
                
                <div class="flex flex-col md:flex-row gap-12 items-center">
                    <div class="md:w-1/2 bg-white p-8 rounded-xl shadow-lg w-full">
                        <h3 class="text-2xl font-semibold mb-6 text-dark-mint">Send Us a Message</h3>
                        <form class="space-y-4">
                            <div>
                                <label for="name" class="block text-dark-text text-sm font-medium mb-2">Name</label>
                                <input type="text" id="name" name="name" class="w-full p-3 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-dark-mint">
                            </div>
                            <div>
                                <label for="email" class="block text-dark-text text-sm font-medium mb-2">Email</label>
                                <input type="email" id="email" name="email" class="w-full p-3 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-dark-mint">
                            </div>
                            <div>
                                <label for="message" class="block text-dark-text text-sm font-medium mb-2">Message</label>
                                <textarea id="message" name="message" rows="5" class="w-full p-3 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-dark-mint"></textarea>
                            </div>
                            <button type="submit" class="w-full bg-dark-peach text-white px-6 py-3 rounded-md text-lg font-semibold hover:bg-dark-mint transition-colors duration-300 shadow-md transform hover:scale-105">
                                Send Message
                            </button>
                        </form>
                    </div>

                    <div class="md:w-1/2 text-dark-text bg-white p-8 rounded-xl shadow-lg w-full">
                        <h3 class="text-2xl font-semibold mb-6 text-dark-mint">Visit Us</h3>
                        <p class="mb-4 text-lg">
                            <strong class="text-dark-peach">Address:</strong> 123 Cafe Lane, Cozy Town, CA 90210
                        </p>
                        <p class="mb-4 text-lg">
                            <strong class="text-dark-peach">Phone:</strong> (123) 456-7890
                        </p>
                        <p class="mb-4 text-lg">
                            <strong class="text-dark-peach">Email:</strong> info@cozycornercafe.com
                        </p>
                        <p class="mb-6 text-lg">
                            <strong class="text-dark-peach">Hours:</strong><br>
                            Mon - Fri: 7:00 AM - 6:00 PM<br>
                            Sat - Sun: 8:00 AM - 5:00 PM
                        </p>
                        <!-- Placeholder for a map -->
                        <div class="w-full h-64 bg-gray-200 rounded-md flex items-center justify-center text-gray-500">
                            <p>Map Placeholder</p>
                            <!-- In a real app, you'd embed Google Maps here -->
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-dark-mint text-white py-8">
        <div class="container mx-auto px-4 text-center">
            <p>&copy; 2025 The Cozy Corner Cafe. All rights reserved.</p>
            <div class="flex justify-center space-x-4 mt-4">
                <a href="#" class="hover:text-peach transition-colors duration-300">Privacy Policy</a>
                <a href="#" class="hover:text-peach transition-colors duration-300">Terms of Service</a>
            </div>
        </div>
    </footer>

    <!-- JavaScript for Mobile Menu Toggle -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuButton = document.getElementById('mobile-menu-button');
            const mobileMenu = document.getElementById('mobile-menu');
            const navLinks = document.querySelectorAll('#main-nav a, #mobile-menu a');

            // Toggle mobile menu visibility
            mobileMenuButton.addEventListener('click', function() {
                mobileMenu.classList.toggle('hidden');
            });

            // Close mobile menu when a link is clicked (for smooth scrolling)
            navLinks.forEach(link => {
                link.addEventListener('click', function(event) {
                    // Only prevent default if it's an internal anchor link
                    if (this.hash !== "") {
                        event.preventDefault();
                        const targetId = this.hash;
                        const targetElement = document.querySelector(targetId);

                        if (targetElement) {
                            window.scrollTo({
                                top: targetElement.offsetTop - document.querySelector('header').offsetHeight, // Adjust for fixed header
                                behavior: 'smooth'
                            });
                        }
                        // Hide mobile menu after clicking a link
                        if (!mobileMenu.classList.contains('hidden')) {
                            mobileMenu.classList.add('hidden');
                        }
                    }
                });
            });
        });
    </script>
</body>
</html>

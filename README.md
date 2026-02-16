<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Al Ghani Fragrances | Luxury Experience</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --royal-gold: #c5a059;
            --soft-gold: #e2c275;
            --deep-navy: #0f172a;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            background: radial-gradient(circle at top, #1e293b 0%, #020617 100%);
            color: #f8fafc;
            overflow-x: hidden;
        }

        .serif-font { font-family: 'Cinzel', serif; }

        .glass-card {
            background: rgba(255, 255, 255, 0.02);
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 255, 255, 0.08);
            transition: all 0.5s cubic-bezier(0.23, 1, 0.32, 1);
        }

        .glass-card:hover {
            background: rgba(255, 255, 255, 0.05);
            border-color: var(--royal-gold);
            transform: translateY(-8px);
        }

        .gold-gradient {
            background: linear-gradient(to right, #bf953f, #fcf6ba, #b38728, #fbf5b7, #aa771c);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .btn-gold {
            background: linear-gradient(135deg, #c5a059 0%, #927438 100%);
            color: #000;
            font-weight: 700;
            letter-spacing: 1px;
            transition: all 0.3s ease;
        }

        /* Sidebar / Hamburger Menu Styles - MOVED TO RIGHT */
        #sideMenu {
            transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            z-index: 100;
        }

        .menu-open { transform: translateX(0) !important; }

        /* FAQ Accordion */
        .faq-item input:checked ~ .faq-content { max-height: 200px; padding-top: 1rem; }
        .faq-content { max-height: 0; overflow: hidden; transition: all 0.3s ease; }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }
        .float-anim { animation: float 4s ease-in-out infinite; }

        .message-toast {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            background: #10b981;
            padding: 1rem 2rem;
            border-radius: 12px;
            display: none;
            z-index: 1000;
        }
    </style>
</head>
<body class="p-4 md:p-8">

    <!-- Hamburger Toggle Button - RIGHT SIDE -->
    <button onclick="toggleMenu()" class="fixed top-6 right-6 z-[110] glass-card p-3 rounded-full hover:border-yellow-500 transition-colors">
        <svg id="menuIcon" class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
        </svg>
    </button>

    <!-- Side Menu Overlay - RIGHT SIDE -->
    <div id="sideMenu" class="fixed top-0 right-0 h-full w-[300px] glass-card border-l border-white/10 p-8 translate-x-full shadow-2xl flex flex-col text-right">
        <div class="mb-12">
            <h2 class="serif-font gold-gradient text-2xl font-bold uppercase tracking-widest">Navigation</h2>
        </div>
        <nav class="flex flex-col gap-6 text-lg uppercase tracking-widest font-light">
            <a href="javascript:void(0)" onclick="handleNav('home')" class="hover:text-yellow-500 transition-colors">Home</a>
            <a href="javascript:void(0)" onclick="handleNav('collections')" class="hover:text-yellow-500 transition-colors">Collections</a>
            <a href="javascript:void(0)" onclick="handleNav('reviews')" class="hover:text-yellow-500 transition-colors">Reviews</a>
            <a href="javascript:void(0)" onclick="handleNav('faqs')" class="hover:text-yellow-500 transition-colors">FAQs</a>
            <a href="javascript:void(0)" onclick="handleNav('order')" class="hover:text-yellow-500 transition-colors">Order Now</a>
        </nav>
        <div class="mt-auto pt-8 border-t border-white/10">
            <p class="text-[10px] text-slate-500 uppercase tracking-widest">Al Ghani Luxury Brands</p>
        </div>
    </div>

    <div class="max-w-7xl mx-auto" id="home-top">
        
        <!-- Header -->
        <header class="text-center mb-16 pt-10">
            <div class="flex justify-center mb-6">
                <img src="https://i.postimg.cc/LqWtTMb1/Screenshot-2024-05-05-152628.png" alt="Al Ghani Logo" class="h-24 md:h-32 float-anim filter brightness-110">
            </div>
            <h1 class="serif-font text-5xl md:text-8xl font-bold gold-gradient tracking-tighter mb-4">Al Ghani</h1>
            <div class="flex items-center justify-center gap-4">
                <div class="h-px w-12 bg-gradient-to-r from-transparent to-yellow-600"></div>
                <p class="text-slate-400 tracking-[0.4em] text-[10px] md:text-sm uppercase font-medium">Pure Luxury Fragrances</p>
                <div class="h-px w-12 bg-gradient-to-l from-transparent to-yellow-600"></div>
            </div>
        </header>

        <!-- Navigation Bar (Sub-categories) -->
        <nav id="topNav" class="fixed top-6 left-1/2 -translate-x-1/2 z-50 glass-card px-4 py-2 rounded-full hidden shadow-2xl">
            <div class="flex gap-2 text-white">
                <button onclick="showCategories()" class="text-[10px] md:text-xs font-bold uppercase px-3 py-2 hover:text-yellow-500">Back</button>
                <button onclick="changeCategory('kids')" class="text-[10px] md:text-xs font-bold uppercase px-3 py-2 hover:text-yellow-500">Kids</button>
                <button onclick="changeCategory('women')" class="text-[10px] md:text-xs font-bold uppercase px-3 py-2 hover:text-yellow-500">Women</button>
                <button onclick="changeCategory('men')" class="text-[10px] md:text-xs font-bold uppercase px-3 py-2 hover:text-yellow-500">Men</button>
                <button onclick="changeCategory('special')" class="text-[10px] md:text-xs font-bold uppercase px-3 py-2 hover:text-yellow-500">Special</button>
            </div>
        </nav>

        <!-- Main Categories -->
        <main id="collections-section">
            <div class="flex flex-col items-center mb-12">
                <h2 id="mainHeading" class="serif-font text-3xl md:text-4xl text-white mb-2 uppercase tracking-widest">Shop By Category</h2>
                <div class="h-1 w-20 bg-yellow-600 rounded-full"></div>
            </div>

            <div id="categoryGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
                <!-- Kids -->
                <div class="glass-card rounded-[2rem] p-6 text-center group cursor-pointer" onclick="changeCategory('kids')">
                    <div class="aspect-square overflow-hidden rounded-2xl mb-6">
                        <img src="https://i.postimg.cc/BPcV86n3/Screenshot-2024-05-05-145813.png" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700">
                    </div>
                    <h3 class="serif-font text-2xl mb-2">Kids Variety</h3>
                    <p class="text-slate-400 text-sm">Gentle and sweet scents for kids.</p>
                </div>
                <!-- Women -->
                <div class="glass-card rounded-[2rem] p-6 text-center group cursor-pointer" onclick="changeCategory('women')">
                    <div class="aspect-square overflow-hidden rounded-2xl mb-6">
                        <img src="https://i.postimg.cc/xqMCxSZS/Screenshot-2024-05-05-151454.png" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700">
                    </div>
                    <h3 class="serif-font text-2xl mb-2">Women Bloom</h3>
                    <p class="text-slate-400 text-sm">Floral elegance and grace.</p>
                </div>
                <!-- Men -->
                <div class="glass-card rounded-[2rem] p-6 text-center group cursor-pointer" onclick="changeCategory('men')">
                    <div class="aspect-square overflow-hidden rounded-2xl mb-6">
                        <img src="https://i.postimg.cc/9420Hgwn/Screenshot-2024-05-05-153442.png" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700">
                    </div>
                    <h3 class="serif-font text-2xl mb-2">Men Intense</h3>
                    <p class="text-slate-400 text-sm">Strong and bold masculine scents.</p>
                </div>
                <!-- Special -->
                <div class="glass-card rounded-[2rem] p-6 text-center group cursor-pointer" onclick="changeCategory('special')">
                    <div class="aspect-square overflow-hidden rounded-2xl mb-6">
                        <img src="https://i.postimg.cc/hJQzKQ2X/Screenshot-2024-05-05-152909.png" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700">
                    </div>
                    <h3 class="serif-font text-2xl mb-2">Exclusive</h3>
                    <p class="text-slate-400 text-sm">Our most precious blends.</p>
                </div>
            </div>

            <div id="productGrid" class="hidden grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8"></div>
        </main>

        <!-- Reviews Section -->
        <section id="reviews-section" class="mt-32">
            <div class="text-center mb-12">
                <h2 class="serif-font text-3xl gold-gradient uppercase tracking-widest">Customer Reviews</h2>
                <p class="text-slate-500 mt-2">What our valued customers have to say</p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="glass-card p-8 rounded-3xl relative">
                    <div class="text-yellow-500 mb-4 text-xl">★★★★★</div>
                    <p class="italic text-slate-300">"Honestly, the fragrance quality is outstanding. Long-lasting and I received the delivery right on time."</p>
                    <div class="mt-6 font-bold text-sm gold-gradient uppercase tracking-tighter">— Ahmed Khan, Karachi</div>
                </div>
                <div class="glass-card p-8 rounded-3xl relative">
                    <div class="text-yellow-500 mb-4 text-xl">★★★★★</div>
                    <p class="italic text-slate-300">"Black Oud has become my favorite. It feels truly premium, comparable to top global brands."</p>
                    <div class="mt-6 font-bold text-sm gold-gradient uppercase tracking-tighter">— Sarah Sheikh, Lahore</div>
                </div>
                <div class="glass-card p-8 rounded-3xl relative">
                    <div class="text-yellow-500 mb-4 text-xl">★★★★★</div>
                    <p class="italic text-slate-300">"My children loved the kids variety, Candy Cloud is the best. The packaging is very luxurious."</p>
                    <div class="mt-6 font-bold text-sm gold-gradient uppercase tracking-tighter">— Mrs. Zafar, Islamabad</div>
                </div>
            </div>
        </section>

        <!-- FAQ Section -->
        <section id="faq-section" class="mt-32 max-w-3xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="serif-font text-3xl gold-gradient uppercase tracking-widest">Frequently Asked Questions</h2>
                <p class="text-slate-500 mt-2">Find answers to common queries</p>
            </div>
            <div class="space-y-4">
                <div class="glass-card rounded-2xl p-6 faq-item">
                    <input type="checkbox" id="faq1" class="hidden">
                    <label for="faq1" class="flex justify-between items-center cursor-pointer font-bold">
                        <span>How long does delivery take?</span>
                        <span class="text-yellow-500 text-xl font-light transition-transform">+</span>
                    </label>
                    <div class="faq-content text-slate-400 text-sm leading-relaxed">
                        Delivery to any city in Pakistan typically takes 2 to 4 working days.
                    </div>
                </div>
                <div class="glass-card rounded-2xl p-6 faq-item">
                    <input type="checkbox" id="faq2" class="hidden">
                    <label for="faq2" class="flex justify-between items-center cursor-pointer font-bold">
                        <span>What is the longevity of the fragrances?</span>
                        <span class="text-yellow-500 text-xl font-light">+</span>
                    </label>
                    <div class="faq-content text-slate-400 text-sm leading-relaxed">
                        Our fragrances usually last 8 to 12 hours on the skin, and even longer on fabric.
                    </div>
                </div>
                <div class="glass-card rounded-2xl p-6 faq-item">
                    <input type="checkbox" id="faq3" class="hidden">
                    <label for="faq3" class="flex justify-between items-center cursor-pointer font-bold">
                        <span>What payment methods are available?</span>
                        <span class="text-yellow-500 text-xl font-light">+</span>
                    </label>
                    <div class="faq-content text-slate-400 text-sm leading-relaxed">
                        We offer both Cash on Delivery (COD) and Bank Transfer/JazzCash payment options.
                    </div>
                </div>
            </div>
        </section>

        <!-- Order Form -->
        <section id="order-section" class="mt-32 max-w-3xl mx-auto">
            <div class="glass-card rounded-[2.5rem] p-8 md:p-12 border-t-4 border-yellow-600">
                <div class="text-center mb-10">
                    <h2 class="serif-font text-3xl gold-gradient uppercase tracking-widest mb-2">Book Your Essence</h2>
                    <p class="text-slate-400 italic text-sm">Order now to experience true luxury.</p>
                </div>
                <form id="orderForm" onsubmit="handleOrder(event)" class="space-y-6">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <input type="text" id="custName" placeholder="Full Name" class="w-full bg-white/5 border border-white/10 rounded-2xl px-6 py-4 focus:border-yellow-600 transition-all text-white outline-none" required>
                        <input type="tel" id="custPhone" placeholder="WhatsApp Number" class="w-full bg-white/5 border border-white/10 rounded-2xl px-6 py-4 focus:border-yellow-600 transition-all text-white outline-none" required>
                    </div>
                    <input type="text" id="custAddress" placeholder="Complete Shipping Address" class="w-full bg-white/5 border border-white/10 rounded-2xl px-6 py-4 focus:border-yellow-600 transition-all text-white outline-none" required>
                    <input type="text" id="selectedProduct" class="w-full bg-yellow-600/10 border border-yellow-600/30 rounded-2xl px-6 py-4 text-yellow-500 font-bold" readonly required placeholder="Select a perfume above">
                    <button type="submit" class="btn-gold w-full py-5 rounded-2xl text-lg flex items-center justify-center gap-3 uppercase tracking-widest">Confirm Order</button>
                </form>
            </div>
        </section>

        <!-- Footer -->
        <footer class="mt-32 pb-16 text-center">
            <div class="h-px w-full bg-gradient-to-r from-transparent via-white/10 to-transparent mb-8"></div>
            <p class="text-slate-500 text-[10px] tracking-[0.5em] uppercase mb-8">&copy; 2024 Al Ghani Fragrances. All Rights Reserved.</p>
            <div class="flex justify-center gap-8 items-center">
                <a href="https://www.facebook.com/profile.php?id=61572821001883" target="_blank" class="w-12 h-12 border border-white/10 rounded-full flex items-center justify-center hover:bg-blue-600 hover:border-blue-600 transition-all text-slate-400 hover:text-white">
                    <svg class="w-6 h-6 fill-current" viewBox="0 0 24 24"><path d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z"/></svg>
                </a>
                <a href="https://www.instagram.com/alghanifragnance" target="_blank" class="w-12 h-12 border border-white/10 rounded-full flex items-center justify-center hover:bg-pink-600 hover:border-pink-600 transition-all text-slate-400 hover:text-white">
                    <svg class="w-6 h-6 fill-current" viewBox="0 0 24 24"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849s-.011 3.584-.069 4.849c-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07s-3.584-.012-4.849-.07c-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849s.012-3.584.07-4.849c.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948s.014 3.667.072 4.947c.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072s3.667-.014 4.947-.072c4.358-.2 6.78-2.618 6.98-6.98.058-1.28.072-1.689.072-4.948s-.014-3.667-.072-4.947c-.2-4.358-2.618-6.78-6.98-6.98-1.28-.058-1.689-.072-4.948-.072zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4z"/></svg>
                </a>
            </div>
        </footer>
    </div>

    <div id="toast" class="message-toast text-white font-bold">Order Sent to WhatsApp!</div>

    <script>
        function toggleMenu() {
            const menu = document.getElementById('sideMenu');
            menu.classList.toggle('menu-open');
        }

        // Central navigation handler to close menu and scroll to section
        function handleNav(section) {
            toggleMenu(); // Close menu
            
            if (section === 'home') {
                showCategories();
                document.getElementById('home-top').scrollIntoView({ behavior: 'smooth' });
            } else if (section === 'collections') {
                showCategories();
                document.getElementById('collections-section').scrollIntoView({ behavior: 'smooth' });
            } else if (section === 'reviews') {
                document.getElementById('reviews-section').scrollIntoView({ behavior: 'smooth' });
            } else if (section === 'faqs') {
                document.getElementById('faq-section').scrollIntoView({ behavior: 'smooth' });
            } else if (section === 'order') {
                document.getElementById('order-section').scrollIntoView({ behavior: 'smooth' });
            }
        }

        const inventory = [
            { name: "Bubblegum Joy", category: "kids", price: 1000, img: "https://i.postimg.cc/BPcV86n3/Screenshot-2024-05-05-145813.png" },
            { name: "Candy Cloud", category: "kids", price: 1000, img: "https://i.postimg.cc/BPcV86n3/Screenshot-2024-05-05-145813.png" },
            { name: "Velvet Rose", category: "women", price: 1800, img: "https://i.postimg.cc/xqMCxSZS/Screenshot-2024-05-05-151454.png" },
            { name: "Golden Bloom", category: "women", price: 2200, img: "https://i.postimg.cc/xqMCxSZS/Screenshot-2024-05-05-151454.png" },
            { name: "Silver Mountain", category: "men", price: 1200, img: "https://i.postimg.cc/9420Hgwn/Screenshot-2024-05-05-153442.png" },
            { name: "Black Oud", category: "men", price: 1500, img: "https://i.postimg.cc/9420Hgwn/Screenshot-2024-05-05-153442.png" },
            { name: "Royal Amber", category: "special", price: 3000, img: "https://i.postimg.cc/hJQzKQ2X/Screenshot-2024-05-05-152909.png" }
        ];

        function changeCategory(cat) {
            document.getElementById('categoryGrid').classList.add('hidden');
            document.getElementById('productGrid').classList.remove('hidden');
            document.getElementById('topNav').classList.remove('hidden');
            document.getElementById('mainHeading').textContent = cat.toUpperCase() + " COLLECTION";
            
            const filtered = inventory.filter(p => p.category === cat);
            const grid = document.getElementById('productGrid');
            grid.innerHTML = '';
            filtered.forEach(p => {
                grid.innerHTML += `
                    <div class="glass-card rounded-[2rem] p-4 text-center">
                        <img src="${p.img}" class="rounded-2xl mb-4">
                        <h4 class="serif-font text-lg">${p.name}</h4>
                        <p class="text-yellow-600 font-bold mb-4">Rs. ${p.price.toLocaleString()}</p>
                        <button onclick="selectForOrder('${p.name}')" class="btn-gold w-full py-2 rounded-xl text-xs uppercase tracking-widest">Select Item</button>
                    </div>`;
            });
            document.getElementById('collections-section').scrollIntoView({ behavior: 'smooth' });
        }

        function showCategories() {
            document.getElementById('categoryGrid').classList.remove('hidden');
            document.getElementById('productGrid').classList.add('hidden');
            document.getElementById('topNav').classList.add('hidden');
            document.getElementById('mainHeading').textContent = "Shop By Category";
        }

        function selectForOrder(pName) {
            document.getElementById('selectedProduct').value = pName;
            document.getElementById('order-section').scrollIntoView({ behavior: 'smooth' });
        }

        function handleOrder(e) {
            e.preventDefault();
            const text = `⚜️ *Al Ghani Order* ⚜️\n\n🛍️ *Item:* ${document.getElementById('selectedProduct').value}\n👤 *Customer:* ${document.getElementById('custName').value}\n📱 *Phone:* ${document.getElementById('custPhone').value}\n📍 *Address:* ${document.getElementById('custAddress').value}`;
            window.open(`https://wa.me/923442128439?text=${encodeURIComponent(text)}`, '_blank');
            const toast = document.getElementById('toast');
            toast.style.display = 'block';
            setTimeout(() => toast.style.display = 'none', 4000);
        }
    </script>
</body>
</html>

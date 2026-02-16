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
            --glass-bg: rgba(255, 255, 255, 0.03);
        }

        body {
            font-family: 'Montserrat', sans-serif;
            background: radial-gradient(circle at top, #1e293b 0%, #020617 100%);
            color: #f8fafc;
            overflow-x: hidden;
        }

        .serif-font { font-family: 'Cinzel', serif; }

        /* Smooth Glass Effect */
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
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
        }

        /* Gold Gradient Text */
        .gold-gradient {
            background: linear-gradient(to right, #bf953f, #fcf6ba, #b38728, #fbf5b7, #aa771c);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* Premium Buttons */
        .btn-gold {
            background: linear-gradient(135deg, #c5a059 0%, #927438 100%);
            color: #000;
            font-weight: 700;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(197, 160, 89, 0.3);
        }

        .btn-gold:hover {
            transform: scale(1.03);
            box-shadow: 0 6px 25px rgba(197, 160, 89, 0.5);
        }

        .btn-outline-gold {
            border: 1px solid var(--royal-gold);
            color: var(--royal-gold);
            transition: all 0.3s ease;
        }

        .btn-outline-gold:hover {
            background: var(--royal-gold);
            color: #000;
        }

        /* Animations */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }

        .float-anim { animation: float 4s ease-in-out infinite; }

        .reveal-anim {
            animation: slideUp 0.8s cubic-bezier(0.23, 1, 0.32, 1) forwards;
        }

        @keyframes slideUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Category Transition */
        .fade-in { animation: fadeIn 0.5s ease-in; }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

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

    <div class="max-w-7xl mx-auto">
        
        <!-- Luxury Header -->
        <header class="text-center mb-16 reveal-anim">
            <div class="flex justify-center mb-6">
                <img src="https://i.postimg.cc/LqWtTMb1/Screenshot-2024-05-05-152628.png" alt="Al Ghani Logo" class="h-24 md:h-32 float-anim filter brightness-110">
            </div>
            <h1 class="serif-font text-5xl md:text-8xl font-bold gold-gradient tracking-tighter mb-4">Al Ghani</h1>
            <div class="flex items-center justify-center gap-4">
                <div class="h-px w-12 bg-gradient-to-r from-transparent to-yellow-600"></div>
                <p class="text-slate-400 tracking-[0.4em] text-xs md:text-sm uppercase">Pure Luxury Fragrances</p>
                <div class="h-px w-12 bg-gradient-to-l from-transparent to-yellow-600"></div>
            </div>
        </header>

        <!-- Navigation Bar (Hidden by default, shown in sub-category) -->
        <nav id="topNav" class="fixed top-6 left-1/2 -translate-x-1/2 z-50 glass-card px-4 py-2 rounded-full hidden fade-in">
            <div class="flex gap-2">
                <button onclick="showCategories()" class="text-xs font-bold uppercase px-4 py-2 hover:text-yellow-500">Home</button>
                <div class="w-px h-4 bg-white/10 self-center"></div>
                <button onclick="changeCategory('kids')" class="text-xs font-bold uppercase px-4 py-2 hover:text-yellow-500">Kids</button>
                <button onclick="changeCategory('women')" class="text-xs font-bold uppercase px-4 py-2 hover:text-yellow-500">Women</button>
                <button onclick="changeCategory('men')" class="text-xs font-bold uppercase px-4 py-2 hover:text-yellow-500">Men</button>
                <button onclick="changeCategory('special')" class="text-xs font-bold uppercase px-4 py-2 hover:text-yellow-500">Special</button>
            </div>
        </nav>

        <!-- Main Content -->
        <main>
            <!-- Title Section -->
            <div class="flex flex-col items-center mb-12">
                <h2 id="mainHeading" class="serif-font text-3xl md:text-4xl text-white mb-2">Shop By Category</h2>
                <div class="h-1 w-20 bg-yellow-600 rounded-full"></div>
            </div>

            <!-- Category Grid (The Home View) -->
            <div id="categoryGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8 reveal-anim">
                <!-- Kids -->
                <div class="glass-card rounded-[2rem] p-6 text-center group cursor-pointer" onclick="changeCategory('kids')">
                    <div class="aspect-square overflow-hidden rounded-2xl mb-6">
                        <img src="https://i.postimg.cc/BPcV86n3/Screenshot-2024-05-05-145813.png" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700">
                    </div>
                    <h3 class="serif-font text-2xl mb-2">Kids Variety</h3>
                    <p class="text-slate-400 text-sm mb-6">Maasoom aur meethey scents bacho ke liye.</p>
                    <button class="btn-outline-gold w-full py-3 rounded-xl font-bold uppercase text-xs tracking-widest">More Options</button>
                </div>

                <!-- Women -->
                <div class="glass-card rounded-[2rem] p-6 text-center group cursor-pointer" onclick="changeCategory('women')">
                    <div class="aspect-square overflow-hidden rounded-2xl mb-6">
                        <img src="https://i.postimg.cc/xqMCxSZS/Screenshot-2024-05-05-151454.png" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700">
                    </div>
                    <h3 class="serif-font text-2xl mb-2">Women Bloom</h3>
                    <p class="text-slate-400 text-sm mb-6">Phoolon jaisi nazaakat aur khushboo.</p>
                    <button class="btn-outline-gold w-full py-3 rounded-xl font-bold uppercase text-xs tracking-widest">More Options</button>
                </div>

                <!-- Men -->
                <div class="glass-card rounded-[2rem] p-6 text-center group cursor-pointer" onclick="changeCategory('men')">
                    <div class="aspect-square overflow-hidden rounded-2xl mb-6">
                        <img src="https://i.postimg.cc/9420Hgwn/Screenshot-2024-05-05-153442.png" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700">
                    </div>
                    <h3 class="serif-font text-2xl mb-2">Men Intense</h3>
                    <p class="text-slate-400 text-sm mb-6">Mazboot aur pur-asar mardana khushboo.</p>
                    <button class="btn-outline-gold w-full py-3 rounded-xl font-bold uppercase text-xs tracking-widest">More Options</button>
                </div>

                <!-- Special -->
                <div class="glass-card rounded-[2rem] p-6 text-center group cursor-pointer" onclick="changeCategory('special')">
                    <div class="aspect-square overflow-hidden rounded-2xl mb-6">
                        <img src="https://i.postimg.cc/hJQzKQ2X/Screenshot-2024-05-05-152909.png" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700">
                    </div>
                    <h3 class="serif-font text-2xl mb-2">Exclusive Edition</h3>
                    <p class="text-slate-400 text-sm mb-6">Hamari sab se nayab aur qeemti blends.</p>
                    <button class="btn-outline-gold w-full py-3 rounded-xl font-bold uppercase text-xs tracking-widest">More Options</button>
                </div>
            </div>

            <!-- Product Display (Filtered Results) -->
            <div id="productGrid" class="hidden grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8 fade-in">
                <!-- Products will be injected here -->
            </div>
        </main>

        <!-- Order Form Section -->
        <section id="order-section" class="mt-32 max-w-3xl mx-auto reveal-anim">
            <div class="glass-card rounded-[2.5rem] p-8 md:p-12 border-t-4 border-yellow-600">
                <div class="text-center mb-10">
                    <h2 class="serif-font text-3xl gold-gradient uppercase tracking-widest mb-2">Book Your Essence</h2>
                    <p class="text-slate-400 italic">Abhi order karein aur luxury mehsoos karein.</p>
                </div>
                
                <form id="orderForm" onsubmit="handleOrder(event)" class="space-y-6">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div class="space-y-2">
                            <label class="text-[10px] uppercase tracking-widest text-slate-500 ml-2">Poora Naam</label>
                            <input type="text" id="custName" placeholder="Enter name" class="w-full bg-white/5 border border-white/10 rounded-2xl px-6 py-4 focus:outline-none focus:border-yellow-600 transition-all text-white" required>
                        </div>
                        <div class="space-y-2">
                            <label class="text-[10px] uppercase tracking-widest text-slate-500 ml-2">WhatsApp No.</label>
                            <input type="tel" id="custPhone" placeholder="03xx xxxxxxx" class="w-full bg-white/5 border border-white/10 rounded-2xl px-6 py-4 focus:outline-none focus:border-yellow-600 transition-all text-white" required>
                        </div>
                    </div>
                    <div class="space-y-2">
                        <label class="text-[10px] uppercase tracking-widest text-slate-500 ml-2">Mukammal Address</label>
                        <input type="text" id="custAddress" placeholder="Ghar ka pata aur shehar" class="w-full bg-white/5 border border-white/10 rounded-2xl px-6 py-4 focus:outline-none focus:border-yellow-600 transition-all text-white" required>
                    </div>
                    <div class="space-y-2">
                        <label class="text-[10px] uppercase tracking-widest text-slate-500 ml-2">Selected Perfume</label>
                        <input type="text" id="selectedProduct" class="w-full bg-yellow-600/10 border border-yellow-600/30 rounded-2xl px-6 py-4 text-yellow-500 font-bold" readonly required placeholder="Upar se koi perfume select karein">
                    </div>
                    
                    <button type="submit" class="btn-gold w-full py-5 rounded-2xl text-lg flex items-center justify-center gap-3 mt-4">
                        <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M12.031 6.172c-3.181 0-5.767 2.586-5.768 5.766-.001 1.298.38 2.27 1.038 3.284l-.569 2.1c-.149.546.338 1.033.884.884l2.1-.569c1.014.658 1.986 1.038 3.284 1.038 3.181 0 5.767-2.586 5.768-5.766 0-3.181-2.587-5.767-5.767-5.767zm3.39 8.135c-.15.422-.743.815-1.026.863-.283.048-.636.064-1.012-.056-.376-.12-1.623-.63-3.087-1.932-1.157-1.037-1.939-2.262-2.165-2.644-.225-.383-.024-.59.171-.785.176-.176.383-.445.575-.668.192-.223.256-.383.383-.638.128-.255.064-.479-.032-.67-.096-.191-.863-2.073-1.183-2.84-.31-.741-.628-.64-.863-.652-.221-.012-.475-.015-.729-.015-.254 0-.668.096-1.017.477-.349.381-1.332 1.302-1.332 3.174 0 1.871 1.364 3.682 1.554 3.937.191.255 2.685 4.1 6.503 5.746.908.391 1.618.625 2.17.8.913.29 1.745.249 2.403.15.733-.11 2.262-.925 2.578-1.819.317-.894.317-1.658.221-1.819-.096-.161-.351-.255-.702-.431z"/></svg>
                        Confirm Order on WhatsApp
                    </button>
                </form>
            </div>
        </section>

        <!-- Simple Footer -->
        <footer class="mt-32 pb-16 text-center">
            <div class="h-px w-full bg-gradient-to-r from-transparent via-white/10 to-transparent mb-8"></div>
            <p class="text-slate-500 text-xs tracking-[0.5em] uppercase mb-4">&copy; 2024 Al Ghani Fragrances</p>
            <div class="flex justify-center gap-6 text-slate-400 text-sm">
                <span>Insta</span>
                <span>Fb</span>
                <span>Contact</span>
            </div>
        </footer>
    </div>

    <!-- Toast Notification -->
    <div id="toast" class="message-toast text-white font-bold shadow-2xl">
        Order Sent to WhatsApp!
    </div>

    <script>
        const inventory = [
            // Kids
            { name: "Bubblegum Joy", category: "kids", price: 1000, img: "https://i.postimg.cc/BPcV86n3/Screenshot-2024-05-05-145813.png", note: "Bacho ka pasandeeda" },
            { name: "Candy Cloud", category: "kids", price: 1000, img: "https://i.postimg.cc/BPcV86n3/Screenshot-2024-05-05-145813.png", note: "Meetahi khushboo" },
            { name: "Fairy Tale", category: "kids", price: 1000, img: "https://i.postimg.cc/BPcV86n3/Screenshot-2024-05-05-145813.png", note: "Magical Scent" },
            // Women
            { name: "Velvet Rose", category: "women", price: 1800, img: "https://i.postimg.cc/xqMCxSZS/Screenshot-2024-05-05-151454.png", note: "Luxury Rose" },
            { name: "Midnight Jasmine", category: "women", price: 1800, img: "https://i.postimg.cc/xqMCxSZS/Screenshot-2024-05-05-151454.png", note: "Raat ki rani" },
            { name: "Golden Bloom", category: "women", price: 2200, img: "https://i.postimg.cc/xqMCxSZS/Screenshot-2024-05-05-151454.png", note: "Premium Floral" },
            // Men
            { name: "Silver Mountain", category: "men", price: 1200, img: "https://i.postimg.cc/9420Hgwn/Screenshot-2024-05-05-153442.png", note: "Fresh & Strong" },
            { name: "Black Oud", category: "men", price: 1500, img: "https://i.postimg.cc/9420Hgwn/Screenshot-2024-05-05-153442.png", note: "Arabic Classic" },
            { name: "Oceanic Blue", category: "men", price: 1200, img: "https://i.postimg.cc/9420Hgwn/Screenshot-2024-05-05-153442.png", note: "Cool Breeze" },
            // Special
            { name: "Royal Amber", category: "special", price: 3000, img: "https://i.postimg.cc/hJQzKQ2X/Screenshot-2024-05-05-152909.png", note: "Rare Blend" },
            { name: "Saffron Spirit", category: "special", price: 3500, img: "https://i.postimg.cc/hJQzKQ2X/Screenshot-2024-05-05-152909.png", note: "Zafran Mix" }
        ];

        function changeCategory(cat) {
            const catGrid = document.getElementById('categoryGrid');
            const prodGrid = document.getElementById('productGrid');
            const nav = document.getElementById('topNav');
            const heading = document.getElementById('mainHeading');

            // Toggle visibility
            catGrid.classList.add('hidden');
            prodGrid.classList.remove('hidden');
            nav.classList.remove('hidden');
            
            heading.textContent = cat.charAt(0).toUpperCase() + cat.slice(1) + " Collection";
            
            // Build items
            const filtered = inventory.filter(p => p.category === cat);
            prodGrid.innerHTML = '';
            
            filtered.forEach(p => {
                prodGrid.innerHTML += `
                    <div class="glass-card rounded-[2rem] p-4 text-center group">
                        <div class="aspect-square overflow-hidden rounded-2xl mb-4 relative">
                            <img src="${p.img}" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                            <div class="absolute inset-0 bg-black/40 opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center">
                                <span class="text-white font-bold tracking-widest text-xs">VIEW DETAILS</span>
                            </div>
                        </div>
                        <h4 class="serif-font text-lg mb-1">${p.name}</h4>
                        <p class="text-yellow-600 font-bold mb-4">Rs. ${p.price.toLocaleString()}</p>
                        <button onclick="selectForOrder('${p.name}')" class="btn-gold w-full py-3 rounded-xl text-xs uppercase">Select Scents</button>
                    </div>
                `;
            });

            window.scrollTo({ top: 400, behavior: 'smooth' });
        }

        function showCategories() {
            document.getElementById('categoryGrid').classList.remove('hidden');
            document.getElementById('productGrid').classList.add('hidden');
            document.getElementById('topNav').classList.add('hidden');
            document.getElementById('mainHeading').textContent = "Shop By Category";
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function selectForOrder(pName) {
            document.getElementById('selectedProduct').value = pName;
            document.getElementById('order-section').scrollIntoView({ behavior: 'smooth', block: 'center' });
        }

        function handleOrder(e) {
            e.preventDefault();
            const name = document.getElementById('custName').value;
            const phone = document.getElementById('custPhone').value;
            const addr = document.getElementById('custAddress').value;
            const prod = document.getElementById('selectedProduct').value;

            const text = `⚜️ *Al Ghani Fragrances - New Order* ⚜️\n\n🛍️ *Item:* ${prod}\n👤 *Customer:* ${name}\n📱 *Contact:* ${phone}\n📍 *Address:* ${addr}\n\n_Thank you for choosing luxury._`;
            
            window.open(`https://wa.me/923442128439?text=${encodeURIComponent(text)}`, '_blank');
            
            const toast = document.getElementById('toast');
            toast.style.display = 'block';
            setTimeout(() => toast.style.display = 'none', 4000);
        }
    </script>
</body>
</html>

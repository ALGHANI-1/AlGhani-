<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Al Ghani Fragrances | Exquisite Scents</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;1,400&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --gold: #d4af37;
            --deep-violet: #2e1065;
        }
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #020617;
            background-image: linear-gradient(rgba(2, 6, 23, 0.8), rgba(2, 6, 23, 0.8)), url('https://i.postimg.cc/zb9yLzPx/Screenshot-2024-05-05-151302.png');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: #f8fafc;
        }
        h1, h2, h3, .brand-font {
            font-family: 'Playfair Display', serif;
        }
        .glass-panel {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        .glass-inner {
            background: rgba(255, 255, 255, 0.98);
            color: #1e293b;
        }
        .gold-border {
            border: 2px solid var(--gold);
        }
        .gold-text {
            color: var(--gold);
        }
        .product-card {
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .product-card:hover {
            transform: translateY(-10px);
            border-color: var(--gold);
        }
        .btn-premium {
            background: linear-gradient(135deg, #4c1d95 0%, #1e1b4b 100%);
            transition: all 0.3s ease;
        }
        .btn-premium:hover {
            box-shadow: 0 0 20px rgba(139, 92, 246, 0.4);
            transform: scale(1.02);
        }
        .message-box {
            position: fixed;
            bottom: 30px;
            left: 50%;
            transform: translate(-50%, 100px);
            padding: 1rem 2.5rem;
            border-radius: 50px;
            color: white;
            z-index: 2000;
            transition: transform 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            text-align: center;
            min-width: 300px;
        }
        .message-box.show {
            transform: translate(-50%, 0);
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .animate-reveal {
            animation: fadeIn 0.8s ease forwards;
        }
    </style>
</head>
<body class="min-h-screen py-6 md:py-10 px-4 flex flex-col items-center">

    <div class="container mx-auto max-w-6xl">
        <!-- Main Frame -->
        <div class="glass-panel rounded-[30px] md:rounded-[40px] overflow-hidden shadow-2xl border border-white/10">
            
            <!-- Elegant Header -->
            <header class="glass-inner relative py-8 md:py-12 px-6 md:px-8 text-center border-b-4 border-[#d4af37]">
                <div class="absolute top-4 right-4 md:top-6 md:right-12">
                    <img src="https://i.postimg.cc/LqWtTMb1/Screenshot-2024-05-05-152628.png" alt="Logo" class="h-14 md:h-28 w-auto">
                </div>
                <div class="animate-reveal">
                    <span class="text-[10px] md:text-sm tracking-[0.3em] uppercase text-violet-600 font-semibold mb-2 block">Since 2024</span>
                    <h1 class="text-4xl md:text-7xl font-bold text-slate-900">Al Ghani</h1>
                    <div class="flex items-center justify-center gap-2 md:gap-4 mt-2">
                        <div class="h-px w-8 md:w-12 bg-gold"></div>
                        <p class="text-base md:text-xl italic font-light text-slate-600">Pure Essence of Luxury</p>
                        <div class="h-px w-8 md:w-12 bg-gold"></div>
                    </div>
                </div>
            </header>

            <!-- Product Grid Section -->
            <div class="glass-inner p-6 md:p-16">
                <div class="flex justify-between items-end mb-8 md:mb-12">
                    <div>
                        <h2 class="text-2xl md:text-3xl font-bold text-slate-800">Our Collection</h2>
                        <div class="h-1 w-16 md:h-1.5 md:w-20 bg-violet-600 mt-2 rounded-full"></div>
                    </div>
                </div>

                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 md:gap-8">
                    <!-- Product Items -->
                    <div class="product-card group bg-white border border-slate-100 rounded-2xl md:rounded-3xl p-4 shadow-sm">
                        <div class="overflow-hidden rounded-xl md:rounded-2xl relative mb-4">
                            <img src="https://i.postimg.cc/BPcV86n3/Screenshot-2024-05-05-145813.png" class="w-full h-56 md:h-64 object-cover group-hover:scale-110 transition-transform duration-700">
                            <div class="absolute top-3 left-3 bg-violet-600 text-white text-[10px] px-3 py-1 rounded-full font-bold uppercase tracking-widest">Bestseller</div>
                        </div>
                        <h3 class="text-lg md:text-xl font-bold text-slate-800 text-center">Kids Special</h3>
                        <p class="text-emerald-600 text-center font-semibold text-base md:text-lg my-2">Rs. 1,000</p>
                        <button onclick="orderNow('Kids Special')" class="btn-premium w-full text-white py-3 md:py-4 rounded-xl md:rounded-2xl font-semibold active:scale-95">Order Now</button>
                    </div>

                    <div class="product-card group bg-white border border-slate-100 rounded-2xl md:rounded-3xl p-4 shadow-sm">
                        <div class="overflow-hidden rounded-xl md:rounded-2xl relative mb-4">
                            <img src="https://i.postimg.cc/xqMCxSZS/Screenshot-2024-05-05-151454.png" class="w-full h-56 md:h-64 object-cover group-hover:scale-110 transition-transform duration-700">
                        </div>
                        <h3 class="text-lg md:text-xl font-bold text-slate-800 text-center">For Women</h3>
                        <p class="text-emerald-600 text-center font-semibold text-base md:text-lg my-2">Rs. 1,800</p>
                        <button onclick="orderNow('For Women')" class="btn-premium w-full text-white py-3 md:py-4 rounded-xl md:rounded-2xl font-semibold active:scale-95">Order Now</button>
                    </div>

                    <div class="product-card group bg-white border border-slate-100 rounded-2xl md:rounded-3xl p-4 shadow-sm">
                        <div class="overflow-hidden rounded-xl md:rounded-2xl relative mb-4">
                            <img src="https://i.postimg.cc/9420Hgwn/Screenshot-2024-05-05-153442.png" class="w-full h-56 md:h-64 object-cover group-hover:scale-110 transition-transform duration-700">
                        </div>
                        <h3 class="text-lg md:text-xl font-bold text-slate-800 text-center">For Men</h3>
                        <p class="text-emerald-600 text-center font-semibold text-base md:text-lg my-2">Rs. 1,200</p>
                        <button onclick="orderNow('For Men')" class="btn-premium w-full text-white py-3 md:py-4 rounded-xl md:rounded-2xl font-semibold active:scale-95">Order Now</button>
                    </div>

                    <div class="product-card group bg-white border border-slate-100 rounded-2xl md:rounded-3xl p-4 shadow-sm">
                        <div class="overflow-hidden rounded-xl md:rounded-2xl relative mb-4">
                            <img src="https://i.postimg.cc/hJQzKQ2X/Screenshot-2024-05-05-152909.png" class="w-full h-56 md:h-64 object-cover group-hover:scale-110 transition-transform duration-700">
                            <div class="absolute inset-0 bg-violet-900/10"></div>
                        </div>
                        <h3 class="text-lg md:text-xl font-bold text-slate-800 text-center">Special Edition</h3>
                        <p class="text-emerald-600 text-center font-semibold text-base md:text-lg my-2">Rs. 2,000</p>
                        <button onclick="orderNow('Special Al Ghani')" class="btn-premium w-full text-white py-3 md:py-4 rounded-xl md:rounded-2xl font-semibold active:scale-95">Order Now</button>
                    </div>
                </div>

                <!-- Featured Benefits Section -->
                <section class="mt-12 md:mt-20 py-10 md:py-16 bg-slate-50 rounded-[30px] md:rounded-[40px] border border-slate-200">
                    <div class="text-center mb-8 md:mb-12">
                        <h2 class="text-3xl md:text-4xl font-bold text-slate-800">Masterfully Crafted</h2>
                        <p class="text-sm md:text-base text-slate-500 mt-2">Quality that lingers throughout the day</p>
                    </div>
                    <div class="max-w-4xl mx-auto px-4 md:px-6">
                        <div class="relative group cursor-pointer overflow-hidden rounded-[24px] md:rounded-[32px] shadow-2xl gold-border">
                            <img src="https://i.postimg.cc/jS7Tfbws/Untitled-design-2.png" alt="Features" class="w-full transform transition-transform duration-1000 group-hover:scale-105">
                        </div>
                    </div>
                </section>

                <!-- Testimonials -->
                <section class="mt-12 md:mt-20 grid grid-cols-1 md:grid-cols-3 gap-6 md:gap-8">
                    <div class="bg-white p-6 md:p-8 rounded-2xl md:rounded-3xl shadow-sm border border-slate-100 italic text-slate-600 relative">
                        <span class="text-4xl md:text-6xl text-violet-200 absolute top-2 left-2 md:top-4 md:left-4 font-serif">“</span>
                        <p class="relative z-10 pt-4 text-sm md:text-base">"The scent lasts all day. I've received so many compliments at work!"</p>
                        <div class="mt-4 font-bold text-slate-800 not-italic text-sm md:text-base">— Sarah K.</div>
                    </div>
                    <div class="bg-violet-900 p-6 md:p-8 rounded-2xl md:rounded-3xl shadow-sm text-white italic relative">
                        <span class="text-4xl md:text-6xl text-violet-700 absolute top-2 left-2 md:top-4 md:left-4 font-serif">“</span>
                        <p class="relative z-10 pt-4 text-sm md:text-base">"The packaging is as luxury as the fragrance itself. Perfect for gifting."</p>
                        <div class="mt-4 font-bold text-gold not-italic text-sm md:text-base">— Ahmed R.</div>
                    </div>
                    <div class="bg-white p-6 md:p-8 rounded-2xl md:rounded-3xl shadow-sm border border-slate-100 italic text-slate-600 relative">
                        <span class="text-4xl md:text-6xl text-violet-200 absolute top-2 left-2 md:top-4 md:left-4 font-serif">“</span>
                        <p class="relative z-10 pt-4 text-sm md:text-base">"Finally, high-end quality fragrances that are actually affordable."</p>
                        <div class="mt-4 font-bold text-slate-800 not-italic text-sm md:text-base">— Maria L.</div>
                    </div>
                </section>

                <!-- Order Form -->
                <section id="order-form-section" class="mt-16 md:mt-24 max-w-4xl mx-auto bg-slate-900 text-white rounded-[30px] md:rounded-[40px] p-6 md:p-16 relative overflow-hidden">
                    <div class="absolute top-0 right-0 w-64 h-64 bg-violet-600/10 rounded-full blur-3xl -mr-32 -mt-32"></div>
                    
                    <div class="relative z-10 text-center mb-8 md:mb-12">
                        <h2 class="text-3xl md:text-4xl font-bold mb-4">Get Your Fragrance</h2>
                        <p class="text-sm md:text-base text-slate-400">Fill in the details below and we'll handle the rest via WhatsApp.</p>
                    </div>

                    <form id="orderForm" onsubmit="return sendOrder(event)" class="space-y-4 md:space-y-6">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 md:gap-6">
                            <div class="space-y-2">
                                <label class="text-xs md:text-sm font-medium text-slate-400 ml-1">Your Name</label>
                                <input type="text" id="name" placeholder="Full Name" class="w-full bg-white/5 border border-white/10 px-4 md:px-6 py-3 md:py-4 rounded-xl md:rounded-2xl focus:border-violet-500 focus:outline-none focus:ring-1 focus:ring-violet-500 transition-all text-white text-sm md:text-base" required>
                            </div>
                            <div class="space-y-2">
                                <label class="text-xs md:text-sm font-medium text-slate-400 ml-1">WhatsApp Number</label>
                                <input type="tel" id="phone" placeholder="03xx xxxxxxx" class="w-full bg-white/5 border border-white/10 px-4 md:px-6 py-3 md:py-4 rounded-xl md:rounded-2xl focus:border-violet-500 focus:outline-none focus:ring-1 focus:ring-violet-500 transition-all text-white text-sm md:text-base" required>
                            </div>
                        </div>
                        <div class="space-y-2">
                            <label class="text-xs md:text-sm font-medium text-slate-400 ml-1">Delivery Address</label>
                            <input type="text" id="address" placeholder="Complete address with city" class="w-full bg-white/5 border border-white/10 px-4 md:px-6 py-3 md:py-4 rounded-xl md:rounded-2xl focus:border-violet-500 focus:outline-none focus:ring-1 focus:ring-violet-500 transition-all text-white text-sm md:text-base" required>
                        </div>
                        <div class="space-y-2">
                            <label class="text-xs md:text-sm font-medium text-slate-400 ml-1">Selected Product</label>
                            <input type="text" id="product" placeholder="Click 'Order Now' on a perfume above" class="w-full bg-violet-500/10 border border-violet-500/30 px-4 md:px-6 py-3 md:py-4 rounded-xl md:rounded-2xl font-bold text-violet-400 cursor-not-allowed text-sm md:text-base" readonly required>
                        </div>
                        <button type="submit" class="w-full py-4 md:py-5 bg-emerald-600 hover:bg-emerald-500 text-white rounded-xl md:rounded-2xl font-bold text-lg md:text-xl shadow-xl transition-all transform active:scale-95 flex items-center justify-center gap-4 mt-6 md:mt-8">
                            <svg class="w-5 h-5 md:w-6 md:h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.946.003-6.556 5.338-11.891 11.893-11.891 3.181.001 6.167 1.24 8.413 3.488 2.245 2.248 3.481 5.236 3.48 8.414-.003 6.557-5.338 11.892-11.893 11.892-1.99-.001-3.951-.5-5.688-1.448l-6.305 1.654zm6.597-3.807c1.676.995 3.276 1.591 5.392 1.592 5.448 0 9.886-4.438 9.889-9.886.002-5.462-4.415-9.89-9.881-9.892-5.452 0-9.887 4.434-9.889 9.884 0 2.225.569 3.807 1.694 5.75l-.936 3.414 3.731-.978z"/></svg>
                            Confirm via WhatsApp
                        </button>
                    </form>
                </section>
            </div>

            <!-- Footer -->
            <footer class="bg-slate-900 border-t border-white/5 py-8 md:py-12 px-6 md:px-8 text-center">
                <div class="mb-6 md:mb-8">
                    <img src="https://i.postimg.cc/LqWtTMb1/Screenshot-2024-05-05-152628.png" alt="Logo" class="h-12 md:h-16 mx-auto mb-4 opacity-80">
                    <p class="text-slate-400 font-light tracking-widest uppercase text-xs md:text-sm">Al Ghani Fragrances</p>
                </div>
                <div class="flex flex-col md:flex-row items-center justify-center gap-4 md:gap-6 text-slate-300 text-sm md:text-base">
                    <a href="tel:03442128439" class="hover:text-gold transition-colors">📞 0344 2128439</a>
                    <span class="hidden md:block text-slate-700">|</span>
                    <span class="text-slate-500">📍 Nationwide Delivery in Pakistan</span>
                </div>
                <p class="mt-8 md:mt-12 text-[10px] md:text-xs text-slate-600 tracking-tighter uppercase font-medium">&copy; 2024 AL GHANI FRAGRANCES. CRAFTED WITH PASSION.</p>
            </footer>
        </div>
    </div>

    <div id="messageBox" class="message-box"></div>

    <script>
        function orderNow(perfume) {
            const productInput = document.getElementById('product');
            productInput.value = perfume;
            
            // Animation for selection
            productInput.parentElement.classList.add('scale-105');
            setTimeout(() => productInput.parentElement.classList.remove('scale-105'), 500);

            const orderFormSection = document.getElementById('order-form-section');
            if (orderFormSection) {
                orderFormSection.scrollIntoView({ behavior: 'smooth', block: 'center' });
            }
        }

        function sendOrder(event) {
            event.preventDefault();

            const name = document.getElementById('name').value.trim();
            const address = document.getElementById('address').value.trim();
            const phone = document.getElementById('phone').value.trim();
            const product = document.getElementById('product').value.trim();

            if (!name || !address || !phone || !product) {
                showMessage("Please select a perfume first.", 'error');
                return false;
            }

            const message = `🌟 *Al Ghani Fragrances - New Order* 🌟\n\n🎁 *Product:* ${product}\n👤 *Customer:* ${name}\n📍 *Address:* ${address}\n📱 *Contact:* ${phone}\n\n_Generated from Al Ghani Web Catalog_`;
            const encodedMessage = encodeURIComponent(message);
            const whatsappNumber = '923442128439';

            window.open(`https://wa.me/${whatsappNumber}?text=${encodedMessage}`, '_blank');

            document.getElementById('orderForm').reset();
            document.getElementById('product').value = '';

            showMessage("Order initiated! Redirecting to WhatsApp...", 'success');
            return false;
        }

        function showMessage(message, type) {
            const messageBox = document.getElementById('messageBox');
            messageBox.textContent = message;
            messageBox.style.backgroundColor = type === 'success' ? '#059669' : '#dc2626';
            
            messageBox.classList.add('show');
            setTimeout(() => messageBox.classList.remove('show'), 5000);
        }
    </script>
</body>
</html>

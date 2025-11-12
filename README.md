<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kotak Harta Karun Memori</title>
    <!-- Memuat Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Font Klasik & Elegan */
        @import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;600;700&family=Inter:wght@300;400;500&display=swap');

        /* Skema Warna Dusty Rose & Gold */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f7f2f4; /* Dusty Rose background */
            color: #333;
            min-height: 100vh;
            line-height: 1.7;
            padding: 0;
            margin: 0;
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        h1, h2, h3, .title-font {
            font-family: 'Cormorant Garamond', serif;
            color: #b08d57; /* Emas Kusam */
        }
        
        /* Card Utama - Lebih Transparan dan Bersih */
        .love-card {
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 10px 40px rgba(100, 100, 100, 0.1);
            border-radius: 25px;
            max-width: 700px;
            margin: 4rem auto;
            padding: 2rem;
        }

        /* --- Animasi Karakter Hati (Detak dan Gerak) --- */
        
        /* Animasi Detak Jantung */
        @keyframes heartbeat {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        /* Container untuk Animasi Latar Belakang */
        .heart-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none; /* Agar tidak menghalangi klik */
            overflow: hidden;
            z-index: -1;
            opacity: 0.5;
        }

        .animated-heart {
            position: absolute;
            font-size: 2.5rem;
            opacity: 0;
            color: #e3a9a9; /* Soft Pink */
            animation: float-up 10s linear infinite, fade-heart 5s ease-in-out infinite alternate;
        }

        @keyframes float-up {
            0% { transform: translateY(100vh) translateX(0); opacity: 0; }
            50% { opacity: 0.7; }
            100% { transform: translateY(-10vh) translateX(50px); opacity: 0; }
        }

        @keyframes fade-heart {
            0% { opacity: 0.5; }
            100% { opacity: 1; }
        }

        /* Script untuk menempatkan hati di posisi acak */
        .heart-container > *:nth-child(2n) { animation-delay: 2s; }
        .heart-container > *:nth-child(3n) { animation-delay: 4s; }
        .heart-container > *:nth-child(4n) { animation-delay: 6s; font-size: 3rem; }
        .heart-container > *:nth-child(5n) { animation-delay: 8s; font-size: 2rem; color: #b08d57; }
        
        /* --- Animasi Teks Fade-In (Scroll) --- */
        
        .reveal-text {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 1s ease-out, transform 0.6s ease-out;
        }
        .reveal-text.active {
            opacity: 1;
            transform: translateY(0);
        }
        
    </style>
</head>
<body>

    <!-- Container Animasi Hati -->
    <div class="heart-container">
        <span class="animated-heart" style="left: 10%;">❤️</span>
        <span class="animated-heart" style="left: 50%;">✨</span>
        <span class="animated-heart" style="left: 80%;">❤️</span>
        <span class="animated-heart" style="left: 25%;">✨</span>
        <span class="animated-heart" style="left: 65%;">❤️</span>
        <span class="animated-heart" style="left: 40%;">✨</span>
    </div>

    <!-- The Main Message Container -->
    <div class="love-card p-8 md:p-16 text-center">
        
        <!-- Header & Title -->
        <header class="mb-12">
            <h1 class="text-6xl md:text-7xl font-bold mb-2 tracking-wider title-font reveal-text">
                Surat yang Tak Selesai
            </h1>
            <h2 class="text-4xl font-light text-gray-700 reveal-text">
                Untuk Shofiana Wilda Salsabila
            </h2>
            
            <hr class="my-8 border-t-2 border-fuchsia-100 reveal-text">
            
            <p class="text-2xl title-font text-fuchsia-500 reveal-text">
                (Setiap detak adalah sebuah kata yang tak terucap)
            </p>
        </header>

        <!-- The Main Message Body -->
        <section class="text-xl text-gray-600 space-y-8">
            
            <p class="reveal-text">
                <span class="text-3xl font-bold title-font" style="color:#b08d57;">S</span>etiap hari yang berlalu sejak aku mengenalmu, aku sadar bahwa ada babak baru dalam hidupku yang sedang kubaca. Babak itu bernama kamu. Aku menemukan kehangatan dan ketenangan yang belum pernah kurasakan sebelumnya.
            </p>

            <p class="reveal-text">
                Kamu seperti kompas yang tiba-tiba muncul di tengah badai, menunjukkan arah yang harus kutuju. Bukan hanya karena pesonamu, tapi juga karena caramu melihat dunia — dengan kebaikan dan kecerdasan yang luar biasa.
            </p>

            <p class="reveal-text">
                Banyak orang datang dan pergi, tapi kamu... kamu adalah jeda yang tak ingin kulewatkan. Kamu adalah halaman utama yang selalu ingin kubuka.
            </p>

            <div class="p-6 bg-yellow-50 rounded-xl shadow-inner reveal-text">
                <p class="italic font-semibold text-2xl text-red-500 title-font">
                    Shofiana Wilda Salsabila,
                </p>
                <p class="mt-4 text-2xl text-gray-800">
                    Aku ingin mengakhiri ketidakpastian ini. Aku menyayangimu. <br>
                    Maukah kamu memberiku kesempatan untuk menulis babak terbaik kita bersama?
                </p>
            </div>

            <p class="reveal-text">
                Jika kamu bersedia, beri aku satu petunjuk kecil saja. Karena hatiku sudah terlalu lama menunggu jawaban itu.
            </p>

        </section>

        <!-- Signature/Footer -->
        <footer class="mt-12">
            <h3 class="text-3xl font-bold title-font reveal-text">
                Dengan segenap hati,
            </h3>
            <p class="text-2xl mt-3 text-gray-800 font-bold reveal-text">
                (Adit)
            </p>
            <p class="text-sm text-gray-400 mt-2 reveal-text">
                — Dikodekan oleh RizkyX, berharap yang terbaik untukmu.
            </p>
        </footer>

    </div>

    <!-- JavaScript for Scroll Fade-In Effect -->
    <script>
        // Logika untuk menambah class 'active' saat elemen masuk viewport
        function checkReveal() {
            const elements = document.querySelectorAll('.reveal-text:not(.active)');
            // Tampilkan elemen ketika 85% dari tinggi viewport sudah dilewati
            const triggerBottom = window.innerHeight * 0.90; 

            elements.forEach(element => {
                const elementTop = element.getBoundingClientRect().top;
                
                if (elementTop < triggerBottom) {
                    element.classList.add('active');
                }
            });
        }

        // Jalankan saat dokumen dimuat dan saat menggulir
        window.onload = function() {
            // Beri sedikit jeda agar semua elemen siap dimuat sebelum dicek
            setTimeout(checkReveal, 300);
            window.addEventListener('scroll', checkReveal);
            window.addEventListener('resize', checkReveal);
        };
    </script>

</body>
</html>

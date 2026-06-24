<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dinda Glow Beauty Store</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            min-height: 100vh;
            background: linear-gradient(135deg, #fce4ec, #f8f0e3);
            font-family: 'Segoe UI', 'Poppins', 'Helvetica Neue', sans-serif;
            padding: 30px 20px;
            display: flex;
            justify-content: center;
            align-items: flex-start;
        }

        .container {
            max-width: 820px;
            width: 100%;
            margin: 0 auto;
        }

        /* TOP BAR */
        .top-bar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(12px);
            padding: 14px 24px;
            border-radius: 60px;
            margin-bottom: 28px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.06);
            border: 1px solid rgba(255, 215, 215, 0.2);
            flex-wrap: wrap;
            gap: 10px;
        }

        .top-bar .brand-small {
            font-weight: 700;
            font-size: 1rem;
            color: #2c1810;
            letter-spacing: 0.5px;
        }

        .top-bar .brand-small span {
            color: #d4839a;
        }

        .top-bar .badge {
            background: linear-gradient(135deg, #e8a0b4, #d4839a);
            color: white;
            font-size: 0.6rem;
            padding: 4px 16px;
            border-radius: 40px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .login-btn-top {
            background: transparent;
            border: 1.5px solid #f0e4dc;
            border-radius: 40px;
            padding: 6px 20px;
            font-size: 0.65rem;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            color: #7a6b62;
            font-family: 'Segoe UI', Arial, sans-serif;
            cursor: pointer;
            transition: 0.3s;
            font-weight: 600;
            text-decoration: none;
            display: inline-block;
        }

        .login-btn-top:hover {
            background: #d4839a;
            color: white;
            border-color: #d4839a;
        }

        /* MAIN CARD */
        .card {
            background: #ffffff;
            border-radius: 40px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.08), 0 8px 24px rgba(0, 0, 0, 0.04);
            padding: 40px 35px 35px;
            border: 1px solid rgba(255, 215, 215, 0.15);
            position: relative;
            overflow: hidden;
        }

        .card::before {
            content: "✨";
            position: absolute;
            top: -30px;
            right: -20px;
            font-size: 120px;
            opacity: 0.04;
            transform: rotate(20deg);
        }

        .card::after {
            content: "💄";
            position: absolute;
            bottom: -40px;
            left: -30px;
            font-size: 150px;
            opacity: 0.03;
            transform: rotate(-15deg);
        }

        /* HEADER */
        .header {
            text-align: center;
            margin-bottom: 30px;
            position: relative;
            z-index: 1;
        }

        .header .icon {
            font-size: 3.2rem;
            margin-bottom: 4px;
        }

        .header h1 {
            font-size: 2.4rem;
            font-weight: 700;
            color: #2c1810;
            letter-spacing: 1px;
        }

        .header h1 span {
            background: linear-gradient(135deg, #e8a0b4, #d4839a);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .header .tagline {
            font-size: 1rem;
            font-weight: 300;
            color: #7a6b62;
            letter-spacing: 4px;
            text-transform: uppercase;
            border-top: 1px solid #f0e4dc;
            padding-top: 10px;
            margin-top: 4px;
        }

        .header .quote {
            font-size: 1.1rem;
            font-style: italic;
            color: #5a4a42;
            margin-top: 10px;
            font-weight: 400;
            letter-spacing: 0.5px;
        }

        .header .quote span {
            color: #d4839a;
            font-weight: 600;
        }

        /* SECTION */
        .section {
            margin-bottom: 28px;
            position: relative;
            z-index: 1;
        }

        .section-title {
            font-size: 1.1rem;
            font-weight: 700;
            color: #2c1810;
            letter-spacing: 1px;
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            gap: 10px;
            border-bottom: 2px solid #f8f0e3;
            padding-bottom: 8px;
        }

        .section-title .emoji {
            font-size: 1.2rem;
        }

        .section-content {
            color: #3d322b;
            font-size: 0.95rem;
            line-height: 1.7;
            padding-left: 6px;
        }

        .section-content p {
            margin-bottom: 6px;
        }

        .section-content ul {
            list-style: none;
            padding-left: 6px;
        }

        .section-content ul li {
            padding: 3px 0 3px 24px;
            position: relative;
        }

        .section-content ul li::before {
            content: "✦";
            position: absolute;
            left: 0;
            color: #d4839a;
            font-size: 0.8rem;
        }

        /* MODAL GRID */
        .modal-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 8px 20px;
            background: #faf6f3;
            border-radius: 20px;
            padding: 16px 20px;
            margin-top: 4px;
        }

        .modal-grid .item {
            display: flex;
            justify-content: space-between;
            padding: 6px 0;
            border-bottom: 1px dashed #f0e4dc;
            font-size: 0.9rem;
        }

        .modal-grid .item:last-child,
        .modal-grid .item:nth-last-child(2) {
            border-bottom: none;
        }

        .modal-grid .item .label {
            color: #7a6b62;
            font-weight: 400;
        }

        .modal-grid .item .value {
            font-weight: 600;
            color: #2c1810;
        }

        .modal-total {
            text-align: right;
            font-size: 1.1rem;
            font-weight: 700;
            color: #d4839a;
            padding-top: 8px;
            margin-top: 4px;
            border-top: 2px solid #f0e4dc;
        }

        /* CONTACT */
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px 20px;
            background: #faf6f3;
            border-radius: 20px;
            padding: 16px 20px;
            margin-top: 4px;
        }

        .contact-grid .item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
            padding: 4px 0;
            color: #3d322b;
        }

        .contact-grid .item .icon {
            font-size: 1rem;
            width: 24px;
            text-align: center;
        }

        .contact-grid .item .label {
            color: #7a6b62;
            font-weight: 400;
            margin-right: 2px;
        }

        .contact-grid .item a {
            color: #d4839a;
            text-decoration: none;
            font-weight: 500;
            transition: 0.2s;
        }

        .contact-grid .item a:hover {
            color: #b86a80;
            text-decoration: underline;
        }

        /* FOOTER */
        .footer-note {
            text-align: center;
            margin-top: 28px;
            font-size: 0.7rem;
            letter-spacing: 2px;
            color: #b9a99a;
            text-transform: uppercase;
            border-top: 1px solid #f0e4dc;
            padding-top: 18px;
            font-family: 'Segoe UI', Arial, sans-serif;
            position: relative;
            z-index: 1;
        }

        .footer-note span {
            font-weight: 600;
            color: #d4839a;
        }

        @media (max-width: 600px) {
            .card {
                padding: 28px 18px 25px;
                border-radius: 32px;
            }
            .header h1 {
                font-size: 1.8rem;
            }
            .modal-grid,
            .contact-grid {
                grid-template-columns: 1fr;
            }
            .modal-grid .item:nth-last-child(2) {
                border-bottom: 1px dashed #f0e4dc;
            }
            .modal-grid .item:last-child {
                border-bottom: none;
            }
            .top-bar {
                padding: 10px 16px;
                border-radius: 40px;
            }
            .top-bar .brand-small {
                font-size: 0.85rem;
            }
        }

        @media (max-width: 400px) {
            body {
                padding: 16px 12px;
            }
            .card {
                padding: 22px 14px 20px;
            }
            .header .quote {
                font-size: 0.95rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- TOP BAR -->
        <div class="top-bar">
            <div class="brand-small">💖 Dinda <span>Glow Beauty</span></div>
            <div style="display: flex; align-items: center; gap: 12px; flex-wrap: wrap;">
                <a href="#" class="login-btn-top" onclick="showLoginModal()">🔐 Login</a>
            </div>
        </div>

        <!-- MAIN CARD -->
        <div class="card">
            <!-- HEADER -->
            <div class="header">
                <div class="icon">💖</div>
                <h1>Dinda <span>Glow Beauty</span></h1>
                <div class="tagline">Parfum • Skincare • Makeup</div>
                <div class="quote">“<span>Cantik</span>, Percaya Diri, dan <span>Bersinar</span> Setiap Hari.”</div>
            </div>

            <!-- DESKRIPSI USAHA -->
            <div class="section">
                <div class="section-title"><span class="emoji">📖</span> Deskripsi Usaha</div>
                <div class="section-content">
                    <p>Glow Beauty Store adalah usaha yang menyediakan berbagai produk kecantikan seperti parfum, skincare, dan makeup dengan harga terjangkau. Produk yang dijual mengikuti tren kecantikan terkini dan cocok untuk remaja maupun dewasa.</p>
                </div>
            </div>

            <!-- MODAL AWAL -->
            <div class="section">
                <div class="section-title"><span class="emoji">💰</span> Modal Awal</div>
                <div class="modal-grid">
                    <div class="item"><span class="label">Stok parfum</span><span class="value">Rp500.000</span></div>
                    <div class="item"><span class="label">Stok skincare</span><span class="value">Rp1.000.000</span></div>
                    <div class="item"><span class="label">Stok makeup</span><span class="value">Rp1.000.000</span></div>
                    <div class="item"><span class="label">Kemasan & promosi</span><span class="value">Rp500.000</span></div>
                </div>
                <div class="modal-total">TOTAL MODAL : Rp3.000.000</div>
            </div>

            <!-- VISI -->
            <div class="section">
                <div class="section-title"><span class="emoji">👁️</span> Visi</div>
                <div class="section-content">
                    <p>Menjadi toko kecantikan terpercaya yang menyediakan produk berkualitas dengan harga terjangkau.</p>
                </div>
            </div>

            <!-- TARGET PASAR -->
            <div class="section">
                <div class="section-title"><span class="emoji">🎯</span> Target Pasar</div>
                <div class="section-content">
                    <ul>
                        <li>Pelajar dan mahasiswa.</li>
                        <li>Remaja hingga dewasa.</li>
                        <li>Pengguna media sosial yang mengikuti tren kecantikan.</li>
                    </ul>
                </div>
            </div>

            <!-- MISI -->
            <div class="section">
                <div class="section-title"><span class="emoji">📌</span> Misi</div>
                <div class="section-content">
                    <ul>
                        <li>Menjual produk kecantikan yang aman dan berkualitas.</li>
                        <li>Memberikan pelayanan yang ramah kepada pelanggan.</li>
                        <li>Mengikuti perkembangan tren kecantikan.</li>
                        <li>Menawarkan harga yang kompetitif.</li>
                    </ul>
                </div>
            </div>

            <!-- KEUNTUNGAN -->
            <div class="section">
                <div class="section-title"><span class="emoji">📈</span> Keuntungan</div>
                <div class="section-content">
                    <p>Jika keuntungan rata-rata 20% dari penjualan, maka dari omzet Rp5.000.000 per bulan bisa memperoleh laba sekitar <strong>Rp1.000.000</strong> per bulan.</p>
                </div>
            </div>

            <!-- KONTAK / INFORMASI -->
            <div class="section">
                <div class="section-title"><span class="emoji">📞</span> Kontak & Informasi</div>
                <div class="contact-grid">
                    <div class="item"><span class="icon">📱</span><span class="label">Telepon</span> <span style="font-weight:500;">0832 1465 8791</span></div>
                    <div class="item"><span class="icon">📷</span><span class="label">Instagram</span> <a href="https://instagram.com/dinsglowbeauty" target="_blank">@dinsglowbeauty</a></div>
                    <div class="item"><span class="icon">📧</span><span class="label">Email</span> <a href="mailto:glowbeauty_@gmail.com">glowbeauty_@gmail.com</a></div>
                    <div class="item"><span class="icon">📍</span><span class="label">Alamat</span> <span style="font-weight:500;">Jl. Taman Sari No. 16</span></div>
                </div>
            </div>

            <!-- FOOTER -->
            <div class="footer-note">
                <span>Dinda</span> · Glow Beauty Store · “Cantik, Percaya Diri, dan Bersinar Setiap Hari.”
            </div>
        </div>
    </div>

    <!-- LOGIN MODAL -->
    <div id="loginModal" style="display:none; position:fixed; top:0; left:0; right:0; bottom:0; background:rgba(0,0,0,0.5); backdrop-filter:blur(6px); z-index:9999; justify-content:center; align-items:center; padding:20px;">
        <div style="background:white; max-width:400px; width:100%; border-radius:32px; padding:40px 30px 35px; position:relative; box-shadow:0 20px 60px rgba(0,0,0,0.2);">
            <button onclick="closeLoginModal()" style="position:absolute; top:16px; right:20px; background:none; border:none; font-size:1.5rem; cursor:pointer; color:#7a6b62;">&times;</button>
            <div style="text-align:center; margin-bottom:24px;">
                <div style="font-size:2.5rem; margin-bottom:4px;">💖</div>
                <h2 style="font-size:1.5rem; color:#2c1810;">Login</h2>
                <p style="font-size:0.8rem; color:#7a6b62; margin-top:4px;">Masuk ke akun Dinda Glow Beauty</p>
            </div>
            <form id="loginForm" onsubmit="return false;">
                <div style="margin-bottom:16px;">
                    <label style="font-size:0.7rem; text-transform:uppercase; letter-spacing:1.5px; color:#7a6b62; font-weight:600; display:block; margin-bottom:4px;">Username</label>
                    <input type="text" id="loginUsername" value="dinda" style="width:100%; padding:12px 18px; border:1.5px solid #f0e4dc; border-radius:30px; font-size:0.95rem; outline:none; transition:0.3s; background:#faf6f3;" required>
                </div>
                <div style="margin-bottom:20px;">
                    <label style="font-size:0.7rem; text-transform:uppercase; letter-spacing:1.5px; color:#7a6b62; font-weight:600; display:block; margin-bottom:4px;">Password</label>
                    <input type="password" id="loginPassword" style="width:100%; padding:12px 18px; border:1.5px solid #f0e4dc; border-radius:30px; font-size:0.95rem; outline:none; transition:0.3s; background:#faf6f3;" required>
                </div>
                <div id="loginError" style="color:#d45a6a; font-size:0.8rem; text-align:center; margin-bottom:12px; display:none;">❌ Username atau password salah!</div>
                <button type="submit" onclick="handleLogin()" style="width:100%; padding:14px; background:linear-gradient(135deg, #e8a0b4, #d4839a); border:none; border-radius:30px; color:white; font-size:0.85rem; font-weight:600; text-transform:uppercase; letter-spacing:2px; cursor:pointer; transition:0.3s; box-shadow:0 4px 15px rgba(212,131,154,0.3);">Masuk</button>
            </form>
            <p style="text-align:center; margin-top:18px; font-size:0.6rem; color:#b9a99a; text-transform:uppercase; letter-spacing:1px;">Dinda · Glow Beauty Store</p>
        </div>
    </div>

    <script>
        function showLoginModal() {
            document.getElementById('loginModal').style.display = 'flex';
            document.getElementById('loginError').style.display = 'none';
            document.getElementById('loginPassword').value = '';
            document.getElementById('loginUsername').focus();
        }

        function closeLoginModal() {
            document.getElementById('loginModal').style.display = 'none';
        }

        function handleLogin() {
            const username = document.getElementById('loginUsername').value.trim().toLowerCase();
            const password = document.getElementById('loginPassword').value.trim();
            const errorEl = document.getElementById('loginError');

            if (username === 'dinda' && password === 'dinda') {
                // Login berhasil
                sessionStorage.setItem('dinda_glow_logged_in', 'true');
                closeLoginModal();
                // Ubah tombol login menjadi logout
                const loginBtn = document.querySelector('.login-btn-top');
                loginBtn.textContent = '🚪 Logout';
                loginBtn.onclick = function(e) {
                    e.preventDefault();
                    sessionStorage.removeItem('dinda_glow_logged_in');
                    location.reload();
                };
                alert('✅ Login berhasil! Selamat datang di Dinda Glow Beauty.');
                // Refresh untuk update tampilan
                location.reload();
            } else {
                errorEl.style.display = 'block';
                // Animasi shake
                const form = document.getElementById('loginForm');
                form.style.animation = 'none';
                setTimeout(() => {
                    form.style.animation = 'shake 0.4s ease';
                }, 10);
                setTimeout(() => {
                    form.style.animation = '';
                }, 500);
                document.getElementById('loginPassword').value = '';
                document.getElementById('loginPassword').focus();
            }
        }

        // Tambahkan animasi shake
        const style = document.createElement('style');
        style.textContent = `
            @keyframes shake {
                0%, 100% { transform: translateX(0); }
                20% { transform: translateX(-10px); }
                40% { transform: translateX(10px); }
                60% { transform: translateX(-6px); }
                80% { transform: translateX(6px); }
            }
        `;
        document.head.appendChild(style);

        // Cek status login saat halaman dimuat
        document.addEventListener('DOMContentLoaded', function() {
            if (sessionStorage.getItem('dinda_glow_logged_in') === 'true') {
                const loginBtn = document.querySelector('.login-btn-top');
                loginBtn.textContent = '🚪 Logout';
                loginBtn.onclick = function(e) {
                    e.preventDefault();
                    sessionStorage.removeItem('dinda_glow_logged_in');
                    location.reload();
                };
            }
        });

        // Tutup modal dengan klik di luar
        document.getElementById('loginModal').addEventListener('click', function(e) {
            if (e.target === this) {
                closeLoginModal();
            }
        });
    </script>
</body>
</html>

/* --- 1. Definisi Palet Warna (Sesuai Permintaan) --- */
:root {
    /* Light Mode */
    --color-background-light: #FFFFFF; /* Putih Bersih */
    --color-text-dark: #333333; /* Abu-abu Gelap/Arang */
    --color-accent-gold: #B89D6B; /* Emas Lembut */
    --color-secondary-green: #4A5F40; /* Hijau Zaitun Gelap (untuk Logo/Heading) */
    --color-border-light: #E0E0E0;
    --color-card-background: #F9F9F9; /* Off-white untuk kartu */
}

/* Dark Mode Override */
.dark-theme {
    --color-background-light: #1F2937; /* Biru Tua Malam */
    --color-text-dark: #E0E0E0; /* Abu-abu Muda untuk kontras */
    --color-border-light: #374151;
    --color-card-background: #2D3748; /* Warna kartu sedikit lebih terang dari background */
}

/* --- 2. Gaya Dasar dan Reset --- */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif; 
    line-height: 1.6;
    color: var(--color-text-dark);
    background-color: var(--color-background-light);
    transition: background-color 0.4s ease-in-out, color 0.4s ease-in-out; /* Transisi lembut */
}

a {
    text-decoration: none;
    color: var(--color-text-dark);
    transition: color 0.3s;
}

a:hover {
    color: var(--color-accent-gold);
}

/* --- 3. Header & Navigasi (Modern & Elegan) --- */
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem 5%;
    border-bottom: 1px solid var(--color-border-light);
    position: sticky;
    top: 0;
    z-index: 1000;
    background-color: var(--color-background-light);
    box-shadow: 0 1px 5px rgba(0, 0, 0, 0.05);
}

.dark-theme header {
    box-shadow: 0 1px 5px rgba(255, 255, 255, 0.05);
}

.logo {
    font-size: 1.6rem;
    font-weight: 700;
    letter-spacing: 1px;
    color: var(--color-secondary-green);
}

nav a {
    margin: 0 1.5rem;
    font-weight: 500;
    position: relative;
    padding-bottom: 5px;
}

nav a::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 0;
    height: 2px;
    background-color: var(--color-accent-gold);
    transition: width 0.3s;
}

nav a:hover::after {
    width: 100%;
}

.controls .control-btn {
    background: none;
    border: 1px solid var(--color-border-light);
    color: var(--color-text-dark);
    padding: 0.5rem 0.75rem;
    margin-left: 0.5rem;
    cursor: pointer;
    font-size: 1rem;
    border-radius: 4px;
    transition: background-color 0.3s, color 0.3s;
}

.controls .control-btn:hover {
    background-color: var(--color-border-light);
}

/* --- 4. Hero Section (Banner Utama) --- */
.hero {
    min-height: 75vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 5rem 5%;
    /* Gunakan overlay warna untuk mempertahankan elegansi, tidak langsung gambar */
    background: linear-gradient(rgba(255, 255, 255, 0.9), rgba(255, 255, 255, 0.9)), url('placeholder_banner.jpg') no-repeat center center/cover;
    transition: background 0.4s;
}

.dark-theme .hero {
    background: linear-gradient(rgba(31, 41, 55, 0.8), rgba(31, 41, 55, 0.8)), url('placeholder_banner.jpg') no-repeat center center/cover;
}

.hero h1 {
    font-size: 3.5rem;
    margin-bottom: 1rem;
    font-weight: 300; 
    color: var(--color-secondary-green);
}

.hero p {
    font-size: 1.35rem;
    margin-bottom: 2.5rem;
    max-width: 700px;
    opacity: 0.8;
}

.cta-button {
    background-color: var(--color-accent-gold);
    color: white; /* Kontras tinggi */
    padding: 1rem 2.5rem;
    border-radius: 5px;
    font-weight: 600;
    letter-spacing: 0.5px;
    box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
    transition: transform 0.3s, background-color 0.3s, box-shadow 0.3s;
}

.cta-button:hover {
    transform: translateY(-3px);
    background-color: #A38A5C;
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
}

/* --- 5. Product & About Sections --- */
section {
    padding: 6rem 5%;
}

h2 {
    font-size: 2.5rem;
    text-align: center;
    margin-bottom: 4rem;
    font-weight: 400;
    color: var(--color-secondary-green);
}

.product-highlight {
    background-color: var(--color-card-background); 
}

.product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 3rem;
    max-width: 1200px;
    margin: 0 auto;
}

.product-card {
    background-color: var(--color-background-light);
    padding: 2rem;
    border-radius: 12px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
    text-align: center;
    transition: transform 0.4s cubic-bezier(0.25, 0.8, 0.25, 1), box-shadow 0.4s; /* Animasi elegan */
    border: 1px solid var(--color-border-light);
}

.product-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
}

.product-card img {
    width: 100%;
    height: 250px;
    object-fit: cover;
    border-radius: 8px;
    margin-bottom: 1.5rem;
}

.product-card h3 {
    color: var(--color-secondary-green);
    margin-bottom: 0.75rem;
    font-weight: 600;
}

.product-card p {
    opacity: 0.7;
    margin-bottom: 1rem;
}

.product-card a {
    display: inline-block;
    color: var(--color-accent-gold);
    font-weight: 600;
    border-bottom: 2px solid transparent;
}

.product-card a:hover {
    border-bottom: 2px solid var(--color-accent-gold);
}

.about-us {
    text-align: center;
    max-width: 900px;
    margin: 0 auto;
}

.about-us p {
    font-size: 1.15rem;
    line-height: 1.8;
}

/* --- 6. Footer --- */
footer {
    padding: 2rem 5%;
    text-align: center;
    font-size: 0.9rem;
    border-top: 1px solid var(--color-border-light);
    opacity: 0.7;
    background-color: var(--color-card-background);
}

/* --- 7. Responsif Sederhana --- */
@media (max-width: 900px) {
    .hero h1 {
        font-size: 2.5rem;
    }
}

@media (max-width: 768px) {
    header {
        flex-direction: column;
        padding: 1rem 5%;
    }

    nav {
        margin-top: 1rem;
    }
    
    .controls {
        margin-top: 1rem;
    }
    
    .hero {
        min-height: 50vh;
    }

    h2 {
        font-size: 2rem;
        margin-bottom: 3rem;
    }
}

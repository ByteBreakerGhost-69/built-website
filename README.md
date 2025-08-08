      <!DOCTYPE html>
      <html lang="id">
      <head>
          <meta charset="UTF-8">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <title>ByteBreakerGhost-69</title>
          <meta name="description" content="Portofolio profesional Maulana Yasyfa'u Al Azhiim Yudho Leksono - Web Developer & Ethical Hacker lulusan SMP/SMA Islam Plus Hidayatut Thullab">
          <script src="https://cdn.tailwindcss.com"></script>
          <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
          <style>
              :root {
                  --dark-blue: #13406d;
                  --black: #0a0a0a;
                  --accent: #4A90E2;
              }
              
              /* ===== SPLASH SCREEN ===== */
              .splash-screen {
                  position: fixed;
                  top: 0;
                  left: 0;
                  width: 100%;
                  height: 100%;
                  background: linear-gradient(135deg, var(--dark-blue) 0%, var(--black) 100%);
                  display: flex;
                  flex-direction: column;
                  justify-content: center;
                  align-items: center;
                  z-index: 9999;
                  transition: opacity 0.5s ease;
              }
      
              .splash-content {
                  display: flex;
                  flex-direction: column;
                  align-items: center;
                  width: 100%;
                  max-width: 1200px;
                  padding: 0 20px;
              }
      
              .splash-logo {
                  font-size: 3rem;
                  font-weight: 700;
                  margin-bottom: 2rem;
                  position: relative;
                  overflow: hidden;
                  white-space: nowrap;
                  border-right: 3px solid var(--accent);
                  animation: typing 8s steps(80, end), blink-caret 0.75s step-end infinite;
              }
      
              .characters-container {
                  display: flex;
                  justify-content: space-between;
                  align-items: center;
                  width: 100%;
                  position: relative;
                  margin: 3rem 0;
              }
      
              .human-character {
                  width: 250px;
                  animation: float 4s ease-in-out infinite;
                  transform: translateX(-50px);
                  opacity: 0;
                  animation: 
                      fadeInLeft 1s ease-out forwards,
                      float 4s ease-in-out 1s infinite;
              }
      
              .robot-character {
                  width: 250px;
                  animation: float 4s ease-in-out infinite 0.5s;
                  transform: translateX(50px);
                  opacity: 0;
                  animation: 
                      fadeInRight 1s ease-out forwards,
                      float 4s ease-in-out 1.5s infinite;
              }
      
              .connecting-line {
                  position: absolute;
                  top: 50%;
                  left: 50%;
                  transform: translate(-50%, -50%);
                  width: 60%;
                  height: 2px;
                  background: linear-gradient(90deg, transparent, var(--accent), transparent);
                  animation: pulse-line 2s ease-in-out infinite;
              }
      
              .loading-bar {
                  width: 300px;
                  height: 6px;
                  background: rgba(46, 17, 126, 0.2);
                  border-radius: 3px;
                  overflow: hidden;
                  margin-top: 2rem;
              }
      
              .loading-progress {
                  height: 100%;
                  background: var(--accent);
                  width: 0;
                  animation: loading 5s ease-in-out forwards;
              }
      
              /* Animasi Khusus Splash */
              @keyframes fadeInLeft {
                  from { opacity: 0; transform: translateX(-50px); }
                  to { opacity: 1; transform: translateX(0); }
              }
      
              @keyframes fadeInRight {
                  from { opacity: 0; transform: translateX(50px); }
                  to { opacity: 1; transform: translateX(0); }
              }
      
              @keyframes pulse-line {
                  0%, 100% { width: 60%; opacity: 0.7; }
                  50% { width: 80%; opacity: 1; }
              }
      
              @keyframes loading {
                  from { width: 0; }
                  to { width: 100%; }
              }
      
              .main-content {
                  display: none;
              }
      
      
              body {
                  font-family: 'Poppins', sans-serif;
                  background-color: var(--black);
                  color: white;
                  overflow-x: hidden;
              }
          
              .bg-dark-blue {
                  background-color: var(--dark-blue);
              }
              
              .bg-gradient-dark {
                  background: linear-gradient(135deg, var(--dark-blue) 0%, var(--black) 100%);
              }
              
              .hover-scale {
                  transition: transform 0.3s ease;
              }
              
              .hover-scale:hover {
                  transform: scale(1.05);
              }
          
              @keyframes float {
                  0%, 100% {
                      transform: translateY(0);
                  }
                  50% {
                      transform: translateY(-10px);
                  }
              }
          
              .floating {
                  animation: float 6s ease-in-out infinite;
              }
          
              .skill-bar {
                  height: 6px;
                  background-color: rgba(255,255,255,0.2);
                  border-radius: 3px;
                  overflow: hidden;
              }
          
              .skill-progress {
                  height: 100%;
                  background-color: var(--accent);
                  animation: progress-animation 2s ease-in-out forwards;
              }
              
              @keyframes progress-animation {
                  0% { width: 0; }
                  100% { width: var(--progress); }
              }
              
              .navbar {
                  backdrop-filter: blur(10px);
                  -webkit-backdrop-filter: blur(10px);
              }
              
              .pulsing {
                  animation: pulse 2s infinite;
              }
          
              @keyframes pulse {
                  0% {
                      box-shadow: 0 0 0 0 rgba(74, 144, 226, 0.7);
                  }
                  70% {
                      box-shadow: 0 0 0 10px rgba(74, 144, 226, 0);
                  }
                  100% {
                      box-shadow: 0 0 0 0 rgba(74, 144, 226, 0);
                  }
              }
          
              .stars {
                  position: fixed;
                  top: 0;
                  left: 0;
                  width: 100%;
                  height: 100%;
                  z-index: -1;
                  pointer-events: none;
              }
          
              .star {
                  position: absolute;
                  background-color: white;
                  border-radius: 50%;
                  animation: twinkle var(--duration) infinite ease-in-out;
                  opacity: var(--opacity);
              }
              
              @keyframes twinkle {
                  0%, 100% { opacity: var(--opacity); }
                  50% { opacity: calc(var(--opacity) * 0.3); }
              }
              
              /* ===== ANIMASI SLIDER TOOLS ===== */
              .tools-slider-container {
                  overflow: hidden;
                  white-space: nowrap;
                  position: relative;
              }
      
              .tools-slider-track {
                  display: inline-block;
                  animation: slideLoop 20s linear infinite;
              }
      
              .tools-slider-track:hover {
                  animation-play-state: paused;
              }
      
              @keyframes slideLoop {
                  0% { transform: translateX(0); }
                  100% { transform: translateX(-50%); } /* Geser ke kiri setengah panjang total */
              }
              /* Efek item tool */
              .tool-item {
                  background: rgba(28, 16, 73, 0.5);
                  border: 1px solid rgba(39, 18, 95, 0.2);
                  border-radius: 8px;
                  padding: 15px;
                  min-width: 120px;
                  text-align: center;
                  transition: all 0.3s ease;
              }
      
              .tool-item:hover {
                  transform: scale(1.05);
                  border-color: rgba(74, 144, 226, 0.5);
                  box-shadow: 0 0 15px rgba(74, 144, 226, 0.3);
              }
      
              .tool-item img {
                  width: 48px;
                  height: 48px;
                  margin: 0 auto 10px;
                  filter: grayscale(100%);
                  transition: filter 0.3s ease;
              }
      
              .tool-item:hover img {
                  filter: grayscale(0);
              }
      
              /* Responsif untuk mobile */
              @media (max-width: 768px) {
                  .tools-slider-track {
                      animation: none;
                      overflow-x: auto;
                      padding-bottom: 15px;
                  }
              }
      
              /* Typing effect styles */
              #typing-text {
                  border-right: 2px solid #4A90E2;
                  white-space: nowrap;
                  overflow: hidden;
                  display: inline-block;
                  min-height: 1.2em;
              }
      
              #typing-text.finished-typing {
                  border-right: none;
              }
      
             /* Efek ketik dengan kursor yang hilang setelah selesai */
              .typing-effect {
                  overflow: hidden;
                  white-space: nowrap;
                  position: relative;
                  border-right: 2px solid transparent; /* Awalnya transparan */
                  animation: 
                      typing 3.5s steps(40, end) forwards,
                      blink-caret .75s step-end 4.6667s; /* Sesuaikan dengan durasi typing */
              }
      
              @keyframes typing {
                  from { width: 0 }
                  to { width: 100% }
              }
      
              @keyframes blink-caret {
                  from, to { border-color: transparent }
                  50% { border-color: #4A90E2; }
              }
      
                      /* SPLASH SCREEN FIXED */
              .splash-screen {
                  position: fixed;
                  top: 0;
                  left: 0;
                  width: 100%;
                  height: 100%;
                  background: linear-gradient(135deg, var(--dark-blue) 0%, var(--black) 100%);
                  display: flex;
                  justify-content: center;
                  align-items: center;
                  z-index: 9999;
                  opacity: 1;
                  transition: opacity 2.5s ease;
              }
      
              .main-content {
                  display: none;
              }
      
              /* ANIMASI TYPING FIX */
              .splash-logo {
                  font-size: 3rem;
                  font-weight: 700;
                  color: white;
                  overflow: hidden;
                  white-space: nowrap;
                  border-right: 3px solid var(--accent);
                  animation: 
                      typing 2s steps(40, end) forwards,
                      blink-caret 0.75s step-end infinite;
              }
      
              /* KARAKTER ANIMASI */
              .human-character {
                  width: 250px;
                  animation: 
                      fadeInLeft 1s ease-out forwards,
                      float 4s ease-in-out 1s infinite;
              }
      
              .robot-character {
                  width: 250px;
                  animation: 
                      fadeInRight 1s ease-out forwards,
                      float 4s ease-in-out 1.5s infinite;
              }
      
              /* KEYFRAMES BARU */
              @keyframes fadeInLeft {
                  from { opacity: 0; transform: translateX(-50px); }
                  to { opacity: 1; transform: translateX(0); }
              }
      
              @keyframes fadeInRight {
                  from { opacity: 0; transform: translateX(50px); }
                  to { opacity: 1; transform: translateX(0); }
              }
      
      
          </style>
      </head>
      
      <script>
          document.addEventListener('DOMContentLoaded', function() {
              // Typing effect
              const text = "Web Developer & Ethical Hacker";
              const typingElement = document.getElementById('typing-text');
              let i = 0;
              
              function typeWriter() {
                  if (i < text.length) {
                      typingElement.innerHTML += text.charAt(i);
                      i++;
                      setTimeout(typeWriter, 150); // Kecepatan ketik (ms)
                  } else {
                      // Setelah selesai, tambahkan kursor yang berkedip
                      typingElement.classList.add('finished-typing');
                  }
              }
              
              // Mulai efek ketik setelah halaman dimuat
              setTimeout(typeWriter, 1500);
          });
      </script>
      
      <body>
      <!-- Splash Screen -->
      <div class="splash-screen" id="splashScreen">
          <div class="splash-content">
              <div class="splash-logo" id="splashLogo"></div>
              
              <div class="characters-container">
                  <img src="https://i.postimg.cc/JnTH0Wmr/Whats-App-Image-2025-08-07-at-23-32-28.jpg" alt="Foto Profil" class="human-character">
                  <div class="connecting-line"></div>
                  <img src="https://i.postimg.cc/CLLtpkLT/CEO-square.jpg" alt="Robot AI" class="robot-character">
              </div>
              
              <div class="loading-bar">
                  <div class="loading-progress"></div>
              </div>
          </div>
      </div>
      
      <!-- Konten Utama -->
      <div class="main-content">
          <!-- Semua konten website yang ada -->
      </div>
      <!-- Floating Stars Background -->
      <div id="stars-container" class="stars"></div>
      
          <!-- Floating Stars Background -->
          <div id="stars-container" class="stars"></div>
          
          <!-- Navigation -->
          <nav class="navbar fixed w-full bg-black bg-opacity-80 z-50">
              <div class="container mx-auto px-6 py-4">
                  <div class="flex items-center justify-between">
                      <a href="#" class="text-2xl font-bold text-white hover:text-blue-400 transition">my website</a>
                      <div class="hidden md:flex space-x-8">
                          <a href="#home" class="text-white hover:text-blue-400 transition">Home</a>
                          <a href="#about" class="text-white hover:text-blue-400 transition">Tentang</a>
                          <a href="#skills" class="text-white hover:text-blue-400 transition">Keahlian</a>
                          <a href="#portfolio" class="text-white hover:text-blue-400 transition">Portofolio</a>
                          <a href="#contact" class="text-white hover:text-blue-400 transition">Kontak</a>
                      </div>
                      <button class="md:hidden text-white focus:outline-none">
                          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
                          </svg>
                      </button>
                  </div>
              </div>
          </nav>
      
          <!-- Hero Section -->
          <section id="home" class="min-h-screen flex items-center justify-center bg-gradient-dark pt-20">
              <div class="container mx-auto px-6 py-12 md:py-24">
                  <div class="flex flex-col md:flex-row items-center">
                      <div class="md:w-1/2 mb-12 md:mb-0">
                          <h1 class="text-4xl md:text-6xl font-bold mb-4">Maulana Yasyfa'u Al Azhiim Yudho Leksono</h1>
                          <h2 class="text-2xl md:text-3xl text-blue-400 mb-6 typing-effect">Web Developer & Ethical Hacker</h2>
                          <p class="text-lg mb-8 opacity-90">Mahir dalam membangun website modern dan sistem keamanan siber yang kokoh.</p>
                          <div class="flex space-x-4">
                              <a href="#contact" class="bg-blue-500 hover:bg-blue-600 text-white px-6 py-3 rounded-full font-medium transition-all transform hover:scale-105 shadow-lg">
                                  Hubungi Saya
                              </a>
                              <a href="#portfolio" class="border border-blue-400 text-blue-400 hover:bg-blue-400 hover:text-black px-6 py-3 rounded-full font-medium transition-all transform hover:scale-105">
                                  Lihat Portofolio
                              </a>
                          </div>
                      </div>
                      <div class="md:w-1/2 flex justify-center">
                          <div class="relative floating">
                              <img src="https://placehold.co/400x450" alt="Potret profesional Maulana Yasyfa'u Al Azhiim dengan latar belakang modern" class="rounded-lg shadow-2xl border-2 border-blue-400">
                              <div class="absolute -bottom-5 -right-5 bg-blue-500 text-white px-4 py-2 rounded-full shadow-lg">
                                  Web & Security Expert
                              </div>
                          </div>
                      </div>
                  </div>
              </div>
          </section>
      
          <!-- About Section -->
          <section id="about" class="py-20 bg-black">
              <div class="container mx-auto px-6">
                  <h2 class="text-3xl md:text-4xl font-bold text-center mb-16 text-white">Tentang Saya</h2>
                  
                  <div class="flex flex-col md:flex-row items-center">
                      <div class="md:w-1/3 mb-8 md:mb-0 flex justify-center">
                          <img src="https://placehold.co/300x300" alt="Foto formal Maulana Yasyfa'u Al Azhiim dengan pakaian profesional" class="rounded-full border-4 border-blue-400 w-64 h-64 object-cover">
                      </div>
                      <div class="md:w-2/3 md:pl-12">
                          <h3 class="text-2xl font-bold mb-4 text-blue-400">Profil Profesional</h3>
                          <p class="mb-6 text-lg">
                              Saya adalah seorang profesional di bidang pengembangan web dan keamanan siber, lulusan dari SMP dan SMA Islam Plus Hidayatut Thullab. 
                              Dengan keterampilan teknis yang mendalam dan pemahaman yang kuat tentang teknologi terbaru, saya dapat memberikan solusi digital yang inovatif dan aman.
                          </p>
                          
                          <h3 class="text-2xl font-bold mb-4 text-blue-400">Pendidikan</h3>
                          <div class="space-y-4 mb-8">
                              <div class="flex items-start">
                                  <div class="bg-blue-500 rounded-full p-2 mr-4 mt-1">
                                      <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path>
                                      </svg>
                                  </div>
                                  <div>
                                      <h4 class="font-bold">SMA Islam Plus Hidayatut Thullab</h4>
                                      <p class="text-gray-300">Lulus dengan fokus pada matematika dan teknologi</p>
                                  </div>
                              </div>
                              <div class="flex items-start">
                                  <div class="bg-blue-500 rounded-full p-2 mr-4 mt-1">
                                      <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path>
                                      </svg>
                                  </div>
                                  <div>
                                      <h4 class="font-bold">SMP Islam Plus Hidayatut Thullab</h4>
                                      <p class="text-gray-300">Dasar pendidikan teknologi dan pemrograman</p>
                                  </div>
                              </div>
                          </div>
                          
                          <div class="bg-dark-blue p-6 rounded-lg shadow-lg">
                              <h3 class="text-2xl font-bold mb-4 text-blue-400">Filosofi Kerja</h3>
                              <p class="italic text-lg">"Dalam setiap kode yang saya tulis dan setiap sistem yang saya amankan, saya selalu berusaha untuk menyertakan nilai-nilai kejujuran, etika profesional, dan komitmen untuk memberikan yang terbaik."</p>
                          </div>
                      </div>
                  </div>
              </div>
          </section>
      
          <!-- Skills Section -->
          <section id="skills" class="py-20 bg-gradient-dark">
              <div class="container mx-auto px-6">
                  <h2 class="text-3xl md:text-4xl font-bold text-center mb-16 text-white">Keahlian</h2>
                  
                  <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                      <div class="bg-black bg-opacity-50 p-8 rounded-lg shadow-lg hover-scale">
                          <div class="flex items-center mb-4">
                              <div class="bg-blue-500 p-3 rounded-full mr-4">
                                  <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"></path>
                                  </svg>
                              </div>
                              <h3 class="text-2xl font-bold text-blue-400">Web Development</h3>
                          </div>
                          <div class="space-y-4">
                              <div>
                                  <p class="mb-1">HTML</p>
                                  <div class="skill-bar">
                                      <div class="skill-progress" style="--progress:95%"></div>
                                  </div>
                              </div>
                              <div>
                                  <p class="mb-1">CSS</p>
                                  <div class="skill-bar">
                                      <div class="skill-progress" style="--progress:85%"></div>
                                  </div>
                              </div>
                              <div>
                                  <p class="mb-1">JAVASCRIPT</p>
                                  <div class="skill-bar">
                                      <div class="skill-progress" style="--progress:90%"></div>
                                  </div>
                              </div>
                              <div>
                                  <p class="mb-1">MongoDB & MySQL</p>
                                  <div class="skill-bar">
                                      <div class="skill-progress" style="--progress:80%"></div>
                                  </div>
                              </div>
                          </div>
                      </div>
                      
                      <div class="bg-black bg-opacity-50 p-8 rounded-lg shadow-lg hover-scale">
                          <div class="flex items-center mb-4">
                              <div class="bg-blue-500 p-3 rounded-full mr-4">
                                  <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"></path>
                                  </svg>
                              </div>
                              <h3 class="text-2xl font-bold text-blue-400">Ethical Hacking</h3>
                          </div>
                          <div class="space-y-4">
                              <div>
                                  <p class="mb-1">Penetration Testing</p>
                                  <div class="skill-bar">
                                      <div class="skill-progress" style="--progress:90%"></div>
                                  </div>
                              </div>
                              <div>
                                  <p class="mb-1">Vulnerability Assessment</p>
                                  <div class="skill-bar">
                                      <div class="skill-progress" style="--progress:85%"></div>
                                  </div>
                              </div>
                              <div>
                                  <p class="mb-1">Network Security</p>
                                  <div class="skill-bar">
                                      <div class="skill-progress" style="--progress:88%"></div>
                                  </div>
                              </div>
                              <div>
                                  <p class="mb-1">Security Auditing</p>
                                  <div class="skill-bar">
                                      <div class="skill-progress" style="--progress:82%"></div>
                                  </div>
                              </div>
                          </div>
                      </div>
                  </div>
                  
                  <!-- ===== SLIDER TOOLS ===== -->
        <div class="mt-12 relative overflow-hidden py-6">
          <div class="tools-slider-container">
              <div class="tools-slider-track">
                  <!-- Original Tools Row -->
                  <div class="flex gap-8 shrink-0">
                      <!-- HTML5 -->
                      <div class="bg-black/50 p-4 rounded-lg text-center min-w-[120px] border border-blue-400/20 hover:border-blue-400/50">
                          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML5" class="w-12 h-12 mx-auto mb-2">
                          <p class="font-mono text-sm">HTML</p>
                      </div>
                      <div class="bg-black/50 p-4 rounded-lg text-center min-w-[120px] border border-blue-400/20 hover:border-blue-400/50">
                          <img src="https://i.postimg.cc/DzzY55Gp/download-css.png" alt="CSS3" class="w-12 h-12 mx-auto mb-2">
                          <p class="font-mono text-sm">CSS</p>
                      </div>
                      <div class="bg-black/50 p-4 rounded-lg text-center min-w-[120px] border border-blue-400/20 hover:border-blue-400/50">
                          <img src="https://i.postimg.cc/nLcc2808/images-javascript.png" alt="JavaScript" class="w-12 h-12 mx-auto mb-2">
                          <p class="font-mono text-sm">JavaScript</p>
                      </div>
                      <div class="bg-black/50 p-4 rounded-lg text-center min-w-[120px] border border-blue-400/20 hover:border-blue-400/50">
                          <img src="https://i.postimg.cc/rm46CQXX/images.png" alt="Kali Linux" class="w-12 h-12 mx-auto mb-2">
                          <p class="font-mono text-sm">Kali Linux</p>
                      </div>
                      <div class="bg-black/50 p-4 rounded-lg text-center min-w-[120px] border border-blue-400/20 hover:border-blue-400/50">
                          <img src="https://i.postimg.cc/P5w42cVq/0-Fp841-N-400x400-blackarch-linux.jpg" alt="BlackArch Linux" class="w-12 h-12 mx-auto mb-2">
                          <p class="font-mono text-sm">BlackArch Linux</p>
                      </div>
                      <div class="bg-black/50 p-4 rounded-lg text-center min-w-[120px] border border-blue-400/20 hover:border-blue-400/50">
                          <img src="https://i.postimg.cc/MGG1gFdR/imagesnmap.jpg" alt="nmap" class="w-12 h-12 mx-auto mb-2">
                          <p class="font-mono text-sm">nmap</p>
                      </div>
                      <div class="bg-black/50 p-4 rounded-lg text-center min-w-[120px] border border-blue-400/20 hover:border-blue-400/50">
                          <img src="https://i.postimg.cc/x1wsQYNH/images-msfconsole.png" alt="metasploit" class="w-12 h-12 mx-auto mb-2">
                          <p class="font-mono text-sm">metasploit</p>
                      </div>
                      <div class="bg-black/50 p-4 rounded-lg text-center min-w-[120px] border border-blue-400/20 hover:border-blue-400/50">
                          <img src="https://i.postimg.cc/4NtP1qSx/images-brup-suite.jpg" alt="burpsuite" class="w-12 h-12 mx-auto mb-2">
                          <p class="font-mono text-sm">burpsuite</p>
                      </div>
                      <div class="bg-black/50 p-4 rounded-lg text-center min-w-[120px] border border-blue-400/20 hover:border-blue-400/50">
                          <img src="https://i.postimg.cc/qMyRMxzF/images-commix.png" alt="commix" class="w-12 h-12 mx-auto mb-2">
                          <p class="font-mono text-sm">commix</p>
                      </div>
                      <div class="bg-black/50 p-4 rounded-lg text-center min-w-[120px] border border-blue-400/20 hover:border-blue-400/50">
                          <img src="https://i.postimg.cc/J4f1fDxQ/images-sqlmap.png" alt="sqlmap" class="w-12 h-12 mx-auto mb-2">
                          <p class="font-mono text-sm">sqlmap</p>
                      </div>
                      <div class="bg-black/50 p-4 rounded-lg text-center min-w-[120px] border border-blue-400/20 hover:border-blue-400/50">
                          <img src="https://i.postimg.cc/Mp7Bc8r1/images-john.png" alt="john the ripper" class="w-12 h-12 mx-auto mb-2">
                          <p class="font-mono text-sm">john the ripper</p>
                      </div>
                      <div class="bg-black/50 p-4 rounded-lg text-center min-w-[120px] border border-blue-400/20 hover:border-blue-400/50">
                          <img src="https://i.postimg.cc/L6ZLpPtC/1-xf-3-MVfi-o-Xhw7-B-ywh5-WQ-hydra.jpg" alt="hydra" class="w-12 h-12 mx-auto mb-2">
                          <p class="font-mono text-sm">hydra</p>
                      </div>
                      <div class="bg-black/50 p-4 rounded-lg text-center min-w-[120px] border border-blue-400/20 hover:border-blue-400/50">
                          <img src="https://i.postimg.cc/7Yw2M5Ff/st-small-507x507-pad-600x600-f8f8f8-u4.jpg" alt="wireshark" class="w-12 h-12 mx-auto mb-2">
                          <p class="font-mono text-sm">wireshark</p>
                      </div>
                  </div>
              </div>
          </div>
      </div>
                 
          <!-- Portfolio Section -->
          <section id="portfolio" class="py-20 bg-black">
              <div class="container mx-auto px-6">
                  <h2 class="text-3xl md:text-4xl font-bold text-center mb-16 text-white">Portofolio</h2>
                  
                  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                      <div class="bg-dark-blue rounded-lg overflow-hidden shadow-lg hover-scale">
                          <div class="relative">
                              <img src="https://placehold.co/600x400" alt="Tampilan website e-commerce dengan dashboard admin" class="w-full h-48 object-cover">
                              <div class="absolute top-2 right-2 bg-blue-500 text-white px-2 py-1 rounded text-sm">
                                  Web Development
                              </div>
                          </div>
                          <div class="p-6">
                              <h3 class="text-xl font-bold mb-2">Sistem E-Commerce</h3>
                              <p class="text-gray-300 mb-4">Membangun platform e-commerce lengkap dengan dashboard admin, sistem pembayaran, dan manajemen produk.</p>
                              <div class="flex flex-wrap gap-2 mb-4">
                                  <span class="bg-blue-500 bg-opacity-20 text-blue-400 px-2 py-1 rounded-full text-xs">React</span>
                                  <span class="bg-blue-500 bg-opacity-20 text-blue-400 px-2 py-1 rounded-full text-xs">Node.js</span>
                                  <span class="bg-blue-500 bg-opacity-20 text-blue-400 px-2 py-1 rounded-full text-xs">MongoDB</span>
                              </div>
                              <a href="#" class="text-blue-400 hover:text-blue-300 font-medium inline-flex items-center">Lihat Detail 
                                  <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path>
                                  </svg>
                              </a>
                          </div>
                      </div>
                      
                      <div class="bg-dark-blue rounded-lg overflow-hidden shadow-lg hover-scale">
                          <div class="relative">
                              <img src="https://placehold.co/600x400" alt="Tampilan dashboard keamanan jaringan dengan analisis real-time" class="w-full h-48 object-cover">
                              <div class="absolute top-2 right-2 bg-red-500 text-white px-2 py-1 rounded text-sm">
                                  Security
                              </div>
                          </div>
                          <div class="p-6">
                              <h3 class="text-xl font-bold mb-2">Security Monitoring System</h3>
                              <p class="text-gray-300 mb-4">Sistem monitoring keamanan jaringan real-time dengan deteksi anomaly dan peringatan otomatis.</p>
                              <div class="flex flex-wrap gap-2 mb-4">
                                  <span class="bg-blue-500 bg-opacity-20 text-blue-400 px-2 py-1 rounded-full text-xs">Python</span>
                                  <span class="bg-blue-500 bg-opacity-20 text-blue-400 px-2 py-1 rounded-full text-xs">Elasticsearch</span>
                                  <span class="bg-blue-500 bg-opacity-20 text-blue-400 px-2 py-1 rounded-full text-xs">Kibana</span>
                              </div>
                              <a href="#" class="text-blue-400 hover:text-blue-300 font-medium inline-flex items-center">Lihat Detail 
                                  <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path>
                                  </svg>
                              </a>
                          </div>
                      </div>
                      
                      <div class="bg-dark-blue rounded-lg overflow-hidden shadow-lg hover-scale">
                          <div class="relative">
                              <img src="https://placehold.co/600x400" alt="Antarmukan aplikasi mobile dengan desain minimalis" class="w-full h-48 object-cover">
                              <div class="absolute top-2 right-2 bg-blue-500 text-white px-2 py-1 rounded text-sm">
                                  Mobile App
                              </div>
                          </div>
                          <div class="p-6">
                              <h3 class="text-xl font-bold mb-2">Aplikasi Edukasi Keamanan Siber</h3>
                              <p class="text-gray-300 mb-4">Aplikasi edukasi berbasis mobile tentang praktik keamanan siber untuk pemula.</p>
                              <div class="flex flex-wrap gap-2 mb-4">
                                  <span class="bg-blue-500 bg-opacity-20 text-blue-400 px-2 py-1 rounded-full text-xs">Flutter</span>
                                  <span class="bg-blue-500 bg-opacity-20 text-blue-400 px-2 py-1 rounded-full text-xs">Firebase</span>
                                  <span class="bg-blue-500 bg-opacity-20 text-blue-400 px-2 py-1 rounded-full text-xs">Dart</span>
                              </div>
                              <a href="#" class="text-blue-400 hover:text-blue-300 font-medium inline-flex items-center">Lihat Detail 
                                  <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path>
                                  </svg>
                              </a>
                          </div>
                      </div>
                  </div>
                  
                  <div class="text-center mt-12">
                      <a href="#" class="inline-flex items-center text-blue-400 hover:text-blue-300 font-medium">
                          Lihat Selengkapnya
                          <svg class="w-4 h-4 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path>
                          </svg>
                      </a>
                  </div>
              </div>
          </section>
      
          <!-- Contact Section -->
          <!DOCTYPE html>
      <html lang="id">
      <head>
          <meta charset="UTF-8">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <title>Kontak Saya</title>
          <script src="https://cdn.tailwindcss.com"></script>
          <script>
              tailwind.config = {
                  theme: {
                      extend: {
                          colors: {
                              primary: '#001f3f',
                              secondary: '#0a0a0a',
                              accent: '#1e40af',
                          }
                      }
                  }
              }
          </script>
      </head>
      <body class="bg-gray-900">
      
          <!-- Contact Section -->
          <section id="contact" class="relative py-20 bg-gradient-to-b from-primary to-secondary z-10 overflow-visible">
              <div class="container mx-auto px-6">
                  <h2 class="text-3xl md:text-4xl font-bold text-center mb-16 text-white">Hubungi Saya</h2>
                  
                  <div class="flex flex-col lg:flex-row gap-8 bg-black bg-opacity-70 backdrop-blur-md rounded-xl shadow-2xl p-8 border border-gray-800">
                      <!-- Contact Info -->
                      <div class="lg:w-1/2 space-y-6">
                          <h3 class="text-2xl font-bold text-blue-400">Let's Collaborate</h3>
                          <p class="text-gray-300">
                              Untuk project web development atau konsultasi keamanan siber, hubungi saya melalui:
                          </p>
                          
                          <div class="space-y-6">
                              <!-- Email -->
                              <div class="flex items-start">
                                  <div class="bg-blue-500 p-2 rounded-full mr-4 mt-1 flex-shrink-0">
                                      <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                                      </svg>
                                  </div>
                                  <div>
                                      <h4 class="font-bold text-white">Email</h4>
                                      <p class="text-gray-300 hover:text-blue-400 transition-colors">
                                          <a href="mailto:admin@myayl.com">yasyfinance.9@gmail.com</a>
                                      </p>
                                  </div>
                              </div>
                              
                              <!-- Phone -->
                              <div class="flex items-start">
                                  <div class="bg-blue-500 p-2 rounded-full mr-4 mt-1 flex-shrink-0">
                                      <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path>
                                      </svg>
                                  </div>
                                  <div>
                                      <h4 class="font-bold text-white">WhatsApp</h4>
                                      <p class="text-gray-300 hover:text-blue-400 transition-colors">
                                          <a href="https://wa.me/6281234567890">+62 812-1585-3104</a>
                                      </p>
                                  </div>
                              </div>
                              
                              <!-- Location -->
                              <div class="flex items-start">
                                  <div class="bg-blue-500 p-2 rounded-full mr-4 mt-1 flex-shrink-0">
                                      <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path>
                                          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path>
                                      </svg>
                                  </div>
                                  <div>
                                      <h4 class="font-bold text-white">Lokasi</h4>
                                      <p class="text-gray-300">Kediri, Jawa Timur, Indonesia</p>
                                  </div>
                              </div>
                          </div>
                          
                          <!-- Social Media -->
                          <div class="pt-8">
                              <h4 class="font-bold text-white mb-3">Follow Me</h4>
                              <div class="flex flex-wrap gap-3">
                                  <!-- Facebook -->
                                  <a href="#" class="bg-[#1877F2] hover:bg-[#166FE5] text-white p-3 rounded-full transition-all transform hover:scale-110">
                                      <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                                          <path d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z"></path>
                                      </svg>
                                  </a>
                                  
                                  <!-- Instagram -->
                                  <a href="#" class="bg-gradient-to-r from-purple-500 to-pink-500 text-white p-3 rounded-full transition-all transform hover:scale-110">
                                      <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                                          <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zM12 16a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z"></path>
                                      </svg>
                                  </a>
                                  
                                  <!-- GitHub -->
                                  <a href="#" class="bg-gray-800 hover:bg-gray-700 text-white p-3 rounded-full transition-all transform hover:scale-110">
                                      <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                                          <path fill-rule="evenodd" clip-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"></path>
                                      </svg>
                                  </a>
                                  
                                  <!-- YouTube -->
                                  <a href="#" class="bg-[#FF0000] hover:bg-[#CC0000] text-white p-3 rounded-full transition-all transform hover:scale-110">
                                      <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                                          <path d="M23.498 6.186a3.016 3.016 0 0 0-2.122-2.136C19.505 3.545 12 3.545 12 3.545s-7.505 0-9.377.505A3.017 3.017 0 0 0 .502 6.186C0 8.07 0 12 0 12s0 3.93.502 5.814a3.016 3.016 0 0 0 2.122 2.136c1.871.505 9.376.505 9.376.505s7.505 0 9.377-.505a3.015 3.015 0 0 0 2.122-2.136C24 15.93 24 12 24 12s0-3.93-.502-5.814zM9.545 15.568V8.432L15.818 12l-6.273 3.568z"></path>
                                      </svg>
                                  </a>
                                  
                                  <!-- LinkedIn -->
                                  <a href="#" class="bg-[#2867B2] hover:bg-[#1E4B82] text-white p-3 rounded-full transition-all transform hover:scale-110">
                                      <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                                          <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"></path>
                                      </svg>
                                  </a>
                              </div>
                          </div>
                      </div>
                      
                      <!-- Contact Form -->
                      <div class="lg:w-1/2">
                          <form class="space-y-4" id="contactForm">
                              <div>
                                  <label for="name" class="block text-sm font-medium text-gray-300 mb-1">Nama Lengkap*</label>
                                  <input type="text" id="name" name="name" class="w-full px-4 py-3 bg-gray-800 border border-gray-700 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500 text-white placeholder-gray-400 transition-all" placeholder="Masukkan nama Anda" required>
                              </div>
                              
                              <div>
                                  <label for="email" class="block text-sm font-medium text-gray-300 mb-1">Email*</label>
                                  <input type="email" id="email" name="email" class="w-full px-4 py-3 bg-gray-800 border border-gray-700 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500 text-white placeholder-gray-400 transition-all" placeholder="email@contoh.com" required>
                              </div>
                              
                              <div>
                                  <label for="subject" class="block text-sm font-medium text-gray-300 mb-1">Subjek</label>
                                  <select id="subject" name="subject" class="w-full px-4 py-3 bg-gray-800 border border-gray-700 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500 text-white appearance-none">
                                      <option value="" disabled selected>Pilih subjek...</option>
                                      <option value="web">Web Development</option>
                                      <option value="security">Keamanan Siber</option>
                                      <option value="collab">Kolaborasi Project</option>
                                      <option value="other">Lainnya</option>
                                  </select>
                              </div>
                              
                              <div>
                                  <label for="message" class="block text-sm font-medium text-gray-300 mb-1">Pesan*</label>
                                  <textarea id="message" name="message" rows="4" class="w-full px-4 py-3 bg-gray-800 border border-gray-700 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500 text-white placeholder-gray-400 transition-all" placeholder="Tulis pesan Anda..." required></textarea>
                              </div>
                              
                              <button type="submit" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-medium py-3 px-6 rounded-lg transition-all duration-300 transform hover:scale-[1.02] flex items-center justify-center shadow-lg">
                                  <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                                  </svg>
                                  Kirim Pesan
                              </button>
                          </form>
                      </div>
                  </div>
              </div>
          </section>
      
          <!-- Video Section -->
          <section class="py-16 bg-gray-900">
              <div class="container mx-auto px-6">
                  <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 text-white">Video Saya</h2>
                  
                  <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                      <!-- Video 1 -->
                      <div class="bg-black bg-opacity-70 rounded-xl overflow-hidden shadow-2xl border border-gray-800">
                          <div class="aspect-w-16 aspect-h-9">
                              <iframe class="w-full h-64 md:h-80" src="https://www.youtube.com/embed/VIDEO_ID_1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                          </div>
                          <div class="p-6">
                              <h3 class="text-xl font-bold text-white mb-2">Judul Video 1</h3>
                              <p class="text-gray-300">Deskripsi singkat tentang video ini dan konten yang dibahas.</p>
                          </div>
                      </div>
                      
                      <!-- Video 2 -->
                      <div class="bg-black bg-opacity-70 rounded-xl overflow-hidden shadow-2xl border border-gray-800">
                          <div class="aspect-w-16 aspect-h-9">
                              <iframe class="w-full h-64 md:h-80" src="https://www.youtube.com/embed/VIDEO_ID_2" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                          </div>
                          <div class="p-6">
                              <h3 class="text-xl font-bold text-white mb-2">Judul Video 2</h3>
                              <p class="text-gray-300">Deskripsi singkat tentang video ini dan konten yang dibahas.</p>
                          </div>
                      </div>
                  </div>
                  
                  <!-- More Videos Button -->
                  <div class="text-center mt-12">
                      <a href="#" class="inline-flex items-center px-6 py-3 bg-blue-600 hover:bg-blue-700 text-white font-medium rounded-lg transition-all duration-300 transform hover:scale-105 shadow-lg">
                          <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 10l4.553-2.276A1 1 0 0121 8.618v6.764a1 1 0 01-1.447.894L15 14M5 18h8a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v8a2 2 0 002 2z"></path>
                          </svg>
                          Lihat Lebih Banyak Video
                      </a>
                  </div>
              </div>
          </section>
      
          <script>
              // Form submission handler
              document.getElementById('contactForm').addEventListener('submit', function(e) {
                  e.preventDefault();
                  
                  // Get form data
                  const formData = new FormData(this);
                  
                  // Here you would typically send the data to a server
                  // For demonstration, we'll just log it and show an alert
                  const formObject = {};
                  formData.forEach((value, key) => {
                      formObject[key] = value;
                  });
                  
                  console.log('Form data:', formObject);
                  alert('Pesan telah berhasil dikirim! Kami akan segera menghubungi Anda.');
                  
                  // Reset form after submission
                  this.reset();
              });
          </script>
      
      <script>
          // Splash screen transition
          window.addEventListener('load', function() {
              setTimeout(function() {
                  const splashScreen = document.getElementById('splashScreen');
                  const mainContent = document.querySelector('.main-content');
                  
                  // Fade out splash screen
                  splashScreen.style.opacity = '0';
                  
                  // Show main content after splash screen fades out
                  setTimeout(function() {
                      splashScreen.style.display = 'none';
                      document.body.style.overflow = 'auto'; // Enable scrolling
                      
                      // Show all elements with main-content class
                      document.querySelectorAll('.main-content').forEach(el => {
                          el.style.display = 'block';
                      });
                      
                      // Initialize stars background if needed
                      if(typeof initStars === 'function') initStars();
                  }, 500);
              }, 3500); // Total splash screen duration (3.5s)
          });
      </script>
      
      <script>
      // SPLASH SCREEN FUNCTION
      function initSplashScreen() {
          const splashScreen = document.getElementById('splashScreen');
          const splashLogo = document.getElementById('splashLogo');
          const mainContent = document.querySelector('.main-content');
          
          // 1. Typing animation
          const name = "Maulana Yasyfa'u Al Azhiim";
          let i = 0;
          
          function typeWriter() {
              if (i < name.length) {
                  splashLogo.textContent += name.charAt(i);
                  i++;
                  setTimeout(typeWriter, 100);
              }
          }
          
          // 2. Start animations
          typeWriter();
          
          // 3. Hide after 3.5s
          setTimeout(() => {
              splashScreen.style.opacity = '0';
              
              setTimeout(() => {
                  splashScreen.style.display = 'none';
                  mainContent.style.display = 'block';
                  
                  // Enable scrolling
                  document.body.style.overflow = 'auto';
              }, 800); // Match with CSS transition
          }, 3500);
      }
      
      // Run when DOM is ready
      document.addEventListener('DOMContentLoaded', initSplashScreen);
      </script>
      
      </body>
      
      </html>
      <!-- Footer -->
          <footer class="bg-black py-8">
              <div class="container mx-auto px-6">
                  <div class="flex flex-col md:flex-row justify-between items-center">
                      <div class="mb-4 md:mb-0">
                          <a href="#" class="text-2xl font-bold text-white hover:text-blue-400 transition">my website</a>
                          <p class="text-gray-400 mt-2">Web Developer & Ethical Hacker</p>
                      </div>
                      <div class="flex space-x-6">
                          <a href="#" class="text-gray-400 hover:text-blue-400 transition">
                              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                  <path d="M12 2C6.477 2 2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12c0-5.523-4.477-10-10-10z"></path>
                              </svg>
                          </a>
                          <a href="#" class="text-gray-400 hover:text-blue-400 transition">
                              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                  <path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84"></path>
                              </svg>
                          </a>
                          <a href="#" class="text-gray-400 hover:text-blue-400 transition">
                              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                  <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452z"></path>
                              </svg>
                          </a>
                          <a href="#" class="text-gray-400 hover:text-blue-400 transition">
                              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                  <path d="M12 0C8.74 0 8.333.015 7.053.072 5.775.132 4.905.333 4.14.63c-.789.306-1.459.717-2.126 1.384S.935 3.35.63 4.14C.333 4.905.131 5.775.072 7.053.012 8.333 0 8.74 0 12s.015 3.667.072 4.947c.06 1.277.261 2.148.558 2.913.306.788.717 1.459 1.384 2.126.667.666 1.336 1.079 2.126 1.384.766.296 1.636.499 2.913.558C8.333 23.988 8.74 24 12 24s3.667-.015 4.947-.072c1.277-.06 2.148-.262 2.913-.558.788-.306 1.459-.718 2.126-1.384.666-.667 1.079-1.335 1.384-2.126.296-.765.499-1.636.558-2.913.06-1.28.072-1.687.072-4.947s-.015-3.667-.072-4.947c-.06-1.277-.262-2.149-.558-2.913-.306-.789-.718-1.459-1.384-2.126C21.319 1.347 20.651.935 19.86.63c-.765-.297-1.636-.499-2.913-.558C15.667.012 15.26 0 12 0zm0 2.16c3.203 0 3.585.016 4.85.071 1.17.055 1.805.249 2.227.415.562.217.96.477 1.382.896.419.42.679.819.896 1.381.164.422.36 1.057.413 2.227.057 1.266.07 1.646.07 4.85s-.015 3.585-.074 4.85c-.061 1.17-.256 1.805-.421 2.227-.224.562-.479.96-.899 1.382-.419.419-.824.679-1.38.896-.42.164-1.065.36-2.235.413-1.274.057-1.649.07-4.859.07-3.211 0-3.586-.015-4.859-.074-1.171-.061-1.816-.256-2.236-.421-.569-.224-.96-.479-1.379-.899-.421-.419-.69-.824-.9-1.38-.165-.42-.359-1.065-.42-2.235-.045-1.26-.061-1.649-.061-4.844 0-3.196.016-3.586.061-4.861.061-1.17.255-1.814.42-2.234.21-.57.479-.96.9-1.381.419-.419.81-.689 1.379-.898.42-.166 1.051-.361 2.221-.421 1.275-.045 1.65-.06 4.859-.06l.045.03zm0 3.678c-3.405 0-6.162 2.76-6.162 6.162 0 3.405 2.76 6.162 6.162 6.162 3.405 0 6.162-2.76 6.162-6.162 0-3.405-2.76-6.162-6.162-6.162zM12 16c-2.21 0-4-1.79-4-4s1.79-4 4-4 4 1.79 4 4-1.79 4-4 4zm7.846-10.405c0 .795-.646 1.44-1.44 1.44-.795 0-1.44-.646-1.44-1.44 0-.794.646-1.439 1.44-1.439.793-.001 1.44.645 1.44 1.439z"></path>
                              </svg>
                          </a>
                      </div>
                  </div>
                  <div class="border-t border-gray-800 mt-8 pt-8 text-center text-gray-400">
                      <p>&copy; 2025 Maulana Yasyfa'u Al Azhiim Yudho Leksono. All rights reserved.</p>
                  </div>
              </div>
          </footer>
      
          <script>
              // Create stars for background
              function createStars() {
                  const starsContainer = document.getElementById('stars-container');
                  const starsCount = 100;
                  
                  for (let i = 0; i < starsCount; i++) {
                      const star = document.createElement('div');
                      star.classList.add('star');
                      
                      // Random size between 1-3px
                      const size = Math.random() * 2 + 1;
                      star.style.width = `${size}px`;
                      star.style.height = `${size}px`;
                      
                      // Random position
                      star.style.left = `${Math.random() * 100}%`;
                      star.style.top = `${Math.random() * 100}%`;
                      
                      // Random opacity
                      const opacity = Math.random() * 0.8 + 0.2;
                      star.style.setProperty('--opacity', opacity);
                      
                      // Random animation duration
                      const duration = Math.random() * 5 + 5;
                      star.style.setProperty('--duration', `${duration}s`);
                      
                      starsContainer.appendChild(star);
                  }
              }
              
              // Mobile menu toggle
              function setupMobileMenu() {
                  const mobileMenuButton = document.querySelector('.md\\:hidden');
                  const navLinks = document.querySelector('.hidden.md\\:flex');
                  
                  mobileMenuButton.addEventListener('click', () => {
                      navLinks.classList.toggle('hidden');
                      navLinks.classList.toggle('flex');
                      navLinks.classList.toggle('flex-col');
                      navLinks.classList.toggle('absolute');
                      navLinks.classList.toggle('top-16');
                      navLinks.classList.toggle('left-0');
                      navLinks.classList.toggle('right-0');
                      navLinks.classList.toggle('bg-black');
                      navLinks.classList.toggle('bg-opacity-90');
                      navLinks.classList.toggle('p-4');
                      navLinks.classList.toggle('space-y-4');
                      navLinks.classList.toggle('space-x-0');
                  });
              }
              
              // Smooth scrolling for anchor links
              function setupSmoothScrolling() {
                  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                      anchor.addEventListener('click', function (e) {
                          e.preventDefault();
                          
                          const targetId = this.getAttribute('href');
                          if (targetId === '#') return;
                          
                          const targetElement = document.querySelector(targetId);
                          if (targetElement) {
                              targetElement.scrollIntoView({
                                  behavior: 'smooth'
                              });
                          }
                      });
                  });
              }
              
              // Initialize all functions when DOM is loaded
              document.addEventListener('DOMContentLoaded', () => {
                  createStars();
                  setupMobileMenu();
                  setupSmoothScrolling();
              });
          </script>
      </body>
      </html>
      

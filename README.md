<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">
    <title>edu ⊕ drive & forms · live learning</title>
    <!-- Font Awesome 5 (free) -->
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.15.4/css/all.css">
    <!-- Google Font Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300..700&display=swap" rel="stylesheet">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: "Inter", sans-serif;
            background: #f7f3eb;
            color: #2f3e2c;
            line-height: 1.5;
            scroll-behavior: smooth;
            -webkit-tap-highlight-color: transparent;
        }
        .container { max-width: 1200px; margin: 0 auto; padding: 0 20px; }

        /* navbar */
        .navbar {
            background: #2c4a3b;
            padding: 12px 0;
            box-shadow: 0 6px 18px rgba(30, 50, 30, 0.2);
            position: sticky;
            top: 0;
            z-index: 10;
        }
        .nav-container {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 8px;
        }
        .logo {
            font-weight: 700; font-size: 1.6rem; letter-spacing: -0.02em;
            color: #f5e7d3;
        }
        .logo span { color: #f3b33d; }
        .nav-actions {
            display: flex;
            gap: 12px;
            align-items: center;
        }
        .whatsapp-header {
            background: #25D366;
            color: #111;
            border: none;
            border-radius: 40px;
            padding: 8px 16px;
            font-weight: 600;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 6px;
            white-space: nowrap;
            cursor: pointer;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: 0.2s;
        }
        .whatsapp-header i { font-size: 1.2rem; }
        .whatsapp-header:hover { background: #20b859; }
        .phone-header {
            background: #f3b33d;
            color: #2c4a3b;
            border: none;
            border-radius: 40px;
            padding: 8px 16px;
            font-weight: 600;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 6px;
            white-space: nowrap;
            cursor: pointer;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: 0.2s;
        }
        .phone-header i { font-size: 1rem; }
        .phone-header:hover { background: #e09f2c; }

        .hero {
            background: linear-gradient(145deg, #f1e3d3 0%, #faf4e9 80%);
            padding: 40px 0;
        }
        .hero-grid {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }
        .hero-content h1 {
            font-size: 2.2rem;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 20px;
            color: #2d4d3a;
        }
        .hero-content .highlight { color: #b6582c; border-bottom: 4px solid #f1c7b0; }
        .hero-content p { font-size: 1.1rem; color: #3f4d3c; margin-bottom: 28px; }
        .btn-primary {
            background: #b6582c; border: none; padding: 14px 28px; border-radius: 60px;
            font-weight: 600; font-size: 1.1rem; color: white; box-shadow: 0 10px 18px -8px #8b4e2e;
            cursor: pointer; transition: 0.2s; width: 100%; max-width: 280px;
        }
        .hero-stats {
            display: flex; gap: 24px; margin-top: 30px; flex-wrap: wrap;
        }
        /* Hero image replaced with Google Drive image via direct link (fits as background) */
        .hero-image {
            min-height: 600px;
            min-width: 100%;
            background: url('https://drive.google.com/thumbnail?id=1y3DvNgy99GRd2WjSLXcJVkNwT4IHEbMX&sz=w1000') no-repeat center center;
            background-size: contain;
            border-radius: 36px;
            box-shadow: 0 20px 30px -10px rgba(70, 50, 30, 0.2);
        }

        .section-title {
            font-size: 1.9rem; font-weight: 600; margin: 40px 0 24px; color: #325a3f;
        }
        .section-title:after {
            content: ""; display: block; width: 70px; height: 4px;
            background: #f3b33d; margin-top: 6px; border-radius: 4px;
        }

        .course-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 22px;
            margin-bottom: 40px;
        }
        @media (min-width: 480px) {
            .course-grid { grid-template-columns: repeat(2, 1fr); }
        }
        @media (min-width: 900px) {
            .course-grid { grid-template-columns: repeat(4, 1fr); }
        }
        .card-link {
            text-decoration: none; color: inherit; display: block;
            transition: all 0.2s;
        }
        .card-link:active .course-card {
            transform: scale(0.98);
            background: #f5efe3;
        }
        .course-card {
            background: #ffffffdd; backdrop-filter: blur(2px); border-radius: 28px;
            padding: 24px; box-shadow: 0 12px 30px rgba(90, 70, 40, 0.08);
            border: 1px solid #eedbbc; height: 100%;
            display: flex; flex-direction: column;
        }
        .course-icon { background: #edd7b0; width: 52px; height: 52px; border-radius: 20px; display: flex; align-items: center; justify-content: center; margin-bottom: 16px; font-size: 24px; color: #9b6d3c; }
        .course-card h3 { font-size: 1.3rem; margin-bottom: 10px; color: #2c4a3b; }
        .course-desc { color: #4d6240; font-size: 0.95rem; margin-bottom: 16px; }
        .meta-info { display: flex; justify-content: space-between; color: #6a6040; font-weight: 500; font-size: 0.85rem; border-top: 1px dashed #dbbf95; padding-top: 16px; margin-top: auto; }

        .demo-panel {
            background: #ffffff; border-radius: 32px; padding: 32px 20px; margin: 40px 0;
            box-shadow: 0 18px 40px -12px #bb9f80; border: 1px solid #e8d7c2;
        }
        .demo-title { font-size: 1.6rem; font-weight: 600; color: #2d4d3a; display: flex; align-items: center; gap: 12px; margin-bottom: 24px; flex-wrap: wrap; }
        .demo-title i { color: #f3b33d; background: #f7e9d6; padding: 10px; border-radius: 50%; }
        .registration-box { display: flex; flex-direction: column; gap: 18px; }
        .input-group label { font-weight: 600; font-size: 0.9rem; display: block; margin-bottom: 6px; color: #4f6d47; }
        .input-group input {
            width: 100%; padding: 14px 18px; border: 2px solid #dccdb4; border-radius: 40px;
            font-size: 1rem; outline: none; background: #fefbf5;
        }
        .contact-buttons {
            display: flex;
            flex-direction: column;
            gap: 12px;
            margin-top: 16px;
        }
        .wa-contact-btn, .call-contact-btn {
            border: none;
            padding: 16px 20px;
            border-radius: 60px;
            font-weight: 600;
            font-size: 1.1rem;
            cursor: pointer;
            transition: 0.2s;
            display: inline-flex;
            align-items: center;
            gap: 12px;
            justify-content: center;
            width: 100%;
            color: white;
        }
        .wa-contact-btn { background: #25D366; color: #111; }
        .wa-contact-btn i { font-size: 1.4rem; }
        .call-contact-btn { background: #2c4a3b; }
        .call-contact-btn i { font-size: 1.2rem; }

        .message-area {
            margin-top: 28px; background: #e4ded1; border-radius: 60px; padding: 16px 22px;
            font-weight: 500; display: flex; align-items: center; gap: 16px;
            color: #2d3f2a; border: 1px solid #d4bc9c; transition: all 0.3s;
        }

        .footer {
            background: #2a4033; color: #e5dccd; padding: 40px 0 24px; margin-top: 50px;
            border-radius: 32px 32px 0 0;
        }
        .footer-grid { display: grid; grid-template-columns: 1fr; gap: 30px; }
        @media (min-width: 700px) {
            .footer-grid { grid-template-columns: repeat(2, 1fr); }
        }
        .footer-logo { font-size: 1.8rem; font-weight: 700; color: #f5e7d3; }
        .footer-logo span { color: #f3b33d; }
        .social-icons i { background: #3e5f48; padding: 10px; border-radius: 50%; margin-right: 8px; color: white; font-size: 1.2rem; transition: 0.2s; cursor: pointer; display: inline-block; }
        .footer-col a { display: block; color: #cfc5b0; text-decoration: none; margin-bottom: 12px; cursor: pointer; }
        .subscribe-box { display: flex; margin-top: 12px; flex-wrap: wrap; gap: 8px; }
        .subscribe-box input { flex: 1 1 160px; padding: 10px; border-radius: 40px 0 0 40px; border: none; }
        .subscribe-box button { background: #f3b33d; border: none; padding: 10px 20px; border-radius: 40px; color: #2c4a3b; cursor: pointer; font-weight: 600; }

        .phone-footer-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: #3e5f48;
            padding: 10px 18px;
            border-radius: 40px;
            color: #f5e7d3;
            text-decoration: none;
            margin-top: 10px;
            border: 1px solid #b48b4c;
            font-weight: 500;
        }
        .phone-footer-link i { color: #f3b33d; }
        .highlight-green { background: #c8e6c9; border-color: #2e7d32; transition: 0.3s; }
    </style>
</head>
<body>
    <nav class="navbar">
        <div class="container nav-container">
            <div class="logo">edu<span>wave</span></div>
            <div class="nav-actions">
                <a href="https://chat.whatsapp.com/Lwfe2Dx4BiuDoXjQYmYhP8?mode=gi_t" target="_blank" style="text-decoration: none;">
                    <button class="whatsapp-header" id="headerWhatsAppBtn">
                        <i class="fab fa-whatsapp"></i> WhatsApp
                    </button>
                </a>
                <button class="phone-header" id="phoneHeaderBtn">
                    <i class="fas fa-phone-alt"></i> Call
                </button>
            </div>
        </div>
    </nav>

    <section class="hero">
        <div class="container hero-grid">
            <div class="hero-content">
                <h1>Unlock your <span class="highlight">potential</span> <br>with modern skills</h1>
                <p>Interactive courses, expert mentors, and a learning path tailored just for you — from zero to hero.</p>
                <button class="btn-primary" id="exploreBtn"><i class="fas fa-rocket" style="margin-right: 8px;"></i> Start exploring</button>
                <div class="hero-stats">
                    <div class="stat-item"><h3>200+</h3><p>courses</p></div>
                    <div class="stat-item"><h3>15k</h3><p>active learners</p></div>
                    <div class="stat-item"><h3>4.8</h3><p>rating</p></div>
                </div>
            </div>
            <!-- Hero image replaced with Google Drive direct link thumbnail (high quality) -->
            <div class="hero-image" style="background: url('https://drive.google.com/thumbnail?id=1y3DvNgy99GRd2WjSLXcJVkNwT4IHEbMX&sz=w1000') no-repeat center center; background-size: contain;"></div>
        </div>
    </section>

    <div class="container">
        <h2 class="section-title">Featured programs (click card → drive folder)</h2>
        <div class="course-grid" id="courseGrid"></div>

        <div class="demo-panel" id="registerDemo">
            <div class="demo-title">
                <i class="fas fa-id-card-alt"></i>
                <span>Get in touch – direct contact</span>
            </div>
            <div class="registration-box">
                <div class="input-group">
                    <label for="studentName"><i class="fas fa-user-graduate"></i> Full name</label>
                    <input type="text" id="studentName" placeholder="e.g., Alex Rivera" value="">
                </div>
                <div class="input-group">
                    <label for="interest"><i class="fas fa-book"></i> Course interest</label>
                    <input type="text" id="interest" placeholder="e.g., Data Science" value="">
                </div>
                <div class="contact-buttons">
                    <!-- WhatsApp live chat – real group invite with tracking -->
                    <a href="https://chat.whatsapp.com/Lwfe2Dx4BiuDoXjQYmYhP8?mode=gi_t" target="_blank" style="text-decoration: none; width: 100%;" id="whatsappLiveLink">
                        <button class="wa-contact-btn" id="whatsappDemoBtn"><i class="fab fa-whatsapp"></i> Chat on WhatsApp</button>
                    </a>
                    <!-- Phone button with real tel: link -->
                    <a href="tel:+255776290901" style="text-decoration: none; width: 100%;">
                        <button class="call-contact-btn" id="phoneDemoBtn"><i class="fas fa-headset"></i> Call +255 776 290 901</button>
                    </a>
                </div>
            </div>
            <div id="dynamicMessage" class="message-area">
                <i class="fas fa-comment-dots"></i>
                <span id="messageText">Alex, we're ready to talk about Data Science!</span>
            </div>
            <p style="font-size:0.8rem; margin-top:14px; color:#7b6e5a;"><i class="fas fa-mobile-alt"></i> Tap WhatsApp to join group, or call us directly.</p>
        </div>
    </div>

    <footer class="footer">
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <div class="footer-logo">edu<span>wave</span></div>
                    <p>Empowering lifelong learning through accessible education.</p>
                    <div class="social-icons">
                        <i class="fab fa-twitter" id="twitterLive" role="button" tabindex="0" title="Twitter (live)"></i>
                        <i class="fab fa-linkedin-in" id="linkedinLive" role="button" tabindex="0" title="LinkedIn (live)"></i>
                        <i class="fab fa-github" id="githubLive" role="button" tabindex="0" title="GitHub (live)"></i>
                    </div>
                    <div style="margin-top:16px; display: flex; flex-direction: column; gap: 8px;">
                        <a href="https://chat.whatsapp.com/Lwfe2Dx4BiuDoXjQYmYhP8?mode=gi_t" target="_blank" class="phone-footer-link" style="background:#25D366; color:#111; border:none;">
                            <i class="fab fa-whatsapp"></i> WhatsApp group
                        </a>
                        <a href="tel:+255776290901" class="phone-footer-link" style="background:#3e5f48;" id="footerPhoneLink">
                            <i class="fas fa-phone"></i> +255 776 290 901
                        </a>
                    </div>
                </div>
                <div class="footer-col"><h4>Platform</h4><a class="footer-link" id="browseCoursesLink">Browse courses</a><a class="footer-link" id="pathsLink">Learning paths</a><a class="footer-link" id="pricingLink">Pricing</a></div>
                <div class="footer-col"><h4>Support</h4><a class="footer-link" id="helpCenterLink">Help center</a><a class="footer-link" id="communityLink">Community</a><a class="footer-link" id="contactFooter">Contact</a></div>
                <div class="footer-col">
                    <h4>Stay curious</h4><p>Subscribe to get updates.</p>
                    <div class="subscribe-box">
                        <input id="subscribeEmail" placeholder="email" type="email">
                        <button id="subscribeBtn">Go</button>
                    </div>
                </div>
            </div>
            <div class="copyright">&copy; 2025 eduwave · <i class="fas fa-heart" style="color:#f3b33d;"></i>imeandaliwa ni JTL Zanzibar, direct contact,</div>
        </div>
    </footer>

    <script>
        (function() {
            // ---------- REAL COURSE CARDS (google drive folders) ----------
            const courseGrid = document.getElementById('courseGrid');
            const courses = [
                { icon: 'fas fa-chart-line', name: 'Data Science', desc: 'Python, SQL, and visualisation.', duration: '8 weeks', level: 'Intermediate', drive: 'https://drive.google.com/drive/folders/1MX1FA_HfTkOcl-MkRGCJGSG3L_ohBYcW' },
                { icon: 'fas fa-laptop-code', name: 'Web Dev bootcamp', desc: 'HTML, CSS, JavaScript, React.', duration: '10 weeks', level: 'Beginner', drive: 'https://drive.google.com/drive/folders/1mo5H_fbdbfuS6BHxjeQipGM3JbiZohY9' },
                { icon: 'fas fa-microchip', name: 'AI & Machine Learning', desc: 'Neural networks, TensorFlow.', duration: '12 weeks', level: 'Advanced', drive: 'https://drive.google.com/drive/folders/1aRRi0C5qbpcsUuqrgnKvyIqlCL00wUaK' },
                { icon: 'fas fa-bullseye', name: 'Product management', desc: 'Go-to-market, agile & analytics.', duration: '6 weeks', level: 'All levels', drive: 'https://drive.google.com/drive/folders/14i708FRvneNRfBEBI3WDnM0OMREu47zT' }
            ];

            function renderCourses() {
                let html = '';
                courses.forEach(c => {
                    html += `
                        <a href="${c.drive}" target="_blank" class="card-link" title="Open Google Drive folder (real)">
                            <div class="course-card">
                                <div class="course-icon"><i class="${c.icon}"></i></div>
                                <h3>${c.name}</h3>
                                <div class="course-desc">${c.desc}</div>
                                <div class="meta-info">
                                    <span><i class="far fa-calendar-alt"></i> ${c.duration}</span>
                                    <span><i class="far fa-chart-bar"></i> ${c.level}</span>
                                </div>
                                <span style="font-size:0.75rem; margin-top:12px; color:#b6582c;"><i class="fas fa-external-link-alt"></i> drive folder</span>
                            </div>
                        </a>
                    `;
                });
                courseGrid.innerHTML = html;
            }
            renderCourses();

            // ---------- DYNAMIC MESSAGE (name/interest) ----------
            const studentInput = document.getElementById('studentName');
            const interestInput = document.getElementById('interest');
            const messageSpan = document.getElementById('messageText');
            const msgBox = document.getElementById('dynamicMessage');

            function updateMessage() {
                const name = studentInput.value.trim() || 'Learner';
                const interest = interestInput.value.trim() || 'your course';
                messageSpan.innerText = `${name}, we're ready to talk about ${interest}!`;
            }
            studentInput.addEventListener('input', updateMessage);
            interestInput.addEventListener('input', updateMessage);
            updateMessage();

            // ---------- REAL CONTACT: no alerts, only live actions ----------
            // Header phone button triggers tel:
            document.getElementById('phoneHeaderBtn').addEventListener('click', function() {
                window.location.href = 'tel:+255776290901';
            });

            // Demo panel phone is already wrapped in <a href="tel:">, but we also want dynamic message update.
            document.getElementById('phoneDemoBtn').addEventListener('click', function(e) {
                messageSpan.innerText = `Calling +255 776 290 901 for ${studentInput.value.trim() || 'you'} ...`;
                msgBox.classList.add('highlight-green');
                setTimeout(() => msgBox.classList.remove('highlight-green'), 800);
                // navigation to tel: will occur because parent <a href="tel:"> captures click
            });

            // WhatsApp buttons: group link + dynamic message
            function handleWhatsAppClick(source) {
                messageSpan.innerText = `Opening WhatsApp group for ${studentInput.value.trim() || 'you'}!`;
                msgBox.classList.add('highlight-green');
                setTimeout(() => msgBox.classList.remove('highlight-green'), 800);
                // navigation handled by href
            }

            document.getElementById('headerWhatsAppBtn')?.addEventListener('click', function() {
                handleWhatsAppClick('header');
            });
            document.getElementById('whatsappDemoBtn')?.addEventListener('click', function() {
                handleWhatsAppClick('demo');
            });
            const footerWA = document.querySelector('.phone-footer-link[href*="whatsapp"]');
            if (footerWA) {
                footerWA.addEventListener('click', function() {
                    handleWhatsAppClick('footer');
                });
            }

            document.getElementById('contactFooter')?.addEventListener('click', (e) => {
                e.preventDefault();
                window.open('https://chat.whatsapp.com/Lwfe2Dx4BiuDoXjQYmYhP8?mode=gi_t', '_blank');
                messageSpan.innerText = `Opening WhatsApp group for you.`;
                msgBox.classList.add('highlight-green');
                setTimeout(() => msgBox.classList.remove('highlight-green'), 800);
            });

            document.getElementById('exploreBtn').addEventListener('click', function() {
                document.getElementById('registerDemo').scrollIntoView({ behavior: 'smooth' });
            });

            // ---------- REAL SOCIAL LINKS ----------
            document.getElementById('twitterLive')?.addEventListener('click', () => {
                window.open('https://twitter.com/eduverse', '_blank');
            });
            document.getElementById('linkedinLive')?.addEventListener('click', () => {
                window.open('https://linkedin.com/school/eduverse', '_blank');
            });
            document.getElementById('githubLive')?.addEventListener('click', () => {
                window.open('https://github.com/eduverse', '_blank');
            });

            // Footer navigation
            document.getElementById('browseCoursesLink')?.addEventListener('click', (e) => {
                e.preventDefault();
                document.querySelector('.course-grid').scrollIntoView({ behavior: 'smooth' });
            });
            document.getElementById('pathsLink')?.addEventListener('click', (e) => {
                e.preventDefault();
                document.getElementById('registerDemo').scrollIntoView({ behavior: 'smooth' });
            });
            document.getElementById('pricingLink')?.addEventListener('click', (e) => {
                e.preventDefault();
                alert('📋 Pricing page would open – we have free and premium plans.');
            });
            document.getElementById('helpCenterLink')?.addEventListener('click', (e) => {
                e.preventDefault();
                window.open('https://support.eduverse.com', '_blank');
            });
            document.getElementById('communityLink')?.addEventListener('click', (e) => {
                e.preventDefault();
                window.open('https://community.eduverse.com', '_blank');
            });

            // subscribe: real email capture simulation
            document.getElementById('subscribeBtn').addEventListener('click', () => {
                const email = document.getElementById('subscribeEmail').value.trim();
                if (email && email.includes('@')) {
                    alert(`✅ Thanks! ${email} subscribed to newsletter.`);
                    localStorage.setItem('eduverse_subscriber', email);
                    document.getElementById('subscribeEmail').value = '';
                } else {
                    alert('📧 Please enter a valid email address.');
                }
            });

            document.getElementById('footerPhoneLink')?.addEventListener('click', function() {
                messageSpan.innerText = `Dialing +255 776 290 901 ...`;
                msgBox.classList.add('highlight-green');
                setTimeout(() => msgBox.classList.remove('highlight-green'), 1000);
            });

            // Ensure hero image remains correct even if style attribute is overridden 
            // (already inline style, but double-check)
            const heroDiv = document.querySelector('.hero-image');
            if (heroDiv) {
                heroDiv.style.background = "url('https://drive.google.com/thumbnail?id=1y3DvNgy99GRd2WjSLXcJVkNwT4IHEbMX&sz=w1000') no-repeat center center";
                heroDiv.style.backgroundSize = "contain";
            }
        })();
    </script>
</body>
</html>

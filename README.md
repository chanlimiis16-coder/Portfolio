<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Sweet E-Portfolio 🎀</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

    <style>
        /* --- CSS STYLING (Pink & Cute Theme) --- */
        :root {
            --bg-pink: #fff0f6;
            --sidebar-pink: #fcc2d7;
            --text-pink: #a61e4d;
            --accent-pink: #ff85b3;
            --white: #ffffff;
        }

        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            display: flex;
            background-color: var(--bg-pink);
            color: #444;
            overflow-x: hidden;
        }

        /* Sidebar Navigation */
        .sidebar {
            width: 260px;
            height: 100vh;
            background-color: var(--sidebar-pink);
            padding: 20px;
            position: fixed;
            box-shadow: 4px 0 10px rgba(0,0,0,0.05);
            z-index: 10;
        }

        .logo {
            font-family: 'Dancing Script', cursive;
            color: var(--text-pink);
            font-size: 2rem;
            text-align: center;
            margin-bottom: 30px;
        }

        .sidebar ul { list-style: none; padding: 0; }
        .sidebar ul li a {
            text-decoration: none;
            color: var(--text-pink);
            display: block;
            padding: 12px;
            border-radius: 10px;
            transition: 0.3s;
            font-weight: 500;
            cursor: pointer;
        }

        .sidebar ul li a:hover {
            background-color: var(--bg-pink);
            transform: translateX(5px);
        }

        .nav-header {
            font-weight: bold;
            color: var(--text-pink);
            margin: 20px 0 10px 10px;
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Main Content */
        .content {
            margin-left: 300px;
            padding: 50px;
            width: 100%;
        }

        .page-section { display: none; }
        .page-section.active { display: block; animation: fadeIn 0.8s ease; }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(15px); }
            to { opacity: 1; transform: translateY(0); }
        }

        h1 { font-family: 'Dancing Script', cursive; color: var(--text-pink); font-size: 3.5rem; margin-top: 0; }

        .card {
            background: var(--white);
            padding: 25px;
            border-radius: 20px;
            box-shadow: 0 8px 20px rgba(255, 133, 179, 0.15);
            margin-bottom: 25px;
        }

        .profile-img { 
            width: 180px; 
            height: 180px;
            border-radius: 50%; 
            border: 6px solid var(--white); 
            box-shadow: 0 5px 15px rgba(0,0,0,0.1); 
            object-fit: cover;
        }

        /* Butterfly Confetti */
        #butterfly-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            pointer-events: none;
            z-index: 9999;
        }

        .butterfly {
            position: absolute;
            width: 60px; 
            opacity: 0;
            animation: moveAround 10s ease-in-out forwards;
        }

        @keyframes moveAround {
            0% { transform: translate(0, 100vh) rotate(0deg); opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { transform: translate(200px, -200px) rotate(360deg); opacity: 0; }
        }

        /* Conclusion Buttons */
        .collapsible {
            background-color: var(--accent-pink);
            color: white;
            cursor: pointer;
            padding: 18px;
            width: 100%;
            border: none;
            text-align: left;
            font-size: 1.1rem;
            border-radius: 12px;
            margin-top: 15px;
            font-weight: 600;
            transition: 0.3s;
        }

        .collapsible:hover { filter: brightness(1.05); }

        .collapsible-content {
            display: none;
            padding: 20px;
            background-color: white;
            border-radius: 0 0 12px 12px;
            border: 2px solid var(--accent-pink);
            border-top: none;
        }

        details summary { cursor: pointer; color: var(--text-pink); font-weight: 600; margin-top: 10px; }
    </style>
</head>
<body onload="startButterflyAnimation()">

    <div id="butterfly-container"></div>

    <nav class="sidebar">
        <h2 class="logo">Portfolio 💖</h2>
        <ul>
            <li><a onclick="showSection('profile')">Profile</a></li>
            <li><a onclick="showSection('cover-letter')">Cover Letter</a></li>
            <div class="nav-header">Table of Contents</div>
            <li><a onclick="showSection('rubric')">a. Rubric ✨</a></li>
            <li><a onclick="showSection('grasps')">b. GRASPS Model</a></li>
            <li><a onclick="showSection('affective')">c.1 Affective Tools</a></li>
            <li><a onclick="showSection('interview')">c.2 Interview</a></li>
            <li><a onclick="showSection('favorable')">d. Favorable/Unfavorable</a></li>
            <li><a onclick="showSection('simulation')">e.2 Simulation 🎥</a></li>
            <li><a onclick="showSection('conclusion')">Conclusion 🎀</a></li>
        </ul>
    </nav>

    <main class="content">
        
        <section id="profile" class="page-section active">
            <h1>Hi, I'm [Your Name]! 🌸</h1>
            <div class="card">
                <img src="profile-pic.jpg" alt="Insert your photo" class="profile-img">
                <p>Welcome to my e-portfolio! This space holds all my hard work, reflections, and growth. I hope you enjoy looking through it! ✨</p>
            </div>
        </section>

        <section id="cover-letter" class="page-section">
            <h1>Cover Letter 💌</h1>
            <div class="card">
                <p>To [Recipient Name],</p>
                <p>Insert your formal cover letter text here. Express your professional goals and why you created this portfolio.</p>
            </div>
        </section>

        <section id="rubric" class="page-section">
            <h1>Assessment Rubrics</h1>
            <div class="card">
                <h3>Analytic & Holistic Rubrics</h3>
                <p>Here I showcase the different scoring guides used in our assessments.</p>
                <details>
                    <summary>View Reflection</summary>
                    <p>Reflection: Through these rubrics, I learned how to measure success objectively...</p>
                </details>
            </div>
        </section>

        <section id="simulation" class="page-section">
            <h1>Simulation Video</h1>
            <div class="card" style="text-align:center; padding: 50px;">
                <p>[Video Placeholder - Upload your video to GitHub and link it here]</p>
            </div>
            <details>
                <summary>Reflection</summary>
                <p>The simulation allowed me to apply theoretical knowledge in a practical setting...</p>
            </details>
        </section>

        <section id="conclusion" class="page-section">
            <h1>Final Thoughts 🎀</h1>
            <button class="collapsible">What I have learned</button>
            <div class="collapsible-content"><p>Insert your learning summary here.</p></div>
            
            <button class="collapsible">Letter to myself</button>
            <div class="collapsible-content"><p>Dear self, look how far you've come!</p></div>
            
            <button class="collapsible">Letter to my parent</button>
            <div class="collapsible-content"><p>Thank you for believing in me and supporting my education.</p></div>
        </section>

    </main>

    <script>
        // Section Switching
        function showSection(sectionId) {
            const sections = document.querySelectorAll('.page-section');
            sections.forEach(sec => sec.classList.remove('active'));
            document.getElementById(sectionId).classList.add('active');
            window.scrollTo(0,0);
        }

        // Butterfly Animation
        function startButterflyAnimation() {
            const container = document.getElementById('butterfly-container');
            const butterflyCount = 20;

            for (let i = 0; i < butterflyCount; i++) {
                const img = document.createElement('img');
                img.src = 'butterfly.png'; // Make sure this file exists!
                img.className = 'butterfly';
                
                // Randomize positions and speed
                img.style.left = Math.random() * 100 + 'vw';
                img.style.top = (Math.random() * 50 + 50) + 'vh'; 
                img.style.animationDelay = (Math.random() * 3) + 's';
                img.style.width = (Math.random() * 40 + 40) + 'px';
                
                container.appendChild(img);
            }

            // Vanish immediately after 10 seconds
            setTimeout(() => {
                container.style.transition = "opacity 1s ease";
                container.style.opacity = "0";
                setTimeout(() => {
                    container.innerHTML = ''; // Delete from page
                }, 1000);
            }, 10000);
        }

        // Collapsible Logic
        var coll = document.getElementsByClassName("collapsible");
        for (let i = 0; i < coll.length; i++) {
            coll[i].addEventListener("click", function() {
                this.classList.toggle("active");
                var content = this.nextElementSibling;
                if (content.style.display === "block") {
                    content.style.display = "none";
                } else {
                    content.style.display = "block";
                }
            });
        }
    </script>
</body>
</html>

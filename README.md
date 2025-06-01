<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ethical Hacking Career Guide | Monu Kumar CyberExport</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #0d1b2a;
            --secondary: #1b263b;
            --accent: #415a77;
            --highlight: #778da9;
            --text: #e0e1dd;
            --success: #2ecc71;
            --warning: #e74c3c;
            --terminal: #00ff41;
            --glow: 0 0 10px rgba(0, 255, 65, 0.7);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0c0f17, #121827);
            color: var(--text);
            line-height: 1.6;
            min-height: 100vh;
            padding: 0;
            overflow-x: hidden;
            position: relative;
        }
        
        body::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 10% 20%, rgba(65, 90, 119, 0.1) 0%, transparent 20%),
                radial-gradient(circle at 90% 80%, rgba(65, 90, 119, 0.1) 0%, transparent 20%);
            z-index: -1;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Header Styles */
        header {
            text-align: center;
            padding: 60px 20px 40px;
            position: relative;
            overflow: hidden;
            border-bottom: 1px solid rgba(119, 141, 169, 0.2);
            background: linear-gradient(to bottom, rgba(13, 27, 42, 0.9), rgba(27, 38, 59, 0.7));
        }
        
        header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path d="M0,0 L100,0 L100,100 Q50,80 0,100" fill="rgba(65,90,119,0.1)"/></svg>');
            background-size: 100% 100%;
            opacity: 0.3;
            z-index: -1;
        }
        
        h1 {
            font-size: 3.5rem;
            margin-bottom: 15px;
            text-transform: uppercase;
            letter-spacing: 3px;
            background: linear-gradient(to right, var(--highlight), var(--text));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: var(--glow);
            position: relative;
            display: inline-block;
        }
        
        h1::after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 25%;
            width: 50%;
            height: 3px;
            background: var(--terminal);
            border-radius: 3px;
            box-shadow: var(--glow);
        }
        
        .byline {
            font-size: 1.4rem;
            color: var(--highlight);
            margin-top: 25px;
            font-style: italic;
            letter-spacing: 1px;
            text-shadow: 0 0 5px rgba(119, 141, 169, 0.5);
        }
        
        .byline span {
            color: var(--terminal);
            font-weight: bold;
        }
        
        .tagline {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 20px auto 0;
            color: var(--highlight);
            line-height: 1.8;
        }
        
        /* Warning Banner */
        .warning-banner {
            background: linear-gradient(to right, #c0392b, #e74c3c);
            padding: 25px;
            border-radius: 8px;
            margin: 40px 0;
            display: flex;
            align-items: center;
            box-shadow: 0 5px 20px rgba(231, 76, 60, 0.3);
            border-left: 5px solid #fff;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(231, 76, 60, 0.5); }
            70% { box-shadow: 0 0 0 15px rgba(231, 76, 60, 0); }
            100% { box-shadow: 0 0 0 0 rgba(231, 76, 60, 0); }
        }
        
        .warning-icon {
            font-size: 2.5rem;
            margin-right: 20px;
            flex-shrink: 0;
            color: white;
        }
        
        .warning-content h2 {
            font-size: 1.8rem;
            margin-bottom: 12px;
            color: white;
        }
        
        /* Content Grid */
        .content-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 50px 0;
        }
        
        .card {
            background: rgba(27, 38, 59, 0.7);
            border-radius: 10px;
            padding: 30px;
            transition: all 0.3s ease;
            border: 1px solid rgba(119, 141, 169, 0.3);
            backdrop-filter: blur(5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            position: relative;
            overflow: hidden;
        }
        
        .card::before {
            content: "";
            position: absolute;
            top: -1px;
            left: 0;
            width: 100%;
            height: 5px;
            background: var(--terminal);
            box-shadow: var(--glow);
        }
        
        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.4);
            border-color: var(--terminal);
        }
        
        .card h3 {
            font-size: 1.6rem;
            margin-bottom: 20px;
            color: var(--terminal);
            display: flex;
            align-items: center;
        }
        
        .card h3 i {
            margin-right: 12px;
            background: rgba(0, 255, 65, 0.1);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            border: 1px solid var(--terminal);
        }
        
        .card ul {
            padding-left: 20px;
        }
        
        .card li {
            margin-bottom: 12px;
            position: relative;
            padding-left: 25px;
        }
        
        .card li:before {
            content: ">";
            color: var(--terminal);
            font-family: monospace;
            font-weight: bold;
            position: absolute;
            left: 0;
            top: 0;
        }
        
        /* Terminal Section */
        .terminal-container {
            background: rgba(15, 23, 36, 0.8);
            border-radius: 10px;
            padding: 30px;
            margin: 50px 0;
            border: 1px solid var(--accent);
            position: relative;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .terminal-header {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid rgba(119, 141, 169, 0.2);
        }
        
        .terminal-dots {
            display: flex;
            gap: 8px;
            margin-right: 15px;
        }
        
        .terminal-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }
        
        .dot-red { background: #e74c3c; }
        .dot-yellow { background: #f39c12; }
        .dot-green { background: var(--terminal); }
        
        .terminal-title {
            color: var(--highlight);
            font-size: 1.2rem;
            letter-spacing: 1px;
        }
        
        .terminal-content {
            background: rgba(0, 0, 0, 0.7);
            border-radius: 5px;
            padding: 20px;
            font-family: 'Courier New', monospace;
            font-size: 1.1rem;
            line-height: 1.8;
            min-height: 200px;
            color: var(--terminal);
            text-shadow: 0 0 5px rgba(0, 255, 65, 0.5);
            border: 1px solid rgba(0, 255, 65, 0.2);
            box-shadow: inset 0 0 10px rgba(0, 255, 65, 0.1);
            overflow: auto;
            white-space: pre;
        }
        
        .terminal-command {
            color: var(--terminal);
        }
        
        .terminal-comment {
            color: #7f8c8d;
        }
        
        .terminal-path {
            color: #3498db;
        }
        
        /* Resources Section */
        .resources {
            margin: 60px 0;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 40px;
            color: var(--highlight);
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .section-title::after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 25%;
            width: 50%;
            height: 3px;
            background: var(--terminal);
            border-radius: 3px;
            box-shadow: var(--glow);
        }
        
        .resource-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
        }
        
        .resource-item {
            background: rgba(27, 38, 59, 0.7);
            border-radius: 8px;
            padding: 25px;
            transition: all 0.3s ease;
            border: 1px solid rgba(119, 141, 169, 0.3);
            text-align: center;
        }
        
        .resource-item:hover {
            transform: translateY(-5px);
            border-color: var(--terminal);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }
        
        .resource-icon {
            font-size: 2.5rem;
            color: var(--terminal);
            margin-bottom: 20px;
        }
        
        .resource-item h3 {
            color: var(--text);
            margin-bottom: 15px;
            font-size: 1.3rem;
        }
        
        .resource-item p {
            color: var(--highlight);
            line-height: 1.6;
        }
        
        /* Call to Action */
        .cta-section {
            text-align: center;
            padding: 60px 30px;
            margin: 50px 0;
            background: linear-gradient(to right, rgba(27, 38, 59, 0.8), rgba(65, 90, 119, 0.5));
            border-radius: 15px;
            border: 1px solid rgba(0, 255, 65, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        .cta-section::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 30%, rgba(0, 255, 65, 0.05) 0%, transparent 20%),
                radial-gradient(circle at 80% 70%, rgba(0, 255, 65, 0.05) 0%, transparent 20%);
            z-index: -1;
        }
        
        .cta-section h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--text);
        }
        
        .cta-section p {
            font-size: 1.3rem;
            max-width: 800px;
            margin: 0 auto 30px;
            line-height: 1.8;
            color: var(--highlight);
        }
        
        .btn {
            display: inline-block;
            background: transparent;
            color: var(--terminal);
            padding: 15px 35px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.2rem;
            transition: all 0.3s ease;
            border: 2px solid var(--terminal);
            cursor: pointer;
            text-transform: uppercase;
            letter-spacing: 1px;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }
        
        .btn::before {
            content: "";
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: var(--terminal);
            transition: all 0.4s ease;
            z-index: -1;
        }
        
        .btn:hover {
            color: var(--primary);
            text-shadow: 0 0 5px rgba(0, 0, 0, 0.5);
        }
        
        .btn:hover::before {
            left: 0;
        }
        
        /* Footer */
        footer {
            text-align: center;
            padding: 40px 20px;
            margin-top: 50px;
            border-top: 1px solid rgba(119, 141, 169, 0.2);
            color: var(--highlight);
            background: rgba(13, 27, 42, 0.8);
        }
        
        .footer-logo {
            font-size: 1.8rem;
            font-weight: bold;
            margin-bottom: 20px;
            color: var(--terminal);
            text-shadow: var(--glow);
        }
        
        .copyright {
            font-size: 0.9rem;
            opacity: 0.7;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            
            .byline {
                font-size: 1.1rem;
            }
            
            .tagline {
                font-size: 1rem;
            }
            
            .warning-banner {
                flex-direction: column;
                text-align: center;
            }
            
            .warning-icon {
                margin-right: 0;
                margin-bottom: 15px;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .animated {
            animation: fadeIn 0.6s ease forwards;
        }
        
        .delay-1 { animation-delay: 0.2s; }
        .delay-2 { animation-delay: 0.4s; }
        .delay-3 { animation-delay: 0.6s; }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1 class="animated">Ethical Hacking Career Guide</h1>
            <p class="byline animated delay-1">by <span>Monu Kumar CyberExport</span></p>
            <p class="tagline animated delay-2">Master the art of cybersecurity through legal and ethical practices. Learn how to protect systems and build a rewarding career as a white hat hacker.</p>
        </header>
        
        <div class="warning-banner animated delay-3">
            <div class="warning-icon">
                <i class="fas fa-exclamation-triangle"></i>
            </div>
            <div class="warning-content">
                <h2>Ethical Responsibility Notice</h2>
                <p>Black hat hacking (unauthorized system access) is illegal and unethical. This guide focuses exclusively on legal cybersecurity practices. Ethical hackers work within legal frameworks to protect systems and data with proper authorization.</p>
            </div>
        </div>
        
        <div class="content-grid">
            <div class="card animated delay-1">
                <h3><i class="fas fa-brain"></i> Core Skills</h3>
                <ul>
                    <li>Operating systems (Linux, Windows internals)</li>
                    <li>Networking concepts (TCP/IP, DNS, HTTP/S)</li>
                    <li>Programming (Python, Bash, C/C++)</li>
                    <li>Web technologies (HTML, JS, APIs)</li>
                    <li>Cryptography principles</li>
                    <li>Vulnerability assessment</li>
                    <li>Penetration testing methodologies</li>
                </ul>
            </div>
            
            <div class="card animated delay-2">
                <h3><i class="fas fa-certificate"></i> Certifications</h3>
                <ul>
                    <li>CEH (Certified Ethical Hacker)</li>
                    <li>OSCP (Offensive Security Certified Professional)</li>
                    <li>CompTIA Security+</li>
                    <li>CISSP (Certified Information Systems Security Professional)</li>
                    <li>eJPT (eLearnSecurity Junior Penetration Tester)</li>
                    <li>Pentest+</li>
                    <li>GIAC Security Certifications</li>
                </ul>
            </div>
            
            <div class="card animated delay-3">
                <h3><i class="fas fa-user-secret"></i> Career Paths</h3>
                <ul>
                    <li>Penetration Tester</li>
                    <li>Security Analyst</li>
                    <li>Vulnerability Researcher</li>
                    <li>Security Consultant</li>
                    <li>Incident Responder</li>
                    <li>Security Architect</li>
                    <li>Bug Bounty Hunter</li>
                </ul>
            </div>
        </div>
        
        <div class="terminal-container animated">
            <div class="terminal-header">
                <div class="terminal-dots">
                    <div class="terminal-dot dot-red"></div>
                    <div class="terminal-dot dot-yellow"></div>
                    <div class="terminal-dot dot-green"></div>
                </div>
                <div class="terminal-title">ethical-hacking-career-guide</div>
            </div>
            <div class="terminal-content" id="terminal-output">
                <span class="terminal-path">user@career-guide:~$</span> ./start_ethical_hacking_career.sh
                
                > Initializing Ethical Hacking Career Path...
                
                [✓] Step 1: Learn fundamentals (Networking, Systems, Programming)
                [✓] Step 2: Practice on legal platforms (HackTheBox, TryHackMe)
                [✓] Step 3: Obtain certifications (CEH, OSCP, Security+)
                [✓] Step 4: Participate in bug bounty programs
                [✓] Step 5: Build professional network
                [✓] Step 6: Apply for security positions
                
                > Career path initialized successfully!
                
                <span class="terminal-path">user@career-guide:~$</span> <span class="terminal-command">view_salaries</span>
                
                Entry-Level Security Analyst: $70,000 - $90,000
                Penetration Tester: $90,000 - $130,000
                Security Consultant: $110,000 - $160,000
                Security Architect: $140,000 - $200,000
                
                <span class="terminal-path">user@career-guide:~$</span> 
            </div>
        </div>
        
        <h2 class="section-title animated">Learning Resources</h2>
        <div class="resources">
            <div class="resource-grid">
                <div class="resource-item animated delay-1">
                    <div class="resource-icon">
                        <i class="fas fa-laptop-code"></i>
                    </div>
                    <h3>Practice Platforms</h3>
                    <p>Hack The Box, TryHackMe, PentesterLab, OverTheWire, PortSwigger Academy</p>
                </div>
                
                <div class="resource-item animated delay-2">
                    <div class="resource-icon">
                        <i class="fas fa-book"></i>
                    </div>
                    <h3>Books</h3>
                    <p>The Web Application Hacker's Handbook, Penetration Testing, RTFM, Black Hat Python, The Hacker Playbook</p>
                </div>
                
                <div class="resource-item animated delay-1">
                    <div class="resource-icon">
                        <i class="fas fa-graduation-cap"></i>
                    </div>
                    <h3>Courses</h3>
                    <p>Offensive Security, SANS Institute, Cybrary, Coursera Cybersecurity, Udemy Ethical Hacking</p>
                </div>
                
                <div class="resource-item animated delay-2">
                    <div class="resource-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3>Communities</h3>
                    <p>OWASP, DEF CON, Black Hat, HackerOne, Reddit r/netsec, Discord Security Servers</p>
                </div>
            </div>
        </div>
        
        <div class="cta-section animated">
            <h2>Begin Your Ethical Hacking Journey</h2>
            <p>Join thousands of security professionals who started exactly where you are now. With dedication and ethical practice, you can build a rewarding cybersecurity career.</p>
            <button class="btn">Download Career Roadmap</button>
        </div>
    </div>
    
    <footer>
        <div class="footer-logo">Monu Kumar CyberExport</div>
        <p>Ethical Hacking Career Guide | Created for Educational Purposes</p>
        <p class="copyright">© 2023 All Rights Reserved | Always obtain proper authorization before security testing</p>
    </footer>
    
    <script>
        // Terminal typing animation
        document.addEventListener('DOMContentLoaded', function() {
            const terminal = document.getElementById('terminal-output');
            const originalContent = terminal.innerHTML;
            
            // Clear terminal initially
            terminal.innerHTML = '';
            
            let i = 0;
            function typeWriter() {
                if (i < originalContent.length) {
                    terminal.innerHTML += originalContent.charAt(i);
                    i++;
                    setTimeout(typeWriter, 20);
                    
                    // Scroll to bottom
                    terminal.scrollTop = terminal.scrollHeight;
                }
            }
            
            // Start typing animation after a delay
            setTimeout(typeWriter, 1000);
        });
        
        // Animation on scroll
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animated');
                }
            });
        }, { threshold: 0.1 });
        
        document.querySelectorAll('.card, .resource-item, .cta-section').forEach(el => {
            observer.observe(el);
        });
    </script>
</body>
</html>

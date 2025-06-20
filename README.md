<!DOCTYPE html>
<html lang="vn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Đỗ Tấn Sang  - 自己紹介</title>
    <link rel="stylesheet" href="style.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.1);
            overflow: hidden;
            animation: slideUp 0.8s ease-out;
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Header Section */
        .header {
            background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
            color: white;
            padding: 40px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="20" cy="20" r="2" fill="white" opacity="0.1"/><circle cx="80" cy="40" r="1.5" fill="white" opacity="0.1"/><circle cx="40" cy="80" r="1" fill="white" opacity="0.1"/></svg>');
            animation: float 20s linear infinite;
        }

        @keyframes float {
            0% { transform: translate(-50%, -50%) rotate(0deg); }
            100% { transform: translate(-50%, -50%) rotate(360deg); }
        }

        .profile-image {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: linear-gradient(135deg, #74b9ff, #0984e3);
            margin: 0 auto 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            border: 5px solid rgba(255,255,255,0.2);
            position: relative;
            z-index: 1;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        .header h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }

        .header .title {
            font-size: 1.3rem;
            opacity: 0.9;
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            position: relative;
            z-index: 1;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.95rem;
        }

        /* Main Content */
        .main-content {
            padding: 40px;
        }

        .section {
            margin-bottom: 40px;
            opacity: 0;
            transform: translateY(20px);
            animation: fadeInUp 0.6s ease-out forwards;
        }

        .section:nth-child(1) { animation-delay: 0.2s; }
        .section:nth-child(2) { animation-delay: 0.4s; }
        .section:nth-child(3) { animation-delay: 0.6s; }
        .section:nth-child(4) { animation-delay: 0.8s; }
        .section:nth-child(5) { animation-delay: 1s; }

        @keyframes fadeInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .section-title {
            font-size: 1.8rem;
            color: #2c3e50;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 3px solid #3498db;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -3px;
            left: 0;
            width: 50px;
            height: 3px;
            background: #e74c3c;
        }

        /* Professional Summary */
        .summary {
            background: linear-gradient(135deg, #f8f9fa, #e9ecef);
            padding: 25px;
            border-radius: 15px;
            border-left: 5px solid #3498db;
            font-size: 1.1rem;
            line-height: 1.8;
        }

        /* Skills */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }

        .skill-category {
            background: #f8f9fa;
            padding: 25px;
            border-radius: 15px;
            border-top: 4px solid #3498db;
            transition: all 0.3s ease;
        }

        .skill-category:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .skill-category h4 {
            color: #2c3e50;
            margin-bottom: 15px;
            font-size: 1.2rem;
        }

        .skills-list {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .skill-tag {
            background: linear-gradient(135deg, #3498db, #2980b9);
            color: white;
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 0.9rem;
            transition: all 0.3s ease;
        }

        .skill-tag:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(52, 152, 219, 0.3);
        }

        /* Experience */
        .experience-item {
            background: white;
            border-left: 4px solid #3498db;
            padding: 25px;
            margin-bottom: 20px;
            border-radius: 10px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.05);
            position: relative;
            transition: all 0.3s ease;
        }

        .experience-item:hover {
            transform: translateX(10px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .experience-item::before {
            content: '';
            position: absolute;
            left: -8px;
            top: 30px;
            width: 12px;
            height: 12px;
            background: #3498db;
            border-radius: 50%;
            border: 3px solid white;
        }

        .job-title {
            font-size: 1.3rem;
            color: #2c3e50;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .company {
            color: #3498db;
            font-weight: 600;
            margin-bottom: 5px;
        }

        .duration {
            color: #7f8c8d;
            font-style: italic;
            margin-bottom: 15px;
        }

        .achievements {
            list-style: none;
        }

        .achievements li {
            margin-bottom: 8px;
            padding-left: 20px;
            position: relative;
        }

        .achievements li::before {
            content: '▶';
            position: absolute;
            left: 0;
            color: #3498db;
        }

        /* Education */
        .education-item {
            background: linear-gradient(135deg, #f8f9fa, #e9ecef);
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 15px;
            border-left: 4px solid #e74c3c;
        }

        .degree {
            font-size: 1.2rem;
            color: #2c3e50;
            font-weight: bold;
        }

        .university {
            color: #e74c3c;
            font-weight: 600;
        }

        /* Languages */
        .languages-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        .language-item {
            background: white;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0,0,0,0.05);
            border-top: 4px solid #27ae60;
            transition: all 0.3s ease;
        }

        .language-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .language-name {
            font-size: 1.2rem;
            color: #2c3e50;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .language-level {
            background: linear-gradient(135deg, #27ae60, #2ecc71);
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
        }

        /* Certifications */
        .cert-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .cert-item {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.05);
            border-left: 4px solid #f39c12;
            transition: all 0.3s ease;
        }

        .cert-item:hover {
            transform: scale(1.02);
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .cert-name {
            font-weight: bold;
            color: #2c3e50;
            margin-bottom: 5px;
        }

        .cert-org {
            color: #f39c12;
            font-size: 0.9rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .container {
                margin: 10px;
                border-radius: 15px;
            }
            
            .header {
                padding: 30px 20px;
            }
            
            .header h1 {
                font-size: 2rem;
            }
            
            .contact-info {
                flex-direction: column;
                gap: 15px;
            }
            
            .main-content {
                padding: 30px 20px;
            }
            
            .skills-grid,
            .languages-grid,
            .cert-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Print styles */
        @media print {
            body {
                background: white;
                padding: 0;
            }
            
            .container {
                box-shadow: none;
                border-radius: 0;
            }
            
            .header {
                background: #2c3e50 !important;
                -webkit-print-color-adjust: exact;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <div class="header">
           
<div class="profile-image">
    <img src="./Ảnh selfie/IMG_5942.jpeg" alt="Avatar" style="width: 100%; height: 100%; border-radius: 50%;">
</div>
            <h1>ド タン サン<br>
             Đỗ Tấn Sang
            </h1>
            <div class="title"> 履歴書</div>
            <div class="contact-info">
                <div class="contact-item">
                    <span>📧メールアドレス</span>
                    <span><a href="mailto:sanglion147@gmail.com">Contact for Work</a></span>
                </div>
                <div class="contact-item">
                    <span>📱携帯電話番号</span>
                    <span>(+81) 7090803379</span>
                </div>
                <div class="contact-item">
                    <span>🌐　ウェブサイト</span>
                    <span><a href="https://www.resume.id/sangti">SangTi </a></span>
                </div>
                <div class="contact-item">
                    <span>📍出身</span>
                    <span>Đồng Nai, Vietnam</span>
                </div>
            </div>
        </div>

        <!-- Main Content -->
        <div class="main-content">
            <!-- Professional Summary -->
            <div class="section">
                <h2 class="section-title">Mind Set</h2>
                <div class="summary">
                    私はドタンサンと申します。ベトナムから参りました。
                    混乱な世の中に色々な業界を発展されました。<br>
                    必ず、自分の知識をアップデートしなければならないと思います。<br>
                    それで、テクノロジーの分野を選びました。
 

                   
                </div>
            </div>

            <!-- Technical Skills -->
            <div class="section">
                <h2 class="section-title">Technical Skills</h2>
                <div class="skills-grid">
                    <div class="skill-category">
                        <h4>Studying Programming Languages</h4>
                        <div class="skills-list">
                            <span class="skill-tag">Java</span>
                            <span class="skill-tag">JavaScript</span>
                            <span class="skill-tag">TypeScript</span>
                            <span class="skill-tag">PHP</span>
                            <span class="skill-tag">DataBase</span>
                            <span class="skill-tag">JavaSpring Framework</span>
                        </div>
                    </div>
                    <div class="skill-category">
                        <h4>Frameworks & Libraries</h4>
                        <div class="skills-list">
                            <span class="skill-tag">Spring Boot</span>
                             
                        </div>
                    </div>
                    <div class="skill-category">
                        <h4>Databases</h4>
                        <div class="skills-list">
                            <span class="skill-tag">MySQL</span>
                            
                        </div>
                    </div>
                    
                    </div>
                </div>
            </div>

            <!-- Work Experience -->
            <div class="section">
                <h2 class="section-title">Work Experience</h2>
                
                <div class="experience-item">
                    <div class="job-title">招き猫レストラン</div>
                    <div class="company"></div>
                    <div class="duration">2017年 12月 </div>
                    <ul class="achievements">
                        <li>
                        <li></li>
                    </ul>
                </div>

                <div class="experience-item">
                    <div class="job-title">ドンナイ チラシ株式会社</div>
                    <div class="company"></div>
                    <div class="duration">2019年　1月 </div>
                    <ul class="achievements">
                        
                        <li></li>
                    </ul>
                </div>

                <div class="experience-item">
                    <div class="job-title">スマートフォンオンラインショップ</div>
                    <div class="company"></div>
                    <div class="duration">2019年 7月　</div>
                    <ul class="achievements">
                        
                        <li></li>
                    </ul>
                </div>
                <div class="experience-item">
                    <div class="job-title">段ボールDucTai株式会社</div>
                    <div class="company"></div>
                    <div class="duration">2020年 1月</div>
                </div>
            </div>

            

            <!-- Languages -->
            <div class="section">
                <h2 class="section-title">Language Skills</h2>
                <div class="languages-grid">
                    <div class="language-item">
                        <div class="language-name">Vietnamese</div>
                        <div class="language-level">Native</div>
                    </div>
                    <div class="language-item">
                        <div class="language-name">English</div>
                        <div class="language-level"> (IELTS 5.5)</div>
                    </div>
                    <div class="language-item">
                        <div class="language-name">🇯🇵 Japanese</div>
                        <div class="language-level"> (JLPT N2)</div>
                    </div>
                </div>
            </div>

            <!-- Certifications -->
            <div class="section">
                <h2 class="section-title">Certifications</h2>
                <div class="cert-grid">
                    <div class="cert-item">
                        <div class="cert-name">J検3級</div>
                        <div class="cert-org"></div>
                    </div>
                    <div class="cert-item">
                        <div class="cert-name">Mos World</div>
                        <div class="cert-org"></div>
                    </div>
                    <div class="cert-item">
                        <div class="cert-name">Mos Excel</div>
                        <div class="cert-org"></div>
                    </div>
                    <div class="cert-item">
                        <div class="cert-name">JLPT N2 Certificate</div>
                        <div class="cert-org"></div>
                    </div>
                    <div class="cert-item">
                        <div class="cert-name">IELTS</div>
                        <div class="cert-org"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Add smooth scrolling and interactive effects
        document.addEventListener('DOMContentLoaded', function() {
            // Add click effects to skill tags
            const skillTags = document.querySelectorAll('.skill-tag');
            skillTags.forEach(tag => {
                tag.addEventListener('click', function() {
                    this.style.transform = 'scale(0.95)';
                    setTimeout(() => {
                        this.style.transform = 'scale(1.05)';
                        setTimeout(() => {
                            this.style.transform = 'scale(1)';
                        }, 100);
                    }, 100);
                });
            });

            // Add hover effects to sections
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => {
                section.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateX(10px)';
                    this.style.transition = 'transform 0.3s ease';
                });
                
                section.addEventListener('mouseleave', function() {
                    this.style.transform = 'translateX(0)';
                });
            });

            // Add print functionality
            const printBtn = document.createElement('button');
            printBtn.innerHTML = '🖨️ Print Resume';
            printBtn.style.position = 'fixed';
            printBtn.style.bottom = '20px';
            printBtn.style.right = '20px';
            printBtn.style.background = 'linear-gradient(135deg, #3498db, #2980b9)';
            printBtn.style.color = 'white';
            printBtn.style.border = 'none';
            printBtn.style.padding = '15px 20px';
            printBtn.style.borderRadius = '50px';
            printBtn.style.cursor = 'pointer';
            printBtn.style.fontSize = '14px';
            printBtn.style.fontWeight = 'bold';
            printBtn.style.boxShadow = '0 5px 15px rgba(52, 152, 219, 0.3)';
            printBtn.style.zIndex = '1000';
            printBtn.style.transition = 'all 0.3s ease';
            
            printBtn.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-5px)';
                this.style.boxShadow = '0 10px 25px rgba(52, 152, 219, 0.4)';
            });
            
            printBtn.addEventListener('mouseleave', function() {
                this.style.transform = 'translateY(0)';
                this.style.boxShadow = '0 5px 15px rgba(52, 152, 219, 0.3)';
            });
            
            printBtn.addEventListener('click', function() {
                window.print();
            });
            
            document.body.appendChild(printBtn);
        });
    </script>
</body>
</html>

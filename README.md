<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>صفحة GitHub - الملف الشخصي</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #1904E5;
            --secondary-color: #FAB2FF;
            --dark-color: #1a1a2e;
            --light-color: #f4f4f9;
            --gray-color: #6c757d;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light-color);
            color: var(--dark-color);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* رأس الصفحة */
        header {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 2rem 0;
            text-align: center;
            border-bottom-left-radius: 30px;
            border-bottom-right-radius: 30px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }
        
        .profile-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1.5rem;
        }
        
        .avatar {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid white;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
            background-color: #fff;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            color: var(--primary-color);
        }
        
        .profile-info h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }
        
        .profile-info p {
            font-size: 1.2rem;
            opacity: 0.9;
        }
        
        .stats {
            display: flex;
            gap: 2rem;
            margin-top: 1rem;
        }
        
        .stat {
            text-align: center;
        }
        
        .stat-value {
            font-size: 1.8rem;
            font-weight: bold;
        }
        
        .stat-label {
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        /* المحتوى الرئيسي */
        main {
            padding: 3rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 2rem;
            color: var(--primary-color);
            position: relative;
        }
        
        .section-title:after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            margin: 10px auto;
            border-radius: 2px;
        }
        
        .cards-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }
        
        .card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .card-header {
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 1rem;
            text-align: center;
        }
        
        .card-body {
            padding: 1.5rem;
        }
        
        .repo-stats {
            display: flex;
            justify-content: space-between;
            margin-top: 1rem;
            font-size: 0.9rem;
            color: var(--gray-color);
        }
        
        .language {
            display: inline-block;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background-color: var(--secondary-color);
            margin-right: 5px;
        }
        
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
            margin-top: 2rem;
        }
        
        .skill {
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 0.5rem 1.5rem;
            border-radius: 20px;
            font-weight: 500;
        }
        
        /* تذييل الصفحة */
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 2rem 0;
            text-align: center;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 1.5rem 0;
        }
        
        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            border-radius: 50%;
            color: white;
            text-decoration: none;
            font-size: 1.5rem;
            transition: transform 0.3s ease;
        }
        
        .social-link:hover {
            transform: scale(1.1);
        }
        
        /* تصميم متجاوب */
        @media (max-width: 768px) {
            .profile-container {
                flex-direction: column;
            }
            
            .stats {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .cards-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="profile-container">
                <div class="avatar">
                    <i class="fas fa-user"></i>
                </div>
                <div class="profile-info">
                    <h1>اسم المطور</h1>
                    <p>مطور ويب ومصمم واجهات مستخدم</p>
                    <div class="stats">
                        <div class="stat">
                            <div class="stat-value">24</div>
                            <div class="stat-label">المستودعات</div>
                        </div>
                        <div class="stat">
                            <div class="stat-value">142</div>
                            <div class="stat-label">المتابعون</div>
                        </div>
                        <div class="stat">
                            <div class="stat-value">56</div>
                            <div class="stat-label">المتابَعون</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>
    
    <main>
        <div class="container">
            <section class="repositories">
                <h2 class="section-title">المستودعات البارزة</h2>
                <div class="cards-container">
                    <div class="card">
                        <div class="card-header">
                            <h3>مشروع تطبيق الويب</h3>
                        </div>
                        <div class="card-body">
                            <p>وصف للمشروع يوضح الهدف منه والتقنيات المستخدمة في تطويره.</p>
                            <div class="repo-stats">
                                <span><i class="fas fa-star"></i> 42</span>
                                <span><i class="fas fa-code-branch"></i> 12</span>
                                <span><span class="language"></span> JavaScript</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <h3>مكتبة CSS</h3>
                        </div>
                        <div class="card-body">
                            <p>مكتبة CSS مخصصة تحتوي على مكونات جاهزة للاستخدام في المشاريع.</p>
                            <div class="repo-stats">
                                <span><i class="fas fa-star"></i> 28</span>
                                <span><i class="fas fa-code-branch"></i> 7</span>
                                <span><span class="language"></span> CSS</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <h3>أداة سطر الأوامر</h3>
                        </div>
                        <div class="card-body">
                            <p>أداة مساعدة لسطر الأوامر لتسهيل مهام التطوير اليومية.</p>
                            <div class="repo-stats">
                                <span><i class="fas fa-star"></i> 15</span>
                                <span><i class="fas fa-code-branch"></i> 3</span>
                                <span><span class="language"></span> Python</span>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
            
            <section class="skills">
                <h2 class="section-title">المهارات والتقنيات</h2>
                <div class="skills-container">
                    <div class="skill">HTML5</div>
                    <div class="skill">CSS3</div>
                    <div class="skill">JavaScript</div>
                    <div class="skill">React</div>
                    <div class="skill">Node.js</div>
                    <div class="skill">Python</div>
                    <div class="skill">Git</div>
                    <div class="skill">UI/UX Design</div>
                </div>
            </section>
        </div>
    </main>
    
    <footer>
        <div class="container">
            <h3>تواصل معي</h3>
            <div class="social-links">
                <a href="#" class="social-link"><i class="fab fa-github"></i></a>
                <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                <a href="#" class="social-link"><i class="fab fa-linkedin"></i></a>
                <a href="#" class="social-link"><i class="fas fa-envelope"></i></a>
            </div>
            <p>© 2023 جميع الحقوق محفوظة</p>
        </div>
    </footer>
    
    <script>
        // تأثيرات بسيطة بالجافا سكريبت
        document.addEventListener('DOMContentLoaded', function() {
            // إضافة تأثير عند التمرير
            const cards = document.querySelectorAll('.card');
            
            const observerOptions = {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            };
            
            const observer = new IntersectionObserver(function(entries) {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = 1;
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, observerOptions);
            
            cards.forEach(card => {
                card.style.opacity = 0;
                card.style.transform = 'translateY(20px)';
                card.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
                observer.observe(card);
            });
        });
    </script>
</body>
</html>

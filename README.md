<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的个人简介</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            text-align: center;
            padding: 50px 0;
            background-color: #3498db;
            color: white;
            border-radius: 8px;
            margin-bottom: 30px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid white;
            margin-bottom: 20px;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        .subtitle {
            font-size: 1.2rem;
            margin-bottom: 20px;
            font-weight: 300;
        }
        
        .social-links {
            margin-top: 15px;
        }
        
        .social-links a {
            display: inline-block;
            margin: 0 10px;
            color: white;
            text-decoration: none;
            font-size: 1.1rem;
        }
        
        .social-links a:hover {
            text-decoration: underline;
        }
        
        section {
            background-color: white;
            padding: 30px;
            margin-bottom: 30px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        
        h2 {
            color: #2c3e50;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #3498db;
        }
        
        .about-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }
        
        .about-text {
            flex: 2;
            min-width: 300px;
        }
        
        .personal-info {
            flex: 1;
            min-width: 250px;
        }
        
        .info-item {
            margin-bottom: 15px;
        }
        
        .info-item strong {
            display: inline-block;
            width: 100px;
            color: #3498db;
        }
        
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        .skill-item {
            background-color: #f0f0f0;
            padding: 10px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
        }
        
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .timeline-item {
            padding: 20px 30px;
            position: relative;
            background-color: inherit;
            width: 100%;
        }
        
        .timeline-item::before {
            content: '';
            position: absolute;
            width: 15px;
            height: 15px;
            background-color: #3498db;
            border-radius: 50%;
            left: 0;
            top: 25px;
        }
        
        .timeline-item::after {
            content: '';
            position: absolute;
            width: 2px;
            height: 100%;
            background-color: #ddd;
            left: 7px;
            top: 25px;
            z-index: -1;
        }
        
        .timeline-item:last-child::after {
            display: none;
        }
        
        .timeline-date {
            font-weight: bold;
            color: #3498db;
            margin-bottom: 5px;
        }
        
        .timeline-title {
            font-weight: bold;
            margin-bottom: 5px;
        }
        
        .contact-form {
            display: grid;
            gap: 15px;
        }
        
        .form-group {
            display: flex;
            flex-direction: column;
        }
        
        label {
            margin-bottom: 5px;
            font-weight: bold;
        }
        
        input, textarea {
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
        }
        
        textarea {
            min-height: 150px;
            resize: vertical;
        }
        
        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1rem;
            transition: background-color 0.3s;
        }
        
        button:hover {
            background-color: #2980b9;
        }
        
        footer {
            text-align: center;
            padding: 20px;
            background-color: #2c3e50;
            color: white;
            border-radius: 8px;
        }
        
        @media (max-width: 768px) {
            .about-content {
                flex-direction: column;
            }
            
            .timeline-item {
                padding-left: 20px;
            }
            
            .timeline-item::before {
                left: 0;
            }
            
            .timeline-item::after {
                left: 7px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <img src="https://via.placeholder.com/150" alt="个人照片" class="profile-img">
            <h1>张三</h1>
            <p class="subtitle">前端开发工程师 | UI设计师</p>
            <div class="social-links">
                <a href="#">微信</a>
                <a href="#">微博</a>
                <a href="#">GitHub</a>
                <a href="#">LinkedIn</a>
            </div>
        </header>
        
        <section id="about">
            <h2>关于我</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>你好！我是张三，一名充满激情的前端开发工程师和UI设计师。我热爱创造美观且用户友好的网站和应用程序。</p>
                    <p>我拥有5年的行业经验，专注于创建响应式、高性能的Web应用。我善于将复杂的问题简化，并通过创新的解决方案来提升用户体验。</p>
                    <p>在工作之余，我喜欢参与开源项目，学习新技术，并通过博客分享我的知识和经验。我相信持续学习和团队合作是成功的关键。</p>
                </div>
                <div class="personal-info">
                    <div class="info-item">
                        <strong>姓名：</strong> 张三
                    </div>
                    <div class="info-item">
                        <strong>年龄：</strong> 28岁
                    </div>
                    <div class="info-item">
                        <strong>所在地：</strong> 北京市
                    </div>
                    <div class="info-item">
                        <strong>邮箱：</strong> zhangsan@example.com
                    </div>
                    <div class="info-item">
                        <strong>电话：</strong> 138-xxxx-xxxx
                    </div>
                </div>
            </div>
        </section>
        
        <section id="skills">
            <h2>专业技能</h2>
            <div class="skills">
                <div class="skill-item">HTML5</div>
                <div class="skill-item">CSS3</div>
                <div class="skill-item">JavaScript</div>
                <div class="skill-item">React</div>
                <div class="skill-item">Vue.js</div>
                <div class="skill-item">Node.js</div>
                <div class="skill-item">UI/UX设计</div>
                <div class="skill-item">响应式设计</div>
                <div class="skill-item">Figma</div>
                <div class="skill-item">Photoshop</div>
                <div class="skill-item">Git</div>
                <div class="skill-item">Webpack</div>
            </div>
        </section>
        
        <section id="education">
            <h2>教育背景</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-date">2014 - 2018</div>
                    <div class="timeline-title">北京大学</div>
                    <div class="timeline-content">计算机科学与技术 学士学位</div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-date">2018 - 2020</div>
                    <div class="timeline-title">清华大学</div>
                    <div class="timeline-content">人机交互 硕士学位</div>
                </div>
            </div>
        </section>
        
        <section id="experience">
            <h2>工作经历</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-date">2020 - 至今</div>
                    <div class="timeline-title">ABC科技有限公司 - 高级前端开发</div>
                    <div class="timeline-content">
                        <p>负责公司核心产品的前端架构设计和开发，优化用户体验和页面性能。</p>
                        <p>带领5人前端团队，实施敏捷开发流程，提高团队协作效率。</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-date">2018 - 2020</div>
                    <div class="timeline-title">XYZ互联网公司 - 前端开发工程师</div>
                    <div class="timeline-content">
                        <p>参与多个Web应用项目的开发，使用React和Vue.js框架。</p>
                        <p>负责UI组件库的设计和实现，提高开发效率和产品一致性。</p>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="contact">
            <h2>联系我</h2>
            <form class="contact-form">
                <div class="form-group">
                    <label for="name">姓名</label>
                    <input type="text" id="name" name="name" required>
                </div>
                <div class="form-group">
                    <label for="email">邮箱</label>
                    <input type="email" id="email" name="email" required>
                </div>
                <div class="form-group">
                    <label for="subject">主题</label>
                    <input type="text" id="subject" name="subject" required>
                </div>
                <div class="form-group">
                    <label for="message">留言</label>
                    <textarea id="message" name="message" required></textarea>
                </div>
                <button type="submit">发送消息</button>
            </form>
        </section>
        
        <footer>
            <p>&copy; 2023 张三个人网站 - 保留所有权利</p>
        </footer>
    </div>
</body>
</html>

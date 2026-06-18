
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的个人主页</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Microsoft YaHei", sans-serif;
        }
        html {
            scroll-behavior: smooth;
        }
        body {
            background-color: #f5f7fa;
            color: #333;
        }
        /* 导航栏 */
        nav {
            width: 100%;
            height: 60px;
            background: #2563eb;
            position: fixed;
            top: 0;
            z-index: 999;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 40px;
        }
        nav a {
            color: #fff;
            text-decoration: none;
            font-size: 16px;
            transition: 0.3s;
        }
        nav a:hover {
            color: #bfdbfe;
        }
        section {
            padding: 80px 10%;
            min-height: 100vh;
        }
        /* 首页简介 */
        #home {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding-top: 120px;
        }
        .avatar {
            width: 160px;
            height: 160px;
            border-radius: 50%;
            background: #cbd5e1;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 48px;
            color: #64748b;
        }
        h1 {
            font-size: 36px;
            margin-bottom: 12px;
            color: #1e293b;
        }
        .desc {
            font-size: 18px;
            color: #64748b;
            max-width: 600px;
            line-height: 1.8;
        }
        /* 技能板块 */
        #skill h2, #project h2, #contact h2 {
            text-align: center;
            font-size: 28px;
            margin-bottom: 40px;
            color: #1e293b;
        }
        .skill-box {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px,1fr));
            gap: 24px;
        }
        .skill-item {
            background: #fff;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 2px 12px rgba(0,0,0,0.08);
            text-align: center;
        }
        .skill-item h3 {
            margin: 12px 0 8px;
            color: #2563eb;
        }
        /* 项目板块 */
        .project-box {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px,1fr));
            gap: 28px;
        }
        .project-card {
            background: #fff;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 2px 12px rgba(0,0,0,0.08);
        }
        .project-card .img {
            height: 160px;
            background: #e2e8f0;
        }
        .project-card .text {
            padding: 20px;
        }
        .project-card h3 {
            margin-bottom: 8px;
        }
        /* 联系方式 */
        #contact {
            text-align: center;
        }
        .contact-info {
            background: #fff;
            max-width: 500px;
            margin: 0 auto;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 2px 12px rgba(0,0,0,0.08);
        }
        .contact-info p {
            margin: 14px 0;
            font-size: 17px;
        }
        footer {
            text-align: center;
            padding: 20px;
            background: #1e293b;
            color: #fff;
            font-size: 14px;
        }
    </style>
</head>
<body>
    <!-- 导航栏 -->
    <nav>
        <a href=" ">首页</a >
        <a href="#skill">专业技能</a >
        <a href="#project">项目作品</a >
        <a href="#contact">联系我</a >
    </nav>

    <!-- 首页个人简介 -->
    <section id="home">
        <div class="avatar">我</div>
        <h1>张家乐 | 计算机专业学生</h1>
        <p class="desc">热爱前端网页开发，擅长HTML/CSS/JS静态页面制作，熟悉网页UI设计，正在学习静态网站部署与运维，这是我的个人展示单页网站。</p >
    </section>

    <!-- 技能板块 -->
    <section id="skill">
        <h2>我的专业技能</h2>
        <div class="skill-box">
            <div class="skill-item">
                <h3>HTML</h3>
                <p>页面结构搭建、语义化标签</p >
            </div>
            <div class="skill-item">
                <h3>CSS</h3>
                <p>响应式布局、动画、Flex/Grid</p >
            </div>
            <div class="skill-item">
                <h3>JavaScript</h3>
                <p>基础交互、页面动态效果</p >
            </div>
            <div class="skill-item">
                <h3>网页部署</h3>
                <p>Gitee/GitHub Pages静态站点上线</p >
            </div>
        </div>
    </section>

    <!-- 项目作品 -->
    <section id="project">
        <h2>项目作品</h2>
        <div class="project-box">
            <div class="project-card">
                <div class="img"></div>
                <div class="text">
                    <h3>个人单页官网</h3>
                    <p>本次期末作业，响应式个人介绍网站</p >
                </div>
            </div>
            <div class="project-card">
                <div class="img"></div>
                <div class="text">
                    <h3>简易商品展示页</h3>
                    <p>前端课程实训静态页面项目</p >
                </div>
            </div>
        </div>
    </section>

    <!-- 联系方式 -->
    <section id="contact">
        <h2>联系我</h2>
        <div class="contact-info">
            <p>学号：2025381045</p >
            <p>姓名：张家乐</p >
            <p>邮箱：2622124590@qq.com</p >
            <p>Gitee：gitee.com/你的用户名</p >
        </div>
    </section>

    <footer>
        © 2026 个人主页 | 期末大作业单页网站
    </footer>
</body>
</html>

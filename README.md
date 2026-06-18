<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>张家乐 · 个人主页</title>
    <style>
        /* ---------- 全局重置 ---------- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: #0a0a0a;      /* 全黑背景，稍微带一点深邃 */
            color: #ffffff;
            font-family: 'Segoe UI', 'PingFang SC', Roboto, 'Helvetica Neue', sans-serif;
            padding: 60px 80px 80px 130px;  /* 左留白大，实现“往右”效果 */
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        /* ---------- 容器 ---------- */
        .container {
            max-width: 1100px;
            width: 100%;
        }

        /* ---------- 头部 ---------- */
        .header {
            display: flex;
            align-items: center;
            gap: 28px;
            margin-bottom: 30px;
        }

        .avatar {
            width: 110px;
            height: 110px;
            background: #2a2a2a;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 56px;
            border: 2px solid #ffffff30;
            flex-shrink: 0;
        }

        .greeting {
            font-size: 76px;
            font-weight: 300;
            letter-spacing: 3px;
            line-height: 1.2;
        }

        .greeting span {
            font-weight: 600;
            background: linear-gradient(135deg, #f0e6a0, #ffffff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* ---------- 姓名 + 标语 ---------- */
        .name-block {
            margin-bottom: 18px;
        }

        .name {
            font-size: 62px;
            font-weight: 400;
            letter-spacing: 4px;
            margin-bottom: 6px;
        }

        .subtitle {
            font-size: 26px;
            font-weight: 200;
            color: #bbbbbb;
            letter-spacing: 2px;
        }

        /* ---------- 分隔装饰 ---------- */
        .divider {
            width: 70px;
            height: 2px;
            background: #ffffff40;
            margin: 28px 0 32px 0;
        }

        /* ---------- 简介 ---------- */
        .bio {
            font-size: 22px;
            font-weight: 300;
            line-height: 1.8;
            color: #dddddd;
            max-width: 720px;
            margin-bottom: 36px;
        }

        /* ---------- 技能标签 ---------- */
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 14px 20px;
            margin-bottom: 40px;
        }

        .skill-tag {
            background: #1e1e1e;
            padding: 8px 22px;
            border-radius: 30px;
            font-size: 18px;
            font-weight: 300;
            border: 1px solid #444444;
            letter-spacing: 1px;
            transition: 0.2s;
        }

        .skill-tag:hover {
            background: #2c2c2c;
            border-color: #aaaaaa;
        }

        /* ---------- 项目展示 ---------- */
        .projects {
            display: flex;
            flex-wrap: wrap;
            gap: 24px;
            margin-bottom: 44px;
        }

        .project-card {
            background: #141414;
            border: 1px solid #2a2a2a;
            border-radius: 12px;
            padding: 20px 28px;
            min-width: 200px;
            flex: 1 0 200px;
            transition: 0.25s;
        }

        .project-card:hover {
            background: #1e1e1e;
            border-color: #666;
            transform: translateY(-4px);
        }

        .project-card h3 {
            font-size: 24px;
            font-weight: 400;
            margin-bottom: 6px;
            letter-spacing: 1px;
        }

        .project-card p {
            font-size: 16px;
            color: #aaaaaa;
            font-weight: 300;
        }

        /* ---------- 联系方式 ---------- */
        .contact {
            display: flex;
            flex-wrap: wrap;
            gap: 24px 40px;
            margin-bottom: 28px;
        }

        .contact a {
            color: #ffffff;
            font-size: 20px;
            font-weight: 300;
            text-decoration: none;
            border-bottom: 1px solid transparent;
            transition: 0.2s;
            letter-spacing: 1px;
        }

        .contact a:hover {
            border-bottom-color: #ffffff;
            opacity: 0.8;
        }

        /* ---------- 进入按钮（保留） ---------- */
        .btn-enter {
            display: inline-block;
            color: #ffffff;
            background: transparent;
            border: 2px solid #ffffff;
            padding: 16px 52px;
            font-size: 30px;
            font-weight: 300;
            letter-spacing: 6px;
            text-decoration: none;
            cursor: pointer;
            transition: all 0.3s ease;
            border-radius: 2px;
            margin-top: 10px;
        }

        .btn-enter:hover {
            background: rgba(255, 255, 255, 0.06);
            border-color: #ccc;
            transform: scale(1.02);
        }

        /* ---------- 响应式 ---------- */
        @media (max-width: 800px) {
            body {
                padding: 40px 40px 60px 60px;
            }
            .greeting {
                font-size: 52px;
            }
            .name {
                font-size: 44px;
            }
            .bio {
                font-size: 19px;
            }
            .avatar {
                width: 80px;
                height: 80px;
                font-size: 40px;
            }
        }

        @media (max-width: 500px) {
            body {
                padding: 30px 20px 40px 30px;
            }
            .header {
                flex-wrap: wrap;
                gap: 14px;
            }
            .greeting {
                font-size: 38px;
            }
            .name {
                font-size: 32px;
            }
            .subtitle {
                font-size: 20px;
            }
            .btn-enter {
                font-size: 22px;
                padding: 12px 32px;
            }
            .project-card {
                flex: 1 0 100%;
            }
        }
    </style>
</head>
<body>

    <div class="container">
        <!-- 头像 + 问候语 -->
        <div class="header">
            <div class="avatar">👨‍💻</div>
            <div class="greeting">
                👋 <span>Hello</span>
            </div>
        </div>

        <!-- 姓名 + 标语 -->
        <div class="name-block">
            <div class="name">✨ I am 张家乐</div>
            <div class="subtitle">计算机应用技术 · 大一</div>
        </div>

        <div class="divider"></div>

        <!-- 简介 -->
        <div class="bio">
            热爱全栈开发与 AI 应用，享受从零构建产品的过程。<br />
            善于将复杂问题拆解为优雅的代码，保持好奇，持续学习。
        </div>

        <!-- 技能标签 -->
        <div class="skills">
            <span class="skill-tag">⚡ Python</span>
            <span class="skill-tag">⚡ JavaScript</span>
            <span class="skill-tag">⚡ React</span>
            <span class="skill-tag">⚡ Node.js</span>
            <span class="skill-tag">⚡ Docker</span>
            <span class="skill-tag">⚡ AI / LLM</span>
        </div>

        <!-- 项目展示 -->
        <div class="projects">
            <div class="project-card">
                <h3>📁 智能助手</h3>
                <p>基于大模型的对话式工具</p >
            </div>
            <div class="project-card">
                <h3>📁 个人博客</h3>
                <p>Vue3 + Vite 动态站点</p >
            </div>
            <div class="project-card">
                <h3>📁 数据看板</h3>
                <p>ECharts 可视化分析平台</p >
            </div>
        </div>

        <!-- 联系方式 -->
        <div class="contact">
            <a href=" ">📧 zhangjiale@example.com</a >
            <a href="#" target="_blank">🐙 GitHub</a >
            <a href="#" target="_blank">🔗 个人博客</a >
        </div>

        <!-- 进入按钮（保留，可当作 CTA） -->
        <a href="#" class="btn-enter">🚀 进入</a >
    </div>

</body>
</html>

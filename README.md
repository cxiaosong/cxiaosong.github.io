<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Personal webpage of Xiaosong Chang, Computer Science Researcher">
    <title>Xiaosong Chang - Computer Science Researcher</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600&family=Playfair+Display:wght@400;500&display=swap" rel="stylesheet">
    <style>
        h1 {
          display: none;
        }

        :root {
            --primary-color: #4a6fa5;
            --secondary-color: #6b8cae;
            --accent-color: #9fc2e3;
            --text-color: #3d3d3d;
            --light-text: #7a7a7a;
            --border-color: #e0e6ed;
            --bg-gradient: linear-gradient(135deg, #f5f7fa 0%, #e4e8f0 100%);
            --card-bg: rgba(255, 255, 255, 0.9);
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            line-height: 1.7;
            color: var(--text-color);
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
            background: var(--bg-gradient);
            background-attachment: fixed;
            background-size: cover;
            position: relative;
        }
        
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('https://images.unsplash.com/photo-1519681393784-d120267933ba?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') center/cover no-repeat;
            opacity: 0.05;
            z-index: -1;
        }
        
        .container {
            background: var(--card-bg);
            border-radius: 16px;
            box-shadow: 0 8px 32px rgba(31, 38, 135, 0.1);
            padding: 40px;
            margin: 40px auto;
            backdrop-filter: blur(4px);
            border: 1px solid rgba(255, 255, 255, 0.3);
        }
        
        h1, h2, h3 {
            font-family: 'Playfair Display', serif;
            color: var(--primary-color);
            margin-top: 1.8em;
            font-weight: 500;
        }
        
        h1 {
            border-bottom: 2px solid var(--accent-color);
            padding-bottom: 12px;
            margin-bottom: 30px;
            font-size: 2.2em;
            letter-spacing: 0.5px;
        }
        
        h2 {
            font-size: 1.6em;
            margin-bottom: 20px;
            padding-bottom: 8px;
            border-bottom: 1px solid var(--border-color);
            position: relative;
        }
        
        h2::after {
            content: "";
            position: absolute;
            left: 0;
            bottom: -1px;
            width: 60px;
            height: 2px;
            background: var(--accent-color);
        }
        
        h3 {
            font-size: 1.3em;
            margin-bottom: 15px;
            color: var(--secondary-color);
        }
        
        a {
            color: var(--primary-color);
            text-decoration: none;
            transition: all 0.3s ease;
            font-weight: 500;
        }
        
        a:hover {
            color: var(--secondary-color);
            text-decoration: underline;
        }
        
        .profile {
            display: flex;
            align-items: center;
            gap: 40px;
            margin-bottom: 40px;
            padding-bottom: 30px;
            border-bottom: 1px dashed var(--border-color);
        }
        
        .profile-img {
            width: 160px;
            height: 160px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid white;
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
        
        .profile-img:hover {
            transform: scale(1.03);
        }
        
        .profile-info {
            flex: 1;
        }
        
        .institution {
            font-weight: 600;
            margin-bottom: 8px;
            font-size: 1.1em;
            color: var(--primary-color);
        }
        
        .position {
            color: var(--light-text);
            margin-bottom: 12px;
            line-height: 1.6;
        }
        
        .contact {
            margin-top: 15px;
        }
        
        .research-focus {
            list-style-type: none;
            padding-left: 0;
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin: 20px 0;
        }
        
        .research-focus li {
            background: rgba(159, 194, 227, 0.2);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.95em;
            color: var(--primary-color);
            border: 1px solid var(--accent-color);
        }
        
        .tools-list, .projects-list, .papers-list {
            margin: 20px 0;
            padding-left: 20px;
        }
        
        .tools-list li, .projects-list li {
            margin-bottom: 12px;
            position: relative;
            padding-left: 25px;
        }
        
        .tools-list li::before, .projects-list li::before {
            content: "•";
            color: var(--accent-color);
            font-size: 1.5em;
            position: absolute;
            left: 0;
            top: -3px;
        }
        
        .experience-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        
        .experience-table tr {
            border-bottom: 1px dashed var(--border-color);
        }
        
        .experience-table td {
            padding: 15px 0;
            vertical-align: top;
        }
        
        .experience-table td:first-child {
            width: 200px;
            font-weight: 500;
            color: var(--primary-color);
        }
        
        .footer {
            text-align: right;
            margin-top: 50px;
            padding-top: 20px;
            border-top: 1px solid var(--border-color);
            color: var(--light-text);
            font-size: 0.9em;
        }
        
        @media (max-width: 768px) {
            .profile {
                flex-direction: column;
                gap: 20px;
                text-align: center;
            }
            
            .profile-img {
                width: 140px;
                height: 140px;
            }
            
            .experience-table td:first-child {
                width: 150px;
            }
            
            .container {
                padding: 25px;
                margin: 20px auto;
            }
        }
    </style>
</head>
<body>
    <div class="container">
       
        
        <div class="profile">
            <img src="123.png" alt="Xiaosong Chang" class="profile-img">
            <div class="profile-info">
                <div class="institution">
                    <a href="https://www.hebust.edu.cn/">Hebei University of Science and Technology</a>
                </div>
                <div class="position">
                    School of Information Science and Technology<br>
                    Master's Candidate in Computer Application Technology<br>
                    Intermediate Software Designer
                </div>
                <div class="contact">
                    Email: <a href="mailto:cxiaosong@foxmail.com">cxiaosong@foxmail.com</a>
                </div>
            </div>
        </div>
        
        <h2>Interests</h2>
        <p>Novels, Music, Movies</p>

        <h2>Research Focus</h2>
        <ul class="research-focus">
            <li>Software testing</li>
            <li>Program security</li>
            <li>Android malware detection</li>
            <li>Intelligent software Engineering</li>
        </ul>
        
        <h2>Technical Skills</h2>
        <ul class="tools-list">
            <li>Java</li>
            <li>Python</li>
            <li>Microservices</li>
            <li>Oracle, MySQL</li>
        </ul>
        
        <h2>Work Experience</h2>
        <table class="experience-table">
            <tr>
                <td>Dalian Tongfang</td>
                <td>Java Developer (Nov 2016 - Jul 2020)</td>
            </tr>
            <tr>
                <td>Kingdee</td>
                <td>Java Developer (Feb 2021 - Aug 2021)</td>
            </tr>
        </table>
        
        <h2>Utility Tools</h2>
        <ul class="tools-list">
            <li><a href="./作用：使用自动机识别论文中的错误的大小写以及空格问题.html">Paper Format Checker: Detecting case and spacing errors in academic papers</a></li>
            <li><a href="./DOS命令备份电脑关键位置到U盘.html">DOS Script for Backing Up Critical Files to USB Drive</a></li>
            <li><a href="./作用：根据关键字检索文件内容，输出文件列表.html">Content-based File Search Tool</a></li>
        </ul>
        
        <h2>Open Source Projects</h2>
        <ul class="projects-list">
            <li><a href="https://github.com/cxiaosong/RefactorMinerDemo">RefactorMiner Demo: Extracting method refactoring patterns from version history</a></li>
            <li><a href="https://github.com/cxiaosong/DeepLog">DeepLog 1.0: Deep Learning-based Log Recommendation System</a></li>
        </ul>
        
        <h2>Publications</h2>
        <div class="papers-list">
            <p>Yang Zhang, <strong>Xiaosong Chang</strong>, Lining Fang, Yifan Lu. (2023). "DeepLog: Deep-Learning-Based Log Recommendation." <em>Proceedings of 45th International Conference on Software Engineering (ICSE - DEMO Track)</em>, May 17-20, 2023, Melbourne, Australia.</p>
        </div>
        
        <div class="footer">
            Page last updated: September 28, 2022
        </div>
    </div>
</body>
</html>

<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>生日快乐</title>
    <style>
        body { 
            background: pink; 
            text-align: center; 
            padding-top: 100px;
            font-family: "Microsoft YaHei";
        }
        h1 { color: #d80073; }
    </style>
</head>
<body>
    <h1>🎂 生日快乐！[朋友名字] 🎂</h1>
    <p>愿你的每一天都如今天般灿烂美好！</p>
    <img src="birthday-photo.jpg" width="60%">

    <!-- 用于挂载 React 组件的容器 -->
    <div id="particles"></div>

    <!-- 引入 React 和 ReactDOM 的 CDN -->
    <script crossorigin src="https://unpkg.com/react@17/umd/react.production.min.js"></script>
    <script crossorigin src="https://unpkg.com/react-dom@17/umd/react-dom.production.min.js"></script>
    <!-- 如果希望直接在浏览器编译 JSX，还需要引入 Babel -->
    <script src="https://unpkg.com/@babel/standalone"></script>
    
    <!-- 定义你的 React 组件 -->
    <script type="text/babel">
        // 模拟 Particles 组件，你可以替换为实际使用的库
        function Particles({ params }) {
            // 这里你可以初始化 particles.js 或其他效果
            return <canvas style={{ width: "100%", height: "300px" }}>Particles 效果</canvas>;
        }
        
        const particleConfig = {
            particles: {
                number: { value: 80 },
                size: { value: 3, random: true },
                line_linked: { shadow: { enable: true } }
            },
            interactivity: { detect_on: "canvas", events: { onhover: { enable: true } } }
        };
        
        function Home() {
            return <Particles params={particleConfig} />;
        }
        
        ReactDOM.render(<Home />, document.getElementById('particles'));
    </script>
</body>
</html>

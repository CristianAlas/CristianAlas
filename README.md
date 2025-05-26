<h1 align="center">Cristian Alas 👨‍💻</h1>
<h3 align="center">Junior Software Developer</h3>

<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet">
    <title>Banner Perfil</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        .banner {
            width: 100%;
            height: 400px;
            background: linear-gradient(135deg, #0f0f0f 0%, #1a1a1a 50%, #0f0f0f 100%);
            position: relative;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: 'JetBrains Mono', 'Consolas', 'Monaco', monospace;
        }

        .geometric-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0.1;
        }

        .circle-1 {
            position: absolute;
            width: 200px;
            height: 200px;
            border: 2px solid #07F3EF;
            border-radius: 50%;
            top: -50px;
            left: -50px;

        }

        .circle-2 {
            position: absolute;
            width: 150px;
            height: 150px;
            border: 1px solid #07F3EF;
            border-radius: 50%;
            bottom: -30px;
            right: -30px;

        }

        .triangle {
            position: absolute;
            width: 0;
            height: 0;
            border-left: 40px solid transparent;
            border-right: 40px solid transparent;
            border-bottom: 60px solid #07F3EF;
            opacity: 0.3;
            top: 20%;
            right: 15%;

        }

        .content {
            text-align: center;
            z-index: 2;
            color: white;
        }

        .main-title {
            font-size: 4.2rem;
            font-weight: bold;
            color: #07F3EF;
            margin-bottom: 1.2rem;
            text-shadow: 0 0 20px rgba(7, 243, 239, 0.3);
            animation: glow 2s ease-in-out infinite alternate;
        }

        .subtitle {
            font-size: 1.8rem;
            color: #ffffff;
            margin-bottom: 1.8rem;
            opacity: 0.9;
        }

        .tags {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .tag {
            padding: 0.6rem 1.3rem;
            background: rgba(7, 243, 239, 0.1);
            border: 1px solid #07F3EF;
            border-radius: 25px;
            color: #07F3EF;
            font-size: 1rem;
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .tag:hover {
            background: rgba(7, 243, 239, 0.2);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(7, 243, 239, 0.3);
        }

        .floating-dots {
            position: absolute;
            width: 100%;
            height: 100%;
        }

        .dot {
            position: absolute;
            width: 4px;
            height: 4px;
            background: #07F3EF;
            border-radius: 50%;

        }

        .dot:nth-child(1) { top: 20%; left: 10%; animation-delay: 0s; }
        .dot:nth-child(2) { top: 60%; left: 85%; animation-delay: 2s; }
        .dot:nth-child(3) { top: 80%; left: 20%; animation-delay: 4s; }
        .dot:nth-child(4) { top: 30%; left: 70%; animation-delay: 1s; }
        .dot:nth-child(5) { top: 70%; left: 60%; animation-delay: 3s; }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        @keyframes rotate-reverse {
            from { transform: rotate(360deg); }
            to { transform: rotate(0deg); }
        }

        @keyframes glow {
            from { text-shadow: 0 0 20px rgba(7, 243, 239, 0.3); }
            to { text-shadow: 0 0 30px rgba(7, 243, 239, 0.6), 0 0 40px rgba(7, 243, 239, 0.4); }
        }

        @keyframes pulse {
            0%, 100% { opacity: 0.3; transform: scale(1); }
            50% { opacity: 0.6; transform: scale(1.1); }
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) scale(1); opacity: 0.7; }
            50% { transform: translateY(-20px) scale(1.2); opacity: 1; }
        }

        .code-symbols {
            position: absolute;
            width: 100%;
            height: 100%;
            font-family: 'JetBrains Mono', monospace;
            font-size: 1.2rem;
            color: #07F3EF;
            opacity: 0.15;
        }

        .symbol {
            position: absolute;

        }

        .symbol:nth-child(1) { top: 15%; left: 8%; animation-delay: 0s; }
        .symbol:nth-child(2) { top: 25%; right: 12%; animation-delay: 1s; }
        .symbol:nth-child(3) { bottom: 20%; left: 15%; animation-delay: 2s; }
        .symbol:nth-child(4) { top: 70%; right: 20%; animation-delay: 3s; }
        .symbol:nth-child(5) { top: 45%; left: 5%; animation-delay: 4s; }
        .symbol:nth-child(6) { bottom: 35%; right: 8%; animation-delay: 5s; }

        @keyframes code-float {
            0%, 100% { 
                transform: translateY(0px) rotate(0deg); 
                opacity: 0.15; 
            }
            25% { 
                transform: translateY(-15px) rotate(5deg); 
                opacity: 0.25; 
            }
            50% { 
                transform: translateY(-25px) rotate(-3deg); 
                opacity: 0.3; 
            }
            75% { 
                transform: translateY(-10px) rotate(2deg); 
                opacity: 0.2; 
            }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .main-title {
                font-size: 3rem;
            }
            .subtitle {
                font-size: 1.4rem;
            }
            .tags {
                gap: 0.5rem;
            }
            .tag {
                font-size: 0.9rem;
                padding: 0.5rem 1rem;
            }
        }
    </style>
</head>
<body>
    <div class="banner">
        <div class="geometric-bg">
            <div class="circle-1"></div>
            <div class="circle-2"></div>
            <div class="triangle"></div>
        </div>
        
        <div class="code-symbols">
            <div class="symbol">&lt;/&gt;</div>
            <div class="symbol">{}</div>
            <div class="symbol">()</div>
            <div class="symbol">[];</div>
            <div class="symbol">&&</div>
            <div class="symbol">!=</div>
        </div>
        
        <div class="floating-dots">
            <div class="dot"></div>
            <div class="dot"></div>
            <div class="dot"></div>
            <div class="dot"></div>
            <div class="dot"></div>
        </div>
        
        <div class="content">
            <h1 class="main-title">Cristian Alas</h1>
            <p class="subtitle">Junior Software Developer</p>
            <div class="tags">
                <span class="tag">Frontend</span>
                <span class="tag">Backend</span>
                <span class="tag">Security</span>
                <span class="tag">Database</span>
            </div>
        </div>
    </div>
</body>
</html>

# 💫 About Me

### ¡Hola y bienvenido a mi perfil! 👋

Soy un desarrollador full stack de 25 años, originario de El Salvador, con una gran pasión por la tecnología y el desarrollo de software. Me encanta aprender constantemente, asumir nuevos retos y trabajar en proyectos que me permitan crecer y aportar soluciones innovadoras.

Estoy siempre abierto a nuevas ideas y colaboraciones, así que no dudes en explorar mis repositorios o contactarme si te interesa trabajar juntos.

¡Gracias por visitar mi perfil! 🚀

---

# 💻 Tech Stack

### 🧠 Lenguajes, Frameworks y Herramientas que uso:

![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) 
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Next JS](https://img.shields.io/badge/next.js-%23000000.svg?style=for-the-badge&logo=next.js&logoColor=white)
![Angular](https://img.shields.io/badge/angular-%23DD0031.svg?style=for-the-badge&logo=angular&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)

![Spring Boot](https://img.shields.io/badge/spring%20boot-%236DB33F.svg?style=for-the-badge&logo=springboot&logoColor=white)
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=c-sharp&logoColor=white)
![.NET Framework](https://img.shields.io/badge/.NET_Framework-%23512BD4.svg?style=for-the-badge&logo=.net&logoColor=white)

![PostgreSQL](https://img.shields.io/badge/postgresql-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![SQL Server](https://img.shields.io/badge/sql%20server-%23CC2927.svg?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)
![MySQL](https://img.shields.io/badge/mysql-%2300000f.svg?style=for-the-badge&logo=mysql&logoColor=white)

![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![JWT](https://img.shields.io/badge/jwt-black?style=for-the-badge&logo=JSON%20web%20tokens)

![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![Bootstrap](https://img.shields.io/badge/bootstrap-%238511FA.svg?style=for-the-badge&logo=bootstrap&logoColor=white)

---

# 🌐 Mis Enlaces

[![Portafolio](https://img.shields.io/badge/Portafolio-222222?style=for-the-badge&logo=vercel&logoColor=white)](https://crsitian-portafolio.vercel.app/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/cristian-alfredo-alas-castellanos-1633732aa/)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/cristian_alas16/)

---

# 🎥 Demo / Video

Sistema Gestor de Inventario: Gestión de Usuarios, Gestión de Compras, Recepciones y Ventas, Implementado Spring Security y JWT:

[![YouTube Video](https://img.shields.io/badge/Ver%20en-YouTube-red?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=O-RILwe75vg)

---

# 📊 GitHub Stats

![](https://github-readme-stats.vercel.app/api?username=CristianAlas&theme=tokyonight&hide_border=false&include_all_commits=true&count_private=true)<br/>
![](https://github-readme-streak-stats.herokuapp.com/?user=CristianAlas&theme=tokyonight&hide_border=false)<br/>
![](https://github-readme-stats.vercel.app/api/top-langs/?username=CristianAlas&theme=tokyonight&hide_border=false&layout=compact)

---

### 🔝 Top Contributed Repo

![](https://github-contributor-stats.vercel.app/api?username=CristianAlas&limit=5&theme=dark&combine_all_yearly_contributions=true)

---

[![](https://visitcount.itsvg.in/api?id=CristianAlas&icon=2&color=6)](https://visitcount.itsvg.in)

<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->

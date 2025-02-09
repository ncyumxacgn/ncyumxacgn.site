# 創造者

A Pen created on CodePen.

Original CODE: 
"
<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>嘉大民雄動漫社</title>
    <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Nunito', sans-serif;
            line-height: 1.6;
            background: linear-gradient(135deg, #f5f7fa, #c3cfe2);
            color: #333;
            overflow-x: hidden;
        }

        header {
            background: linear-gradient(135deg, #6a11cb, #2575fc);
            color: white;
            padding: 2rem 1rem;
            text-align: center;
            position: relative;
        }

        header h1 {
            font-size: 3rem;
            margin-bottom: 0.5rem;
        }

        header p {
            font-size: 1.5rem;
            font-weight: 300;
        }

        nav {
            display: flex;
            justify-content: center;
            background: #333;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        nav a {
            color: white;
            padding: 1rem;
            text-decoration: none;
            transition: background 0.3s ease;
        }

        nav a:hover {
            background: #575757;
        }

        section {
            padding: 4rem 2rem;
            text-align: center;
        }

        section:nth-child(even) {
            background: #f0f4f8;
        }

        h2 {
            font-size: 2.5rem;
            color: #6a11cb;
            margin-bottom: 1rem;
        }

        p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }

        .contact a {
            display: inline-block;
            margin: 0.5rem;
            color: #2575fc;
            font-weight: bold;
            text-decoration: none;
            border: 2px solid #2575fc;
            padding: 0.5rem 1rem;
            border-radius: 25px;
            transition: background 0.3s, color 0.3s;
        }

        .contact a:hover {
            background: #2575fc;
            color: white;
        }

        #backToTop {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: #6a11cb;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 50%;
            cursor: pointer;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            display: none;
        }

        .shape {
            position: absolute;
            width: 50px;
            height: 50px;
            opacity: 0.3;
        }

        .triangle {
            clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
            background: #6a11cb;
        }

        .square {
            background: #2575fc;
        }

        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0); }
        }
    </style>
</head>
<body>
    <header>
        <h1>嘉大民雄動漫社</h1>
        <p>讓動漫成為我們的共同語言！</p>
    </header>

    <nav>
        <a href="#about">社團介紹</a>
        <a href="#activities">活動資訊</a>
        <a href="#contact">聯絡我們</a>
    </nav>

    <section id="about">
        <h2>社團介紹</h2>
        <p>我們是嘉義大學民雄動漫社，致力於推廣動畫、漫畫、遊戲及小說（ACGN）文化，歡迎所有喜愛動漫、漫畫、遊戲和Cosplay的朋友加入我們的大家庭！</p>
    </section>

    <section id="activities">
        <h2>活動資訊</h2>
        <p>每週四晚上 19:00-22:00，我們在嘉義大學民雄校區人文館J101舉辦各種精彩活動，包含繪畫、寫作、遊戲交流及Cos道具製作等，歡迎參加！</p>
    </section>

    <section id="contact">
        <h2>聯絡我們</h2>
        <div class="contact">
            <a href="https://discord.com/invite/uWab7j7g9U" target="_blank">加入Discord</a>
            <a href="mailto:ncyumxacgn@gmail.com">寄送Email</a>
            <a href="https://www.instagram.com/ncyu_mx_acgn/" target="_blank">追蹤Instagram</a>
            <a href="https://www.facebook.com/profile.php?id=61559429451140" target="_blank">按讚Facebook</a>
        </div>
    </section>

    <button id="backToTop">⬆</button>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const backToTopButton = document.getElementById('backToTop');

            window.addEventListener('scroll', () => {
                if (window.scrollY > 300) {
                    backToTopButton.style.display = 'block';
                } else {
                    backToTopButton.style.display = 'none';
                }
            });

            backToTopButton.addEventListener('click', () => {
                window.scrollTo({ top: 0, behavior: 'smooth' });
            });

            const shapes = ['triangle', 'square'];
            const numShapes = Math.floor(Math.random() * (8 - 4 + 1)) + 4;

            for (let i = 0; i < numShapes; i++) {
                const shape = document.createElement('div');
                shape.classList.add('shape', shapes[Math.floor(Math.random() * shapes.length)]);
                shape.style.left = `${Math.random() * 100}vw`;
                shape.style.top = `${Math.random() * 100}vh`;
                shape.style.animation = `float ${Math.random() * 5 + 5}s ease-in-out infinite`;

                document.body.appendChild(shape);
            }
        });
    </script>
</body>
</html>
"

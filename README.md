<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>GitHub Profile</title>
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            background-color: #F5F5F5;
            color: #333;
            margin: 0;
            padding: 0;
        }
        .container {
            display: flex;
            align-items: center;
            margin: 2em;
            background: #FFFFFF;
            border-radius: 8px;
            box-shadow: 0px 3px 1px -2px rgba(0,0,0,0.2),
                        0px 2px 2px 0px rgba(0,0,0,0.14),
                        0px 1px 5px 0px rgba(0,0,0,0.12);
        }
        .text {
            margin: 20px;
            flex: 1;
        }
        h2 {
            font-size: 24px;
            margin-bottom: 20px;
            font-weight: 400;
        }
        img {
            max-width: 300px;
            border-top-left-radius: 8px;
            border-bottom-left-radius: 8px;
        }
        ul {
            list-style-type: none;
            padding-left: 0;
        }
        ul li {
            background: #E0E0E0;
            margin: 8px 0;
            padding: 10px;
            border-radius: 4px;
        }
    </style>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const speed = 100;
            const deleteSpeed = 50;
            const delay = 1000;

            document.querySelectorAll('h2').forEach((element) => {
                const text = element.textContent;
                element.textContent = '';

                const typeText = (index) => {
                    if (index < text.length) {
                        element.textContent += text[index];
                        setTimeout(() => typeText(index + 1), speed);
                    } else {
                        setTimeout(() => deleteText(index - 1), delay);
                    }
                };

                const deleteText = (index) => {
                    if (index > 0) {
                        element.textContent = element.textContent.substring(0, index);
                        setTimeout(() => deleteText(index - 1), deleteSpeed);
                    } else {
                        element.innerHTML = '&nbsp;'; // Use a non-breaking space instead of making it completely empty
                        setTimeout(() => typeText(0), delay);
                    }
                };

                typeText(0);
            });
        });
    </script>
</head>
<body>

    <!-- First Section: Developer Typing -->
    <div class="container">
        <img src="https://i.giphy.com/media/5eLDrEaRGHegx2FeF2/giphy.webp" alt="Developer Typing">
        <div class="text">
            <h2>About Me</h2>
            <p>I'm a Fullstack Software Engineer passionate about solving complex problems and creating efficient solutions. With experience at companies like SAP, Amazon AWS, and currently at Flexport Inc., I love working on platform-level code and am enthusiastic about startups and SaaS.</p>
        </div>
    </div>

    <!-- Second Section: Cat Typing -->
    <div class="container" style="flex-direction: row-reverse;">
        <img src="https://i.giphy.com/media/M4NykXxUE0HAcK7UJ6/giphy.webp" alt="Cat Typing">
        <div class="text">
            <h2>Languages I'm Proficient In</h2>
            <ul>
                <li>JavaScript</li>
                <li>Python</li>
                <li>Java</li>
                <li>C++</li>
                <li>Go</li>
            </ul>
        </div>
    </div>

    <!-- Third Section: Earth -->
    <div class="container">
        <img src="https://i.giphy.com/media/ehIc2Rb3HRrb1YiQBr/giphy.webp" alt="Earth">
        <div class="text">
            <h2>Open Source Contributions</h2>
            <p>I love creating open-source projects that people love to use.</p>
            <img src="https://github-readme-stats.vercel.app/api?username=yourusername&show_icons=true" alt="Your GitHub Stats">
        </div>
    </div>

</body>
</html>

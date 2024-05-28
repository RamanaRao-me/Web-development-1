
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
    <style>
        :root {
            --background-color: #f4f4f4;
            --text-color: #333;
            --header-background: #333;
            --header-text-color: white;
            --button-background: #333;
            --button-text-color: white;
        }

        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            background-color: var(--background-color);
            color: var(--text-color);
        }

        header {
            background-color: var(--header-background);
            color: var(--header-text-color);
            padding: 1rem 0;
            text-align: center;
        }

        header h1 {
            margin: 0;
        }

        nav ul {
            list-style: none;
            padding: 0;
        }

        nav ul li {
            display: inline;
            margin: 0 10px;
        }

        nav ul li a {
            color: var(--header-text-color);
            text-decoration: none;
        }

        #theme-toggle {
            background-color: var(--button-background);
            color: var(--button-text-color);
            border: none;
            padding: 0.5rem 1rem;
            cursor: pointer;
            margin-top: 10px;
        }

        section {
            padding: 2rem;
            margin: 1rem 0;
        }

        #about, #skills, #projects, #contact {
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            padding: 2rem;
        }

        h2 {
            margin-top: 0;
        }

        ul {
            list-style: none;
            padding: 0;
        }

        ul li {
            background: var(--header-background);
            color: var(--header-text-color);
            display: inline-block;
            margin: 0.5rem;
            padding: 0.5rem 1rem;
            border-radius: 5px;
        }

        .project {
            margin: 1rem 0;
        }

        footer {
            text-align: center;
            padding: 1rem 0;
            background-color: var(--header-background);
            color: var(--header-text-color);
            position: fixed;
            width: 100%;
            bottom: 0;
        }

        /* Dark theme */
        body.dark {
            --background-color: #333;
            --text-color: #f4f4f4;
            --header-background: #f4f4f4;
            --header-text-color: #333;
            --button-background: #f4f4f4;
            --button-text-color: #333;
        }
    </style>
</head>
<body>
    <header>
        <h1>Ramana Rao</h1>
        <nav>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
        <button id="theme-toggle">Toggle Theme</button>
    </header>
    
    <section id="about">
        <h2>About Me</h2>
        <p>Hi, I'm Ramana, a web developer with a passion for creating beautiful and functional websites. I have experience with HTML, CSS, JavaScript, and various frameworks.</p>
    </section>
    
    <section id="skills">
        <h2>Skills</h2>
        <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>JavaScript</li>
            <li>React</li>
            <li>Node.js</li>
        </ul>
    </section>
    
    <section id="projects">
        <h2>Projects</h2>
        <div class="project">
            <h3>Project One</h3>
            <p>Description of project one. This project showcases my skills in HTML and CSS.</p>
        </div>
        <div class="project">
            <h3>Project Two</h3>
            <p>Description of project two. This project showcases my skills in JavaScript and React.</p>
        </div>
    </section>
    
    <section id="contact">
        <h2>Contact</h2>
        <p>Email: ramanaraogv2002@gmail.com</p>
        <p>LinkedIn: <a href="https://www.linkedin.com/in/ramanarao">John Doe</a></p>
    </section>
    
    <footer>
        <p>&copy; 2024 John Doe. All rights reserved.</p>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('nav ul li a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Theme toggle
        const themeToggleBtn = document.getElementById('theme-toggle');
        themeToggleBtn.addEventListener('click', () => {
            document.body.classList.toggle('dark');
        });
    </script>
</body>
</html>

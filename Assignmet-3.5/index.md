Here is the complete source code for your Personal Portfolio & Blog Website mini-project. This project ties together everything you've learned so far—combining semantic HTML tags, accessible navigation, lists, images, internal section links, and clean styling.

To keep everything simple and self-contained, this solution is structured as a single-file website (index.html) with working internal anchor links, clean indentation, and responsive design.

index.html (Complete Portfolio & Blog Code)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alex Morgan - Developer Portfolio & Blog</title>
    <style>
        :root {
            --primary-color: #1a2a3a;
            --accent-color: #0066cc;
            --bg-color: #f8f9fa;
            --text-color: #333333;
            --card-bg: #ffffff;
        }

        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            color: var(--text-color);
            background-color: var(--bg-color);
        }

        /* Header & Navigation */
        header {
            background-color: var(--primary-color);
            color: #fff;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: #fff;
            text-decoration: none;
        }

        nav ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
            gap: 20px;
        }

        nav a {
            color: #fff;
            text-decoration: none;
            font-weight: 600;
            transition: color 0.2s;
        }

        nav a:hover, nav a:focus {
            color: #66b3ff;
            text-decoration: underline;
        }

        /* Main Container */
        main {
            max-width: 1000px;
            margin: 30px auto;
            padding: 0 20px;
        }

        section {
            background: var(--card-bg);
            padding: 30px;
            margin-bottom: 30px;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
        }

        h2 {
            color: var(--primary-color);
            border-bottom: 2px solid var(--accent-color);
            padding-bottom: 8px;
            margin-top: 0;
        }

        /* About Section */
        .about-content {
            display: flex;
            gap: 30px;
            align-items: center;
            flex-wrap: wrap;
        }

        .profile-img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--accent-color);
        }

        .about-text {
            flex: 1;
            min-width: 280px;
        }

        /* Skills / Interests Lists */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .skills-grid ul {
            padding-left: 20px;
        }

        /* Projects / Blog Posts */
        article {
            background: #fdfdfd;
            border: 1px solid #e0e0e0;
            padding: 20px;
            border-radius: 6px;
            margin-bottom: 20px;
        }

        article h3 {
            margin-top: 0;
            color: var(--accent-color);
        }

        .project-img {
            max-width: 100%;
            height: auto;
            border-radius: 4px;
            margin-top: 10px;
        }

        .meta {
            font-size: 0.85rem;
            color: #666;
            margin-bottom: 10px;
        }

        /* Useful Links List */
        .links-list {
            list-style-type: square;
            padding-left: 20px;
        }

        .links-list li {
            margin-bottom: 8px;
        }

        .links-list a {
            color: var(--accent-color);
            text-decoration: none;
        }

        .links-list a:hover {
            text-decoration: underline;
        }

        /* Footer */
        footer {
            background-color: var(--primary-color);
            color: #fff;
            text-align: center;
            padding: 30px 20px;
            margin-top: 40px;
        }

        footer p {
            margin: 5px 0;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            header {
                flex-direction: column;
                gap: 15px;
            }
            nav ul {
                gap: 15px;
            }
            .about-content {
                flex-direction: column;
                text-align: center;
            }
        }
    </style>
</head>
<body>

    <!-- Header & Navigation Bar -->
    <header>
        <a href="#about" class="logo">Alex Morgan</a>
        <nav aria-label="Main Navigation">
            <ul>
                <li><a href="#about">About Me</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#blog">Blog</a></li>
                <li><a href="#links">Links</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <!-- About Me Section -->
        <section id="about">
            <h2>About Me</h2>
            <div class="about-content">
                <img src="https://via.placeholder.com/180" alt="Professional portrait photograph of Alex Morgan smiling" class="profile-img">
                <div class="about-text">
                    <p>
                        Hello! I'm <strong>Alex Morgan</strong>, a passionate web development student and aspiring software engineer. 
                        I love building clean, accessible, and user-friendly web interfaces using modern HTML5, CSS3, and JavaScript. 
                        When I'm not coding, you can find me exploring open-source projects or reading about computer science fundamentals.
                    </p>
                    <p>
                        Welcome to my personal portfolio and blog where I share my ongoing projects, coding notes, and useful learning resources.
                    </p>
                </div>
            </div>
        </section>

        <!-- Skills or Interests Section -->
        <section id="skills">
            <h2>Skills & Technical Interests</h2>
            <div class="skills-grid">
                <div>
                    <h3>Core Technologies</h3>
                    <ul>
                        <li>HTML5 & Semantic Web Markup</li>
                        <li>CSS3 (Flexbox, Grid, Responsive Design)</li>
                        <li>JavaScript (ES6+) & DOM Manipulation</li>
                        <li>Git & GitHub Version Control</li>
                    </ul>
                </div>
                <div>
                    <h3>Interests & Learning Goals</h3>
                    <ul>
                        <li>Web Accessibility (a11y) Best Practices</li>
                        <li>UI/UX Prototyping & Wireframing</li>
                        <li>Basic Backend Integration (Node.js)</li>
                        <li>Responsive Mobile-First Architecture</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Projects Section -->
        <section id="projects">
            <h2>Featured Projects</h2>
            
            <article>
                <h3>Project 1: Interactive Task Planner</h3>
                <p class="meta">Built with Vanilla JavaScript, HTML5, and CSS3</p>
                <img src="https://via.placeholder.com/800x400" alt="Screenshot of the Task Planner web application showing active lists and task completion interface" class="project-img">
                <p>
                    A fully responsive task management application allowing users to add, prioritize, and check off daily todos 
                    with data persistence using browser LocalStorage.
                </p>
                <a href="https://github.com" target="_blank" rel="noopener">View Source on GitHub</a>
            </article>

            <article>
                <h3>Project 2: University Campus Guide</h3>
                <p class="meta">Built with Semantic HTML5 and CSS Grid</p>
                <img src="https://via.placeholder.com/800x400" alt="Screenshot of the University Campus Guide homepage with navigation headers and department sections" class="project-img">
                <p>
                    An accessible informational portal structured using semantic HTML tags (`&lt;main&gt;`, `&lt;article&gt;`, `&lt;aside&gt;`), 
                    featuring campus maps and department details.
                </p>
                <a href="https://github.com" target="_blank" rel="noopener">View Source on GitHub</a>
            </article>
        </section>

        <!-- Blog Posts Section -->
        <section id="blog">
            <h2>Latest Blog Posts</h2>
            
            <article>
                <h3>Why Semantic HTML Matters for Accessibility</h3>
                <p class="meta">Published on <time datetime="2026-10-24">October 24, 2026</time> | 5 min read</p>
                <p>
                    Transitioning away from generic <code>&lt;div&gt;</code> elements to meaningful structural tags like 
                    <code>&lt;header&gt;</code>, <code>&lt;nav&gt;</code>, and <code>&lt;article&gt;</code> dramatically improves 
                    screen reader compatibility and helps search engines index your content correctly.
                </p>
            </article>

            <article>
                <h3>Getting Started with CSS Grid Layouts</h3>
                <p class="meta">Published on <time datetime="2026-10-15">October 15, 2026</time> | 4 min read</p>
                <p>
                    A quick beginner's guide to mastering two-dimensional layouts with CSS Grid, helping you build complex, 
                    responsive web designs with minimal code.
                </p>
            </article>
        </section>

        <!-- Useful Links Section -->
        <section id="links">
            <h2>Useful Links & Resources</h2>
            <ul class="links-list">
                <li><a href="https://developer.mozilla.org" target="_blank" rel="noopener">MDN Web Docs — Comprehensive web development reference</a></li>
                <li><a href="https://github.com" target="_blank" rel="noopener">GitHub — Code hosting and repository management</a></li>
                <li><a href="https://www.w3.org/WAI/" target="_blank" rel="noopener">W3C Web Accessibility Initiative (WAI)</a></li>
                <li><a href="https://css-tricks.com" target="_blank" rel="noopener">CSS-Tricks — Guides and tutorials on CSS layout techniques</a></li>
            </ul>
        </section>
    </main>

    <!-- Footer with Contact Details -->
    <footer id="contact">
        <h2>Get in Touch</h2>
        <p>Email: <a href="mailto:alex.morgan@example.com" style="color: #66b3ff;">alex.morgan@example.com</a></p>
        <p>GitHub: <a href="https://github.com" target="_blank" rel="noopener" style="color: #66b3ff;">github.com/alex-morgan</a></p>
        <p>Location: San Francisco, CA</p>
        <p style="margin-top: 20px; font-size: 0.9rem; color: #aaa;">&copy; 2026 Alex Morgan. All rights reserved.</p>
    </footer>

</body>
</html>
Assignment Requirements Checklist
Header with name/logo: Included at the top (<header> with Alex Morgan logo/name).

Navigation bar: Fully functional sticky navigation bar linking directly to page sections via anchor IDs (#about, #skills, #projects, #blog, #links, #contact).

About Me: Dedicated introductory section with profile image and bio.

Skills or Interests: Categorized list covering core technologies and learning goals.

Blog posts or projects: Dedicated sections featuring styled articles with metadata, images, and descriptions.

Images: Integrated placeholder images (<img src="...">) with descriptive alt texts for accessibility.

Useful links: Styled list of external web development resources with target and security attributes (target="_blank" rel="noopener").

Footer with contact details: Includes email, GitHub handle, location, and copyright notice.

Semantic HTML & Clean Code: Uses HTML5 structural elements (<header>, <nav>, <main>, <section>, <article>, <footer>) with clean indentation and responsive CSS styling.

How to Complete Your Submission
Save the code above as index.html on your computer.

Double-click index.html to test it in your web browser and ensure all navigation links jump smoothly to their respective sections.

Push your project code to a public GitHub Repository (naming it something like portfolio-mini-project).

Submit your source code (index.html), a browser screenshot, and your GitHub repository link to your instructor.
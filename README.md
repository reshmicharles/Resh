<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1.0"/>
  <title>reshmi's Portfolio</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; font-family: Arial, sans-serif; }
    body { line-height: 1.6; background: #f9f9f9; color: #333; }

    /* Navbar */
    header { background: #333; color: #fff; padding: 1rem; position: sticky; top: 0; z-index: 1000; }
    nav { display: flex; justify-content: space-between; align-items: center; }
    nav .logo { font-size: 1.5rem; font-weight: bold; }
    nav ul { list-style: none; display: flex; gap: 1rem; }
    nav a { color: #fff; text-decoration: none; }
    nav a:hover { text-decoration: underline; }

    /* Sections */
    section { padding: 2rem; }
    .hero { display: flex; justify-content: center; align-items: center; text-align: center; height: 90vh; background: #eee; }
    .hero h1 span { color: #0077cc; }

    .about-content { display: flex; gap: 1rem; align-items: center; }
    .about-content img { width: 150px; border-radius: 50%; }

    .projects .project-grid { display: grid; grid-template-columns: repeat(auto-fit,minmax(200px,1fr)); gap: 1rem; }
    .project-card { background: #fff; padding: 1rem; border-radius: 8px; box-shadow: 0 0 5px rgba(0,0,0,0.1); }

    /* Quiz */
    .quiz-container { background: #fff; padding: 20px; border-radius: 10px; width: 90%; max-width: 500px; margin: auto; box-shadow: 0 0 10px rgba(0,0,0,0.2); }
    .quiz-container ul { list-style: none; margin-bottom: 20px; }
    .quiz-container ul li { margin: 10px 0; }
    .quiz-container button { background: #333; color: white; padding: 10px 15px; border: none; border-radius: 5px; cursor: pointer; }
    .quiz-container button:hover { background: #555; }
    .quiz-container .result { font-size: 18px; font-weight: bold; text-align: center; }

    /* Blog */
    .post { background: white; padding: 15px; margin-bottom: 20px; border-radius: 8px; box-shadow: 0 0 5px rgba(0,0,0,0.1); }
    .post h2 { margin: 0 0 10px; }
    .post small { color: gray; font-size: 12px; }

    /* Responsive Website Demo */
    .responsive-demo nav { display: flex; justify-content: center; background: #444; flex-wrap: wrap; }
    .responsive-demo nav a { color: white; padding: 1rem; text-decoration: none; text-align: center; }
    .responsive-demo nav a:hover { background: #666; }
    .responsive-demo .container { display: grid; grid-template-columns: 3fr 1fr; gap: 1rem; padding: 1rem; }
    .responsive-demo .content, .responsive-demo .sidebar { background: #f4f4f4; padding: 1rem; border-radius: 8px; }
    @media (max-width: 768px) { .responsive-demo .container { grid-template-columns: 1fr; } }

    footer { text-align: center; background: #333; color: white; padding: 1rem; margin-top: 2rem; }
  </style>
</head>
<body>
  <!-- Navbar -->
  <header>
    <nav>
      <div class="logo">reshmi's Portfolio</div>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#quiz">Quiz App</a></li>
        <li><a href="#blog">Blog</a></li>
        <li><a href="#responsive">Responsive Site</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero -->
  <section id="home" class="hero">
    <div>
      <h1>Hello, I'm <span>reshmi</span></h1>
      <p>Student passionate about technology & design.</p>
      <a href="#projects" class="btn">View My Work</a>
    </div>
  </section>

  <!-- About -->
  <section id="about" class="about">
    <h2>About Me</h2>
    <div class="about-content">
      <img src="IMG-20250915-WA0007.jpg" alt="Profile Photo">
      <p>I love building interactive, user-friendly web applications and exploring new tools in the tech world.</p>
    </div>
  </section>

  <!-- Portfolio Projects -->
  <section id="projects" class="projects">
    <h2>My Projects</h2>
    <div class="project-grid">
      <div class="project-card"><h3>Responsive Website</h3><p>A simple responsive website.</p></div>
      <div class="project-card"><h3>Quiz App</h3><p>JavaScript-based quiz app.</p></div>
      <div class="project-card"><h3>Personal Blog</h3><p>Blog with local storage CMS.</p></div>
    </div>
  </section>

  <!-- Science Quiz -->
  <section id="quiz">
    <h2>Science Quiz App</h2>
    <div class="quiz-container" id="quizBox">
      <h2 id="question">Question text</h2>
      <ul>
        <li><label><input type="radio" name="answer" class="answer" id="a"> <span id="a_text">Answer A</span></label></li>
        <li><label><input type="radio" name="answer" class="answer" id="b"> <span id="b_text">Answer B</span></label></li>
        <li><label><input type="radio" name="answer" class="answer" id="c"> <span id="c_text">Answer C</span></label></li>
        <li><label><input type="radio" name="answer" class="answer" id="d"> <span id="d_text">Answer D</span></label></li>
      </ul>
      <button id="submit">Submit</button>
      <div class="result" id="result"></div>
    </div>
  </section>

  <!-- Blog -->
  <section id="blog">
    <h2>My Blog</h2>
    <div class="container" id="postsContainer"></div>
  </section>

  <!-- Responsive Website Demo -->
  <section id="responsive" class="responsive-demo">
    <h2>Responsive Website Demo</h2>
    <nav>
      <a href="#">Home</a><a href="#">About</a><a href="#">Services</a><a href="#">Contact</a>
    </nav>
    <div class="container">
      <div class="content"><h3>Main Content</h3><p>Resize the window to see the responsive effect.</p></div>
      <div class="sidebar"><h3>Sidebar</h3><p>Extra information or links.</p></div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h2>Contact Me</h2>
    <form id="contact-form">
      <input type="text" name="user_name" placeholder="Your Name" required>
      <input type="email" name="user_email" placeholder="Your Email" required>
      <textarea name="message" placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
    </form>
    <p id="form-status"></p>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 reshmi | All rights reserved</p>
  </footer>

  <script>
    /* Quiz Script */
    const quizData = [
      {question: "what does CSS stand for?", a:"computer style sheets", b:"cascading style sheets", c:"Creative style sheets", d:"concise style sheets", correct:"b"},
      {question: "What planet is known as the Red Planet?", a:"Venus", b:"Saturn", c:"Mars", d:"Jupiter", correct:"c"},
      {question: "What force keeps us on the ground?", a:"Magnetism", b:"Friction", c:"Gravity", d:"Inertia", correct:"c"},
      {question: "what is JavaScript primarily used for?", a:"styling web pages", b:"creating database queries", c:"adding interactivity to web pages", d:"managing server side logic", correct:"c"}
    ];
    const answerEls=document.querySelectorAll(".answer"),questionEl=document.getElementById("question"),
      a_text=document.getElementById("a_text"),b_text=document.getElementById("b_text"),
      c_text=document.getElementById("c_text"),d_text=document.getElementById("d_text"),
      submitBtn=document.getElementById("submit"),resultEl=document.getElementById("result");
    let currentQuiz=0,score=0;
    loadQuiz();
    function loadQuiz(){deselectAnswers();const currentQuizData=quizData[currentQuiz];
      questionEl.innerText=currentQuizData.question;a_text.innerText=currentQuizData.a;
      b_text.innerText=currentQuizData.b;c_text.innerText=currentQuizData.c;d_text.innerText=currentQuizData.d;}
    function getSelected(){let answer;answerEls.forEach(el=>{if(el.checked){answer=el.id;}});return answer;}
    function deselectAnswers(){answerEls.forEach(el=>el.checked=false);}
    submitBtn.addEventListener("click",()=>{const answer=getSelected();
      if(answer){if(answer===quizData[currentQuiz].correct){score++;}currentQuiz++;
        if(currentQuiz<quizData.length){loadQuiz();}
        else{document.getElementById("quizBox").innerHTML=`<h2 class="result">You answered correctly ${score}/${quizData.length} questions.</h2><button onclick="location.reload()">Restart</button>`;}}});

    /* Blog Load */
    function loadPosts(){
      const postsContainer=document.getElementById("postsContainer");
      const posts=JSON.parse(localStorage.getItem("blogPosts"))||[];
      postsContainer.innerHTML="";
      posts.reverse().forEach(post=>{
        const postEl=document.createElement("div");
        postEl.classList.add("post");
        postEl.innerHTML=`<h2>${post.title}</h2><small>${new Date(post.date).toLocaleString()}</small><p>${post.content}</p>`;
        postsContainer.appendChild(postEl);
      });
    }
    loadPosts();
  </script>
</body>
</html>

<!DOCTYPE html> 
<html lang="en"> 
<head> 
<meta charset="UTF-8" /> 
<meta name="viewport" content="width=device-width, initial-scale=1.0"/> 
<title>Ramisetty Baladatta | Portfolio</title> 
<style> 
* { margin: 0; padding: 0; box-sizing: border-box; } 
body { 
font-family: 'Segoe UI', sans-serif; 
background-color: #f4f6f9; 
color: #222; 
min-height: 100vh; 
display: flex; 
flex-direction: column; 
} 
header { 
background: #1e1e2f; 
color: white; 
display: flex; 
justify-content: space-between; 
align-items: center; 
padding: 20px 40px; 
} 
.logo-section { 
  display: flex; 
  align-items: center; 
} 
.logo { 
  width: 50px; 
  height: 50px; 
  margin-right: 15px; 
  border-radius: 50%; 
  display: none; 
} 
nav { 
  display: flex; 
  gap: 20px; 
} 
nav button { 
  background: none; 
  border: none; 
  color: white; 
  font-size: 16px; 
  cursor: pointer; 
  padding: 5px 10px; 
} 
nav button:hover { 
  border-bottom: 2px solid #00bcd4; 
} 
main { 
  flex-grow: 1; 
  padding: 40px 20px; 
  max-width: 1000px; 
  margin: auto; 
} 
.section { 
  display: none; 
  animation: fadeIn 0.6s ease-in-out; 
} 
.section.active { 
  display: block; 
} 
.hero { 
  text-align: center; 
  margin-top: 40px; 
} 
.hero img { 
  width: 160px; 
  border-radius: 50%; 
  animation: float 3s ease-in-out infinite; 
  margin-bottom: 20px; 
  display: none; 
} 
h2 { 
  margin-bottom: 15px; 
  color: #444; 
} 
ul { 
  list-style-type: square; 
  padding-left: 20px; 
} 
.project-card { 
  background: white; 
  border: 1px solid #ddd; 
  border-radius: 10px; 
  padding: 20px; 
  margin-bottom: 20px; 
  transition: box-shadow 0.3s; 
} 
.project-card:hover { 
  box-shadow: 0 4px 10px rgba(0,0,0,0.1); 
} 
.resume-pic { 
  width: 100%; 
  max-width: 600px; 
  border-radius: 10px; 
  margin-top: 20px; 
  border: 1px solid #ccc; 
} 
.download-btn { 
  display: inline-block; 
  background: #00bcd4; 
  color: white; 
  padding: 10px 20px; 
  text-decoration: none; 
  border-radius: 6px; 
  margin-top: 10px; 
} 
footer { 
  background-color: #1e1e2f; 
  color: white; 
  text-align: center; 
  padding: 20px; 
} 
.social-icons a { 
  color: white; 
  margin: 0 10px; 
  text-decoration: none; 
} 
@keyframes float { 
  0%, 100% { transform: translateY(0); } 
  50% { transform: translateY(-10px); } 
} 
@keyframes fadeIn { 
  from { opacity: 0; transform: translateY(20px); } 
  to { opacity: 1; transform: translateY(0); } 
} 
@media(max-width: 768px) { 
  nav { flex-wrap: wrap; gap: 10px; } 
  header { flex-direction: column; align-items: flex-start; } 
} 
</style> 
</head> 
<body> 
<header> 
<div class="logo-section"> 
<img class="logo" alt="Logo" /> 
<h1>Ramisetty Baladatta</h1> 
</div> 
<nav> 
<button onclick="showSection('hero')">Home</button> 
<button onclick="showSection('about')">About</button> 
<button onclick="showSection('skills')">Skills</button> 
<button onclick="showSection('projects')">Projects</button> 
<button onclick="showSection('resume')">Resume</button> 
<button onclick="showSection('contact')">Contact</button> 
</nav> 
</header> 
<main> 
<!-- Hero Section --> 
<section id="hero" class="section active hero"> 
<img alt="My Photo"> 
<h2>Hi, I'm Bala Datta Ramisetty</h2> 
<p>Machine Learning Intern | Full-Stack Learner | Creative Developer</p> 
</section> 
<!-- About --> 
<section id="about" class="section"> 
<h2>About Me</h2> 
<p>I'm an enthusiastic ML intern based in Visakhapatnam with strong programming knowledge in 
Python, Flask, and JavaScript frameworks. Passionate about solving real-world problems through tech 
and learning continuously.</p> 
</section> 
<!-- Skills --> 
<section id="skills" class="section"> 
<h2>Skills</h2> 
<ul> 
<li>Python</li> 
<li>Machine Learning</li> 
<li>Flask</li> 
<li>React.js</li> 
<li>HTML, CSS, JavaScript</li> 
</ul> 
</section> 
<!-- Projects --> 
<section id="projects" class="section"> 
<h2>Projects</h2> 
<div class="project-card"> 
<h3>Smart Parking Management System</h3> 
<p>Built a smart parking app with real-time UPI payment, slot visualization, and email reminders 
using Flask + SQLite.</p> 
</div> 
<div class="project-card"> 
<h3>Personal Portfolio Website</h3> 
<p>This modern and responsive portfolio you’re browsing, showcasing skills, projects, and 
animated visuals.</p> 
</div> 
</section> 
<!-- Resume --> 
<section id="resume" class="section"> 
<h2>Resume</h2> 
<a href="resume.jpg" class="download-btn" download="Ramisetty_Baladatta_Resume.jpg">Download Resume</a> 
<img src="resume.jpg" alt="Resume" class="resume-pic"> 
</section> 
<!-- Contact --> 
<section id="contact" class="section"> 
<h2>Contact Me</h2> 
<p><strong>Phone:</strong> 7075451091</p> 
<p><strong>Email:</strong> ramisettybaladatta8@gmail.com</p> 
</section> 
</main> 
<footer> 
<p>© 2025 Ramisetty Baladatta. All rights reserved.</p> 
<div class="social-icons"> 
<a href="#">LinkedIn</a> | 
<a href="#">GitHub</a> | 
<a href="#">Twitter</a> 
</div> 
</footer> 
<script> 
function showSection(id) { 
document.querySelectorAll('.section').forEach(sec => { 
sec.classList.remove('active'); 
}); 
document.getElementById(id).classList.add('active'); 
} 
</script> 
</body> 
</html>

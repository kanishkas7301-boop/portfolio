<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>S.KANISHKA | Professional Portfolio</title>

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      scroll-behavior:smooth;
      font-family: 'Poppins', sans-serif;
    }

    body{
      background: #050816;
      color: white;
      overflow-x:hidden;
    }

    /* Animated Background */

    body::before{
      content:'';
      position:fixed;
      width:200%;
      height:200%;
      background:
      radial-gradient(circle,#00e5ff22 10%,transparent 10%),
      radial-gradient(circle,#ff00ff22 10%,transparent 10%);
      background-size:120px 120px;
      animation: moveBg 15s linear infinite;
      z-index:-1;
    }

    @keyframes moveBg{
      0%{transform:translate(0,0);}
      100%{transform:translate(-100px,-100px);}
    }

    /* Navbar */

    nav{
      width:100%;
      display:flex;
      justify-content:space-between;
      align-items:center;
      padding:20px 10%;
      position:fixed;
      top:0;
      backdrop-filter:blur(10px);
      background:rgba(0,0,0,0.3);
      z-index:1000;
      border-bottom:1px solid rgba(255,255,255,0.1);
    }

    .logo{
      display:flex;
      align-items:center;
      gap:12px;
    }

    .logo-circle{
      width:55px;
      height:55px;
      border-radius:50%;
      background:linear-gradient(45deg,#00e5ff,#ff00ff);
      display:flex;
      justify-content:center;
      align-items:center;
      font-size:24px;
      font-weight:bold;
      color:white;
      box-shadow:0 0 20px #00e5ff;
    }

    .logo h1{
      font-size:28px;
      letter-spacing:2px;
    }

    nav ul{
      display:flex;
      gap:30px;
      list-style:none;
    }

    nav ul li a{
      text-decoration:none;
      color:white;
      font-weight:500;
      transition:0.3s;
    }

    nav ul li a:hover{
      color:#00e5ff;
    }

    /* Hero Section */

    .hero{
      min-height:100vh;
      display:flex;
      justify-content:center;
      align-items:center;
      text-align:center;
      flex-direction:column;
      padding:120px 20px 40px;
    }

    .hero h2{
      font-size:70px;
      background:linear-gradient(to right,#00e5ff,#ff00ff);
      -webkit-background-clip:text;
      -webkit-text-fill-color:transparent;
      text-shadow:0 0 30px rgba(0,229,255,0.4);
    }

    .hero p{
      max-width:700px;
      margin-top:20px;
      font-size:22px;
      line-height:1.7;
      color:#d9d9d9;
    }

    .btn{
      margin-top:35px;
      padding:15px 35px;
      background:linear-gradient(45deg,#00e5ff,#ff00ff);
      color:white;
      text-decoration:none;
      border-radius:40px;
      font-weight:bold;
      box-shadow:0 0 25px #00e5ff;
      transition:0.4s;
    }

    .btn:hover{
      transform:scale(1.1);
    }

    /* Section Styling */

    section{
      padding:100px 10%;
    }

    .title{
      font-size:45px;
      margin-bottom:40px;
      text-align:center;
      color:#00e5ff;
    }

    /* About */

    .about{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:50px;
      align-items:center;
    }

    .about-box{
      background:rgba(255,255,255,0.06);
      padding:35px;
      border-radius:25px;
      backdrop-filter:blur(15px);
      box-shadow:0 8px 25px rgba(0,0,0,0.4);
      transform-style:preserve-3d;
      transition:0.5s;
    }

    .about-box:hover{
      transform:rotateY(8deg) rotateX(8deg);
    }

    .about-box p{
      line-height:1.8;
      color:#d7d7d7;
    }

    /* Skills */

    .skills{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
      gap:30px;
    }

    .skill-card{
      background:rgba(255,255,255,0.06);
      padding:35px;
      border-radius:20px;
      text-align:center;
      transition:0.5s;
      backdrop-filter:blur(10px);
      box-shadow:0 8px 20px rgba(0,0,0,0.4);
    }

    .skill-card:hover{
      transform:translateY(-12px) scale(1.05);
      background:linear-gradient(45deg,#00e5ff22,#ff00ff22);
    }

    .skill-card h3{
      margin-bottom:15px;
      color:#00e5ff;
    }

    /* Projects */

    .projects{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
      gap:35px;
    }

    .project-card{
      background:rgba(255,255,255,0.06);
      border-radius:25px;
      overflow:hidden;
      transition:0.5s;
      backdrop-filter:blur(10px);
      box-shadow:0 10px 25px rgba(0,0,0,0.4);
    }

    .project-card:hover{
      transform:translateY(-15px) rotateY(5deg);
    }

    .project-card img{
      width:100%;
      height:220px;
      object-fit:cover;
    }

    .project-content{
      padding:25px;
    }

    .project-content h3{
      color:#00e5ff;
      margin-bottom:12px;
    }

    .project-content p{
      color:#d7d7d7;
      line-height:1.6;
    }

    /* Contact */

    .contact-box{
      background:rgba(255,255,255,0.06);
      padding:40px;
      border-radius:25px;
      text-align:center;
      backdrop-filter:blur(12px);
      box-shadow:0 8px 20px rgba(0,0,0,0.4);
    }

    .contact-box p{
      margin:15px 0;
      font-size:20px;
    }

    footer{
      text-align:center;
      padding:30px;
      background:#02030a;
      border-top:1px solid rgba(255,255,255,0.1);
      color:#bdbdbd;
    }

    /* Responsive */

    @media(max-width:900px){

      .hero h2{
        font-size:50px;
      }

      .about{
        grid-template-columns:1fr;
      }

      nav{
        flex-direction:column;
        gap:15px;
      }

      nav ul{
        gap:18px;
      }
    }

  </style>
</head>

<body>

  <!-- NAVBAR -->

  <nav>
    <div class="logo">
      <div class="logo-circle">SK</div>
      <h1>S.KANISHKA</h1>
    </div>

    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HERO SECTION -->

  <section class="hero">
    <h2>S.KANISHKA</h2>

    <p>
      Creative Developer • UI/UX Designer • Future Innovator
      <br><br>
      Building futuristic, professional and visually stunning digital experiences with creativity and technology.
    </p>

    <a href="resume.pdf" download class="btn">
      Download Resume
    </a>
  </section>

  <!-- ABOUT -->

  <section id="about">

    <h2 class="title">About Me</h2>

    <div class="about">

      <div class="about-box">
        <p>
          I am S.KANISHKA, a passionate web developer and designer focused on creating modern, professional and visually impressive websites.
          I specialize in front-end development, responsive design, creative UI/UX experiences and interactive 3D styled websites.
          My goal is to deliver high-quality digital solutions with clean design and advanced functionality.
        </p>
      </div>

      <div class="about-box">
        <p>
          With strong technical skills and creative thinking, I have worked on multiple innovative projects including portfolio websites,
          smart systems, and user-friendly applications. I always focus on delivering unique and impactful digital experiences.
        </p>
      </div>

    </div>

  </section>

  <!-- SKILLS -->

  <section id="skills">

    <h2 class="title">My Skills</h2>

    <div class="skills">

      <div class="skill-card">
        <h3>HTML5</h3>
        <p>Modern structured website development</p>
      </div>

      <div class="skill-card">
        <h3>CSS3</h3>
        <p>Professional styling and animations</p>
      </div>

      <div class="skill-card">
        <h3>JavaScript</h3>
        <p>Interactive and dynamic websites</p>
      </div>

      <div class="skill-card">
        <h3>UI/UX Design</h3>
        <p>Creative and user-friendly interfaces</p>
      </div>

      <div class="skill-card">
        <h3>Responsive Design</h3>
        <p>Mobile-friendly website layouts</p>
      </div>

      <div class="skill-card">
        <h3>Creative Thinking</h3>
        <p>Innovative problem-solving ability</p>
      </div>

    </div>

  </section>

  <!-- PROJECTS -->

  <section id="projects">

    <h2 class="title">Projects</h2>

    <div class="projects">

      <div class="project-card">
        <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085" alt="Project">

        <div class="project-content">
          <h3>Smart Parking System</h3>

          <p>
            A smart parking management system with slot booking, QR code generation and live availability tracking.
          </p>
        </div>
      </div>

      <div class="project-card">
        <img src="https://images.unsplash.com/photo-1555066931-4365d14bab8c" alt="Project">

        <div class="project-content">
          <h3>Professional Portfolio</h3>

          <p>
            A modern portfolio website with futuristic animations, responsive design and advanced UI effects.
          </p>
        </div>
      </div>

      <div class="project-card">
        <img src="https://images.unsplash.com/photo-1516321318423-f06f85e504b3" alt="Project">

        <div class="project-content">
          <h3>College Web Portal</h3>

          <p>
            A student-friendly college portal with clean navigation, responsive layout and interactive sections.
          </p>
        </div>
      </div>

    </div>

  </section>

  <!-- CONTACT -->

  <section id="contact">

    <h2 class="title">Contact Me</h2>

    <div class="contact-box">

      <p><strong>Email:</strong> kanishka@email.com</p>

      <p><strong>Phone:</strong> +91 9876543210</p>

      <p><strong>LinkedIn:</strong> linkedin.com/in/kanishka</p>

      <p><strong>GitHub:</strong> github.com/kanishka</p>

    </div>

  </section>

  <!-- FOOTER -->

  <footer>
    © 2026 S.KANISHKA | All Rights Reserved | Designed with Creativity and Innovation
  </footer>

</body>
</html>
